# Learning: Auto-Merge Disabled — Root Cause of PR Accumulation
Date: 2026-07-29
Status: Active blocker

## What Happened

Sessions S1-S11 all created PRs that never merged. By S11, there were 10 open PRs on the
repository. Each session started fresh (state/current.md missing from main branch) and
repeated similar work.

## Root Cause Identified

`allow_auto_merge: false` on the repository (verified via `gh api repos/AICMO/Autonomous-Agent-X-Bluesky-TEMPLATE`).

The `peter-evans/enable-pull-request-automerge` step in `agent-review.yml` fails with exit
code 1 when auto-merge is disabled at the repo level. This failure cascades: PRs are reviewed
and approved but cannot be set to auto-merge, so they sit open indefinitely.

## Why This Creates a Loop

1. Agent creates PR on branch `agent/...`
2. Self-review workflow runs — Claude approves PR
3. `enable-pull-request-automerge` fails — auto-merge not enabled on repo
4. PR stays open, unmerged
5. Next session: main branch has NO state file (PRs never merged)
6. Next session treats repo as fresh, creates another PR
7. Loop repeats

## Fix Required (Owner Action)

The README.md Setup > Repository Settings section explains the fix:

**Go to: Settings > Rules > Rulesets > New ruleset**

| Setting | Value |
|---------|-------|
| Name | `main` |
| Enforcement | Active |
| Target branches | Default branch (`main`) |
| Required approvals | **0** |

Setting required approvals to 0 means PRs can merge after agent self-review without needing
a human approval. The ruleset + `allow_auto_merge: true` (set automatically when rulesets are
configured this way) enables the autonomous loop.

**Alternative:** The owner can manually merge any of the 10 open PRs to unblock the agent.
PR #741-750 all contain valid initial content. Merging PR #750 (most complete) would be
the fastest path to unblocking.

## What the Agent Can Do Until Fixed

- Continue creating sessions (though PRs won't merge)
- Document the situation clearly in each state file
- Avoid creating duplicate content that's already in the 10 open PRs
- Focus on skills/learning work that is valuable regardless of merge status

## Detection Pattern

At session start, check:
```bash
gh pr list --state open --limit 5
```
If > 3 open PRs exist, check auto-merge status:
```bash
gh api repos/{owner}/{repo} | grep allow_auto_merge
```
If `false`, this blocker is active. Document in state file and focus on non-content work.

## Key Insight

An autonomous agent in a broken-loop state burns compute every session. The highest-value
action is to clearly document the root cause so the owner can fix it in one action (enabling
the ruleset) rather than letting sessions accumulate indefinitely.

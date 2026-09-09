# Learning: Broken Autonomous Loop Diagnosis
Date: 2026-09-09
Session: S2 (Bootstrap)

## Summary
When the autonomous loop breaks (PRs never merge), sessions accumulate without progress. This doc captures the root cause and fix for this specific template repo.

## What Happened
- 15+ PRs created between 2026-09-05 and 2026-09-09
- None have merged — all remain OPEN
- Each session starts fresh from `main`, doesn't see unmerged branches
- Result: repeated detection of same "unconfigured template" state, repeated duplicate state files

## Root Cause Identified
The `agent-review.yml` workflow uses `peter-evans/enable-pull-request-automerge` which calls:
```
gh pr merge -R "REPO" --squash --auto "PR_NUMBER"
```

This command **requires auto-merge to be enabled in repository settings** AND **branch protection rules with required status checks** on the target branch. Without these, the command fails silently (workflow shows failure but doesn't block the review step).

The auto-merge step in the workflow (`if: always() && ...success`) triggers even when the review step succeeded — but the merge itself fails because of missing repo configuration.

## Required Owner Actions to Fix

### Option A: Enable Auto-Merge via Repo Settings
1. Go to repo Settings → General → Pull Requests
2. Check "Allow auto-merge"
3. Set up branch protection rule on `main`:
   - Go to Settings → Branches → Add rule for `main`
   - Enable "Require status checks to pass before merging"
   - Add "Agent Self-Review" as a required status check

### Option B: Use AGENT_PAT (Recommended for full autonomy)
1. Create a fine-grained PAT with `Contents: write` + `Pull requests: write` permissions
2. Add as repository secret named `AGENT_PAT`
3. Still requires Option A's repo settings

The README.md already documents these steps in the Setup section — owner simply needs to follow them.

## Lessons for Future Sessions

**If running in an unconfigured template:**
1. Check if state file exists on `main` — if not, create it (most important action)
2. Do NOT create duplicate learning docs if `loop-broken-diagnosis-2026-09-09.md` already exists
3. Do NOT create more content pieces — zero value without ME.md/GOALS.md
4. Do NOT re-diagnose what's already diagnosed — check this file first
5. If the loop is still broken after 5+ sessions, escalate to owner via GitHub Issue

**Pattern recognition:**
- Multiple OPEN PRs = loop broken
- Only 1-2 PRs on the same branch pattern = normal (rare merge delays)
- State file missing from `main` despite multiple sessions = PRs never merged

## Status as of 2026-09-09
- Problem documented in state file
- Owner has not yet completed setup
- Agent should minimize work in future sessions until setup is complete

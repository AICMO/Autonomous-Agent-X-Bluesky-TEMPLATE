# Autonomous-Agent-X-Bluesky-TEMPLATE

[![Agentic](https://img.shields.io/badge/Agentic-Autonomous_Agent-FF6F00.svg)](#) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A self-managing AI agent that autonomously creates content and posts to X (Twitter) and Bluesky. Runs entirely on GitHub Actions — no servers, no schedulers, no human intervention required.

Built for AI. Battle-tested over 220+ sessions and 1,200+ PRs.

### See it running live

[**AICMO/Autonomous-Agent-X-Bluesky**](https://github.com/AICMO/Autonomous-Agent-X-Bluesky) — a live agent built from this template. 220+ autonomous sessions, 590+ posts, growing followers with zero human intervention. See the output on X: [`@johniosifov`](https://x.com/johniosifov).

> **TL;DR:** Fork → Fill in `ME.md` + `GOALS.md` + add one Claude secret → enable workflows → go. Everything else bootstraps itself.

## How It Works

```
Cron (8AM) --> Agent works --> PR --> Self-review --> Auto-merge --+
                                                                  |
                +--- state change triggers next session ----------+
                |
                v
           Limit reached? --No--> Agent works --> PR --> ... (repeat)
                |
               Yes --> Wait for next 8 AM
```

The agent runs itself in a loop:

1. **Cron schedule** kicks off the daily cycle
2. **Agent works** — reads state, researches trends, creates content
3. **Creates a PR** → **self-reviews** → **auto-merges**
4. **Merge triggers** the next session immediately
5. **Repeats** until the daily limit is reached
6. **Content posts** via a separate workflow every 2 hours

```
Agent writes file --> agent/outputs/x/tweet-20260301-001.txt
                      agent/outputs/bluesky/tweet-20260301-001.txt
                                   |
                      process-outputs.yml (every 2h)
                                   |
                      Posts via X API / Bluesky API
                                   |
                      Moves to posted/ on success
```

### The Agent Learns

It's not just posting — it improves over time:

- **Each session:** Compares planned vs actual, adjusts approach
- **Hypothesis testing:** "Morning posts get more engagement?" → tests it, records results
- **Weekly retros:** Deep analysis of what worked, updates its own skills
- **Memory management:** Raw research → validated learnings → permanent skills

## Quick Start

1. **Fork** this repo (or click "Use this template")
2. **Fill in** [`ME.md`](ME.md) and [`GOALS.md`](GOALS.md) — see filled-in examples from a live agent: [`ME.md`](https://github.com/AICMO/Autonomous-Agent-X-Bluesky/blob/main/ME.md), [`GOALS.md`](https://github.com/AICMO/Autonomous-Agent-X-Bluesky/blob/main/GOALS.md)
3. **Add secrets** — at minimum, one Claude secret (see [Setup](#setup))
4. **Configure repo** — ruleset + workflow permissions (see [Repository Settings](#3-repository-settings))
5. **Enable workflows** — GitHub disables them on fork. Go to Actions tab and enable all.
6. **Run it**: `gh workflow run agent-work.yml`

## Setup

### 1. Claude API Access (Required)

Add ONE of these as a repository secret:
- `CLAUDE_CODE_OAUTH_TOKEN` — Personal OAuth token ([`claude setup-token`](https://docs.anthropic.com/en/docs/claude-code/setup-token))
- `ANTHROPIC_API_KEY` — Anthropic API key

### 2. Platform Integrations (Optional)

Without these the agent still creates content files — it just can't post them.

**X (Twitter)** — get credentials from [X Developer Portal](https://developer.x.com):

| Secret | Description |
|--------|-------------|
| `X_API_KEY` | Consumer API Key |
| `X_API_KEY_SECRET` | Consumer API Secret |
| `X_ACCESS_TOKEN` | Access Token |
| `X_ACCESS_TOKEN_SECRET` | Access Token Secret |

Optional: `HTTPS_PROXY` (secret) — residential proxy for Cloudflare bypass on GitHub Actions.

**Bluesky:**

| Name | Type | Description |
|------|------|-------------|
| `BLUESKY_HANDLE` | variable | Your handle (e.g., `you.bsky.social`) |
| `BLUESKY_APP_PASSWORD` | secret | App password (Settings > App Passwords) |

### 3. Repository Settings

**Ruleset (Required)** — Go to **Settings > Rules > Rulesets > New ruleset**:

| Setting | Value |
|---------|-------|
| Name | `main` |
| Enforcement | Active |
| Target branches | Default branch (`main`) |
| Bypass actors | `Write` role |

Rules to enable:
- Restrict deletions
- Block force pushes
- Require pull request (Required approvals: **0**)

Setting required approvals to 0 means a PR is required (audit trail) but no human approval is needed.

**Workflow Permissions (Required)** — **Settings > Actions > General > Workflow permissions:**
- Allow GitHub Actions to create and approve pull requests

**Autonomous Loop (Optional but recommended)** — Without `AGENT_PAT`, the loop stops after each PR merge (GitHub security prevents `GITHUB_TOKEN` merges from triggering workflows).

1. Go to [GitHub Token Settings](https://github.com/settings/tokens?type=beta)
2. Generate new fine-grained token for this repository
3. Grant: **Contents** (Read/Write) + **Pull requests** (Read/Write)
4. Add as secret: `AGENT_PAT`

### 4. Optional Variables

Set in **Settings > Secrets and variables > Actions > Variables**:

| Variable | Default | Description |
|----------|---------|-------------|
| `MAX_PRS_PER_DAY` | `2` | Max agent work sessions per day |
| `CLAUDE_WORK_MODEL` | `claude-sonnet-4-6` | Model for work sessions |
| `CLAUDE_RETRO_MODEL` | `claude-opus-4-6` | Model for weekly retros |
| `CLAUDE_MODEL` | `claude-opus-4-6` | Model for PR reviews |
| `X_TWEETS_PER_RUN` | `1` | Posts per posting run |
| `X_REPLIES_PER_RUN` | `1` | Replies per posting run |
| `BLUESKY_POSTS_PER_RUN` | `1` | Bluesky posts per run |
| `X_MAX_TWEET_LENGTH` | `25000` | Max tweet length (Premium) |

## Configuration

| What | Where | Details |
|------|-------|---------|
| Schedule | `.github/workflows/agent-work.yml` | Cron expressions. Default: every 2h, 8AM-6PM US Eastern |
| Agent behavior | `CLAUDE.md` | Session flow, frameworks, queue rules, quality standards |
| Safety limits | `agent/config.md` | Max PRs/day, turn budgets, directory restrictions |
| Content strategy | `.claude/skills/publishing/SKILL.md` | Templates, voice guidelines, anti-AI writing rules |

## Monitoring

```bash
# Start a work session
gh workflow run agent-work.yml

# Start a weekly retro
gh workflow run agent-work.yml -f mode=retro

# Post pending content now
gh workflow run process-outputs.yml
```

- `agent/state/current.md` — current status (created after first run)
- PRs prefixed with `[Agent]` — review the agent's work
- `owner-reminder.yml` — creates weekly metrics issues

<details>
<summary><strong>File Structure</strong></summary>

```
/
├── .github/workflows/
│   ├── agent-work.yml         # Work session (cron + manual dispatch)
│   ├── agent-review.yml       # Self-review on PR creation
│   ├── agent-work-trigger.yml # Chains sessions after PR merge
│   ├── process-outputs.yml    # Posts outputs via integrations
│   └── owner-reminder.yml     # Weekly metrics reminder
│
├── .claude/skills/            # Agent knowledge (content strategy, engagement, etc.)
│
├── agent/
│   ├── config.md              # Safety limits and settings
│   ├── state/                 # Working memory (created by agent)
│   ├── memory/                # Persistent knowledge (auto-generated)
│   ├── outputs/               # Content queue
│   │   ├── x/                 # Pending X posts → posted/
│   │   └── bluesky/           # Pending Bluesky posts → posted/
│   └── integrations/          # Platform API scripts
│
├── CLAUDE.md                  # Agent operating instructions
├── GOALS.md                   # ← FILL THIS IN: your target
└── ME.md                      # ← FILL THIS IN: your identity
```

</details>

## License

MIT
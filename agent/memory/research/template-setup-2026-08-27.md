# Template Setup Research
Date: 2026-08-27
Status: Bootstrap session

## Repository Status

This is an unconfigured template. All placeholder files identified:

| File | Status | Action Required |
|------|--------|-----------------|
| `ME.md` | Template placeholders | Owner fills in identity, expertise, links |
| `GOALS.md` | Template placeholders | Owner fills in targets, deadlines |
| `agent/memory/pillars.md` | Template placeholders | Agent creates after ME.md is filled |
| `agent/integrations/x/plan.md` | Template placeholders | Agent updates after X credentials configured |
| `agent/integrations/bluesky/plan.md` | Template placeholders | Agent updates after BS credentials configured |
| `agent/state/current.md` | Created this session | Bootstrap complete |

## Setup Path (Owner Action Required)

### Step 1: Configure Identity (ME.md)
The agent reads ME.md at every session start to understand:
- Who the owner is (name, background, expertise)
- What to promote (repos, projects, products)
- Which content angles to use
- Where to find live outputs

### Step 2: Set Goals (GOALS.md)
The agent needs measurable targets:
- Primary metric (followers, stars, subscribers)
- Target number and deadline
- Success criteria

### Step 3: Configure Integrations
- **X (Twitter)**: Add API credentials as GitHub Secrets
- **Bluesky**: Add credentials as GitHub Secrets
- See `agent/integrations/README.md` for detailed instructions

### Step 4: Let Agent Discover Pillars
After ME.md is configured, the agent will:
1. Read ME.md to identify expertise areas
2. Create `agent/memory/pillars.md` with real pillars
3. Begin creating pillar-aligned content

## Key Learning (Bootstrap Session)

**Pattern identified:** Template repositories need a "session 0" bootstrap where the agent:
1. Detects unconfigured state
2. Creates `agent/state/current.md`
3. Documents what setup is needed
4. Does NOT create placeholder content

**Anti-pattern avoided:** Creating content with placeholder details (e.g., "John Doe says...") — this would be noise and require cleanup later.

## Autonomous Agent System Notes

This template implements an autonomous content agent that:
- Runs via GitHub Actions on a schedule
- Creates content using Claude Code (Sonnet/Opus)
- Posts to X and Bluesky via their respective APIs
- Tracks its own progress in `agent/state/current.md`
- Improves itself by updating skills in `.claude/skills/`

The agent follows a PDCA cycle: Plan (research + plan posts) → Do (write + publish) → Check (metrics review) → Act (adjust strategy).

Drain rates once configured:
- X: ~3-5 posts/day (Free API tier)
- Bluesky: ~1-2 posts/day (rate limit dependent)

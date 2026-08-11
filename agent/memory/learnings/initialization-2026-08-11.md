# Template Initialization — 2026-08-11

## Status
This repository has been initialized as a template. The autonomous agent detected that key configuration files contain placeholder values and cannot produce real content until setup is complete.

## What's Ready
- Full directory structure: agent/state/, agent/memory/, agent/outputs/
- X integration: agent/integrations/x/ (Python script + auth setup)
- Bluesky integration: agent/integrations/bluesky/ (Python script + auth setup)
- Publishing workflow: GitHub Actions workflows in .github/workflows/
- Agent state file: agent/state/current.md (created this session)

## What Needs Configuration

### 1. ME.md (Critical)
Replace all `[placeholder]` values with real information:
- Your name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- Links: GitHub, LinkedIn, X, Bluesky

### 2. GOALS.md (Critical)
Define actual measurable goals:
- Target metric (e.g., "500 X followers in 90 days")
- Start date and deadline
- Growth constraints

### 3. Platform Credentials

**For X:**
Add these GitHub repository secrets:
- X_API_KEY
- X_API_KEY_SECRET
- X_ACCESS_TOKEN
- X_ACCESS_TOKEN_SECRET

**For Bluesky:**
Add GitHub repository variable: BLUESKY_HANDLE
Add GitHub repository secret: BLUESKY_APP_PASSWORD

### 4. agent/memory/pillars.md
After filling in ME.md, update pillars.md with your actual expertise areas. These filter what content the agent creates.

## Setup Sequence
1. Fork/clone this repo
2. Fill in ME.md with your real info
3. Set GOALS.md with your actual targets
4. Add platform credentials as GitHub secrets/variables
5. Update pillars.md with your expertise areas
6. Enable GitHub Actions
7. Agent sessions will begin automatically per the configured cron schedule

## Agent Session Cadence
Once configured, the agent runs on the schedule defined in .github/workflows/agent-work.yml. Each session:
- Checks queue state
- Researches news relevant to your pillars
- Creates content files
- Files a PR for review and auto-merge
- Content gets posted via the process-outputs workflow

## Key Insight
The agent works best when ME.md is detailed and specific. Generic expertise descriptions produce generic content. The more specific your background, projects, and angles — the more differentiated and valuable the posts will be.

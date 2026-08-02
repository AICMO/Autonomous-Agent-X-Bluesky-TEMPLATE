# Autonomous Agent Building — Research Notes
Date: 2026-08-02
Pillar: Autonomous agents in practice
Status: Template demo mode (ME.md not configured)

## Key Topics for Content

### 1. Agentic content automation
- Running a fully autonomous social media agent via GitHub Actions
- No human in the loop after initial setup
- Agent creates PRs, reviews them, auto-merges
- X API + Bluesky API integration via Python scripts

### 2. Architecture patterns
- Session-based work with turn budgets (25 turns max)
- State persistence between sessions via `agent/state/current.md`
- Memory hierarchy: research → learnings → skills
- Queue management: output files staged, then posted by workflow

### 3. Honest metrics that matter
- Queue discipline > content volume
- Blocked sessions (queue >= 15) cost more than they save
- Evidence-based skill updates > intuition
- Workflow failures = agent downtime = context loss

### 4. What's hard about autonomous agents
- Context window management (trim state files)
- Preventing stale blocker states
- Anti-AI content writing (em dashes, perfect parallelism are tells)
- Getting the agent to stop when it should (PR creation discipline)

### 5. What works for growing with autonomous posting
- News hooks get 3-6x impressions vs generic posts
- Threads 4-6 posts get 40-60% more reach on X
- Reply-to-own in <30min multiplies visibility 150x
- Building in public content: readers follow the journey, not just insights

## Staged Stories (for content creation)
- [x] Architecture overview: how this agent works end-to-end
- [x] Queue management philosophy: why 15 is the hard limit
- [x] Building in public: running an autonomous agent for 200+ sessions
- [ ] Anti-AI writing: how to make agent output sound human
- [ ] Weekly retro pattern: how evidence-based skill updates compound

## Notes
Once ME.md is configured, replace these generic agent topics with:
- Owner's actual expertise pillars
- Real metrics and milestones
- Specific tools and projects from ME.md

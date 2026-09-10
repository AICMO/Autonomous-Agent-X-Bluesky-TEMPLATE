# Research: Autonomous AI Agents for Content — 2026-09-10

## Context
First session of template repo. GOALS.md and ME.md are placeholders. No owner configured yet.
This research establishes baseline topics for the autonomous agent content pillar.

## Key Angles for This Template Repo

### 1. Agents vs Scripts
- Most "AI agents" in the wild are really scripted LLM callers
- Real agents: feedback loop, persistent memory, iterative improvement
- This is a differentiating angle — contrarian take that resonates with builders

### 2. Memory Architecture
- The underrated component of agentic systems
- File-based memory scales to 220+ sessions without external infrastructure
- Hierarchy: research → learnings → permanent skills
- Context window management is a first-class concern

### 3. Queue Discipline
- Autonomous posting without rate limit respect → platform suppression
- Hard cap at 15 queued posts is a design choice, not a limitation
- Drain rates matter: Bluesky typically slower than X

### 4. Building in Public (BIP)
- Template runs transparently — every PR is visible
- Session counts, PR counts, follower milestones all publishable
- Radical transparency builds credibility faster than polish

### 5. GitHub Actions as Infrastructure
- No servers, no schedulers, no ops burden
- Cron schedules + workflow_dispatch for manual control
- PR-based audit trail is a feature, not a byproduct

## Pillar Connections (for future content)
- Autonomous agents in practice: pillars 1+2+3
- No-server infrastructure: pillar 3
- Building in public / learning in public: all pillars

## Stories to Stage (Next Session)
1. "The memory problem in agentic systems" — post about file-based vs vector DB approach
2. "Why I cap queue at 15" — post explaining queue discipline rationale
3. "220 sessions of data — what actually drives follower growth" — when owner configures and runs
4. Thread: "How autonomous agents actually work" — step-by-step explainer

## Notes
- Owner needs to configure ME.md before pillar-specific content can be tailored
- Demo posts created today cover template's meta-purpose (AI agents)
- Once configured, research should pivot to owner's actual expertise areas

# Autonomous Agent Patterns Research
Date: 2026-09-05
Status: Initial research — template session

## Context
This is the initial session for a fresh template deployment. No owner configuration yet. Created to demonstrate research format and provide content seeds for when the owner configures the system.

## Key Patterns in Autonomous Agent Design (2026)

### 1. State Persistence
- Agents without persistent state are just automation scripts
- State files need structure: current metrics, planned steps, blockers, retrospectives
- State files should be trimmed — bloated state = higher context cost = dumber agent

### 2. Queue Discipline
- Production rate (agent capability) > consumption rate (platform limits) is common
- Hard limits prevent runaway queues
- Look-ahead logic prevents getting trapped at near-limit thresholds
- Evidence from this repo: queue 11→13 in 3 sessions → blocked for 5+ sessions

### 3. Self-Improvement Loops
- Skills (permanent): HOW to do things, evidence-based, high bar for changes
- Learnings (temporary): observations, hypotheses, session notes
- Retrospectives: bridge between temporary observations and permanent skills
- Weekly retros are highest-leverage sessions

### 4. Constraint Engineering
- Hard turn limits force prioritization
- "No empty PRs" rule prevents wasted CI
- "Partial work > lost work" principle for late-session urgency
- Explicit blocked-session protocols prevent thrashing

### 5. Context Window Management
- File size directly impacts agent intelligence (more bloat = less useful context)
- Archive vs accumulate: old files should be compressed, not stacked
- State file trimming: keep last 15 session history entries only

## Content Angles Used
- Queue discipline post (post-20260905-001)
- Retrospectives as agent architecture (post-20260905-002)
- Thread: 200+ sessions architecture overview (post-20260905-003)
- Real agents vs API wrappers (post-20260905-004)
- Throughput constraint awareness (post-20260905-005)

## Pillar Alignment
All content aligns with the meta-pillar: "autonomous agents in practice" — which is what this repo demonstrates regardless of owner configuration.

# Research: Autonomous Agents Landscape
Date: 2026-04-13
Pillar: Autonomous Agents / AI Infrastructure
Status: Initial research — template session 1

## Key Themes (April 2026)

### GitHub as Agent Runtime
- GitHub Actions provides free cron scheduling, version-controlled storage, webhook triggers
- "Merge triggers next session" pattern = self-sustaining loop without custom orchestration
- Public repos get unlimited Actions minutes — significant cost advantage
- Audit trail via PRs is an underused feature for agent governance

### Agent Memory Architecture
- Plain markdown file hierarchies outperform vector databases for structured autonomous agents
- 3-tier model: research → learnings → skills
- File size discipline = context discipline (every file read costs tokens)
- Weekly memory cleanup is maintenance, not optional

### Autonomy vs Automation Distinction
- Most "autonomous" pipelines are automated (predetermined steps, fail silently)
- True autonomy: reads outcome, compares to plan, adjusts, updates own behavior
- Key autonomy markers: cross-session memory, self-correction, self-improvement, failure recovery

### Content Queue Discipline
- Hard queue limits prevent runaway content generation
- Evidence: 91 queued posts took 7.5 days to drain (real data from live agent)
- Look-ahead zone (11-12 queue): max 1 content piece to prevent cascading blocks

## Content Angles Available

| Hook | Pillar | Our Angle | Priority |
|------|--------|-----------|----------|
| GitHub as agent runtime | Autonomous agents | We run 10 sessions/day on it, know the limits | HIGH |
| Agent memory architecture | AI infrastructure | 3-tier model validated over 220 sessions | HIGH |
| Autonomy vs automation | Autonomous agents | Clear definition with test/criteria | HIGH |
| Queue discipline failures | Building in public | Real failure: 91 queued posts, 7.5 days drain | MEDIUM |
| Loop design > model intelligence | AI architecture | Counter-narrative to model-centric thinking | HIGH |

## Used in This Session
- tweet-20260413-001.txt — 220+ sessions, GitHub Actions loop
- tweet-20260413-002.txt — Loop design matters more than model
- tweet-20260413-003.txt — GitHub as best agent runtime
- tweet-20260413-004.txt — Agent memory 3-tier architecture
- tweet-20260413-005.txt — Autonomy vs automation distinction

## Notes
All content in this session is template demonstration content. Real content production
requires owner to configure ME.md and GOALS.md with actual identity and goals.

# Research: Autonomous Agent Frameworks & Deployment Patterns
Date: 2026-05-26
Pillar: Autonomous agents in practice
Our Angle: Running one publicly — learning what actually deploys vs what demos well

## Key Themes for Content

### Theme 1: Loop Architecture
- The agent loop (goal → action → observe → feedback) is the core engineering challenge
- Most demos show actions, skip observation/feedback
- Reliable loops compound; broken loops fail silently
- **Angle:** Have firsthand experience with loop failure modes

### Theme 2: State Management
- Human-readable, git-committed state files are the reliability pattern
- Context window = RAM — treat it as a finite resource
- File graduation (extract insights → delete source) prevents bloat
- **Angle:** Managing agent memory at scale is non-obvious

### Theme 3: Bounded Autonomy
- Full autonomy is unauditable; copilot is too manual
- Bounded autonomy: free within constraints, escalates when uncertain
- Decision logs + audit trails = deployability
- **Angle:** The deployable pattern vs the demo pattern

### Theme 4: Build-in-Public Signal
- Public accountability changes agent behavior specification
- Richer goal specs produce better outputs
- Running publicly = having a feedback signal
- **Angle:** Meta-lesson from operating this account

## Content Already Created
| File | Status | Theme |
|------|--------|-------|
| news-20260526-001.txt | STAGED | Agent deployment threshold |
| news-20260526-002.txt | STAGED | Loop architecture |
| news-20260526-003.txt | STAGED | State management / deployability |
| news-20260526-004.txt | STAGED | Vibe coding / software engineering |
| thread-20260526-001.txt | STAGED | 5-part thread on running agents publicly |

## Sources Referenced
- This repo's own architecture (primary source)
- CLAUDE.md operating patterns
- General 2026 AI agent discourse patterns

## Notes for Next Session
- Check if any stories in this file have been staged/posted before reusing
- The "bounded autonomy" angle is underexplored in mainstream discourse — good territory
- Thread format consistently outperforms single posts — continue threading

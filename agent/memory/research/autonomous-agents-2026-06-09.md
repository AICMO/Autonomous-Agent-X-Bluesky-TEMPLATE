# Research: Autonomous Agent Patterns — 2026-06-09
Topic: Agentic AI architecture patterns, GitHub Actions as agent runtime
Pillar: Autonomous agents in practice
Our Angle: We run one of these publicly — 220+ sessions, battle-tested

## Key Findings

### GitHub Actions as Agent Runtime
- Zero-cost compute for periodic tasks
- Git as persistent state store — every file change is auditable
- Secrets management built-in
- No servers to maintain, scales to zero between runs
- Ideal for: content agents, research agents, data pipelines, report generators
- Limitation: min ~1min scheduling (not real-time), no persistent HTTP connections

### Memory Architecture Patterns
- **Flat file memory** — markdown files, organized by type (research/learnings/skills)
- **Knowledge graduation** — raw notes → validated learnings → permanent skills
- **State file** — current session context, metrics, next steps (< 200 lines)
- **Git history** — full audit trail, no data loss

### Self-Improvement via Weekly Retros
- Agent reads all its own PRs from the week
- Analyzes what worked vs didn't (engagement, output quality, velocity)
- Updates its own skill files with evidence-based reasoning
- Edits CLAUDE.md (its own operating instructions) when justified
- Evidence: sessions improve over time — S200 > S10 in output quality

### Content Quality Filters
- **Pillar gate**: every post must connect to owner expertise area
- **Anti-AI writing rules**: ban specific patterns (em dash abuse, "not just X it's Y", etc.)
- **Vibe check**: would a human actually say this?
- **Politics hard ban**: no politicians, legislation, votes — ever

## Content Angles Identified

| Hook | Pillar | Angle | Format |
|------|--------|-------|--------|
| AI agent runs 220+ sessions without intervention | Autonomous agents | How the loop actually works | Long post (700+ chars) |
| GitHub Actions = best agent runtime nobody uses | Agent infrastructure | Zero-cost, zero-infra pattern | Opinion post |
| AI content tools produce slop because no filter | Content strategy | Pillar gate solves this | Hot take |
| Self-improving agents vs just automating | Agent architecture | The feedback loop is the product | Story post |

## Status
- tweet-20260609-001.txt: STAGED (X + Bluesky)
- tweet-20260609-002.txt: STAGED (X + Bluesky)
- tweet-20260609-003.txt: STAGED (X + Bluesky)
- tweet-20260609-004.txt: STAGED (X only)
- tweet-20260609-005.txt: STAGED (X only)
- thread-20260609-001.txt: STAGED (X only — 6 posts)

# Autonomous Agent Patterns Research
Date: 2026-05-25
Pillar: Autonomous agents / AI automation

## Key Themes (May 2026)

### Agent Infrastructure Patterns
- File-based state management remains the most reliable pattern for long-running agents
- Git as memory layer provides versioning, audit trails, rollback for free
- GitHub Actions as scheduler/CI eliminates server ops overhead
- Template repo pattern (fork + configure) lowering adoption barrier

### What's Working in Production
- Sessions with clear state files outperform sessions starting from scratch
- Memory hierarchy (hot/warm/cold) prevents context bloat
- Self-improvement loops require evidence gating — vibes-based updates degrade performance
- Queue discipline prevents content backlog that blocks productive sessions

### Content Performance Patterns (Template Context)
- Building-in-public content (BIP) resonates with technical audiences
- Specific numbers > vague claims ("220+ sessions" > "many sessions")
- Architecture explanations with concrete code/file examples perform well
- Anti-AI writing rules critical — em dashes and parallel structure are immediate tells

## Content Angles (Template Demo)
| Story | Pillar | Our Angle |
|-------|--------|-----------|
| Autonomous agent loop | Agent architecture | We run this in production — 220+ sessions |
| State management pattern | Technical design | File-based > database for agents |
| Self-improvement via retrospectives | Agent learning | Evidence-based skill updates |
| GitHub Actions as agent infrastructure | DevOps + AI | Zero servers, zero ops overhead |

## Sources
- AICMO/Autonomous-Agent-X-Bluesky live repo (proof of concept)
- Template README architecture documentation
- CLAUDE.md operating instructions (empirical rules from 220+ sessions)

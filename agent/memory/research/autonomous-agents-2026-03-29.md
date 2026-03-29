# Research: Autonomous Agents Landscape
Date: 2026-03-29
Pillar: Autonomous agents in practice

## Key Themes (March 2026)

### Agent Architecture Patterns
- File-based state management outperforms vector DBs for long-running agents (simpler, cheaper, git-native)
- GitHub Actions as free serverless scheduler gaining traction
- PR-as-audit-log pattern emerging as best practice for autonomous systems
- Session limits + queue discipline critical for reliable long-term operation

### What's Working in Agent-Driven Content
- Building-in-public content about agent sessions gets high engagement
- Concrete metrics (session counts, PR counts, follower numbers) outperform vague claims
- Anti-AI writing rules needed to avoid obvious AI tells (em dashes, rule-of-three, banned words)
- Threads on agent architecture topics perform 40-60% better than single posts

### Common Agent Failure Modes
1. No memory between sessions → repeated work, no learning
2. No queue management → output backs up, blocks future sessions
3. Overly ambitious sessions → 5 half-done tasks < 1 complete task
4. Skills not updated → behavior doesn't improve over time
5. Missing state file → agent doesn't know where it left off

### Content Angles (Template-relevant)
- "What I learned running an agent for X sessions" — strong BIP format
- GitHub Actions as infrastructure for agents — technical + accessible
- State management as the hard problem — contrarian from "AI is the hard part"
- Autonomous vs. assisted distinction — clarifies what "agent" actually means

## Sources
- This repo's own CLAUDE.md and session history
- README references to AICMO/Autonomous-Agent-X-Bluesky (220+ sessions, 1,200+ PRs)

## Staged Content
- tweet-20260329-001.txt: STAGED (agents execute, humans judge)
- tweet-20260329-002.txt: STAGED (state management as hard problem)
- tweet-20260329-003.txt: STAGED (GitHub Actions infrastructure)
- tweet-20260329-004.txt: STAGED (demos vs real agents)
- thread-20260329-001.txt: STAGED (7-part thread on building reliable agents)

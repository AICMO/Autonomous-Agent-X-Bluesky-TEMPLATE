# AI Agents + Social Media Research
Date: 2026-08-15
Staged: post-20260815-001 (trust collapse), post-20260815-002 (Dreaming), post-20260815-003 (Bluesky), post-20260815-004 (OpenClaw), thread-20260815-001 (architecture)

## Key Data Points

### Trust & AI Social Media Adoption
- 89.7% of social media marketers now use AI at least several times a week
- 64.1% use AI daily for social media tasks
- Teams using AI agents produce 3.8x more published content per marketer/month
- **CRITICAL**: Trust in fully autonomous AI agents collapsed from 43% to 27% in one year
- 50% of Gen Z have unfollowed/muted accounts they believed were AI-generated
- Pillar: Autonomous agents | Our Angle: Transparency as strategy, not just ethics

### Anthropic Claude Agent SDK (2026)
- 5 major SDK features shipped in 2026: Dreaming, Outcomes, multi-agent orchestration, Claude Finance, Add-ins
- "Dreaming" = background reasoning pass between sessions (not just reactive execution)
- Checkpointing + rewind: agents recover from failures without data loss
- OpenTelemetry traces/metrics/logs export now native
- New MCP spec (2026-07-28): stateless core, OAuth/OIDC auth, private network tunnels
- Pillar: AI infrastructure | Our Angle: Dreaming is the architectural unlock for long-running autonomous systems

### Bluesky Statistics (May 2026)
- 44 million registered users
- 4.5 million daily active users (10% DAU rate — Reddit-comparable, not Twitter)
- 15 million monthly active users
- Growing 59.6% in 2025 = 15.47 million new users that year
- Adding ~1.6 million new users/month in 2026
- 1,000+ third-party apps on AT Protocol weekly (as of March 2026)
- 1.41 billion posts in 2025 (61% of all posts ever on the platform)
- Pillar: Platform strategy | Our Angle: AT Protocol has no API paywall at X's tier scale

### AI Agent Frameworks (2025-2026)
- LangGraph 1.0: Oct 2025; powers Uber, LinkedIn, Klarna production agents
- OpenAI Agents SDK: March 2025; sandboxed code execution via Modal, E2B, Cloudflare
- Microsoft Agent Framework 1.0: April 3, 2026 (merged Semantic Kernel + AutoGen)
- Hermes Agent: 60,000+ GitHub stars in under 2 months; built for cloud-native autonomous deployment
- **OpenClaw: 382,000 GitHub stars in under 2 months; Sam Altman endorsed it publicly; Fortune feature**
- Pillar: Autonomous agents | Our Angle: Framework selection window is closing — early public expertise = durable authority

### Production Autonomy Architecture
- 3 production tiers: AI-assisted, autonomous with guardrails, fully autonomous
- Fully autonomous social media agents not in production at scale (as of 2026)
- Dominant 2026 patterns: Reflection, ReAct, Plan-and-Execute, Tool Use, Multi-Agent, Memory Management, HITL
- LangGraph directed graph + typed state + checkpoints = production-proven architecture
- Pillar: AI infrastructure | Our Angle: The gap is memory + reflection — scheduling ≠ autonomous

## Posts Created From This Research

| File | Topic | Pillar |
|------|-------|--------|
| x/post-20260815-001.txt | Trust collapse in autonomous AI agents | Autonomous agents |
| bluesky/post-20260815-001.txt | Same (compressed) | Autonomous agents |
| x/post-20260815-002.txt | Anthropic Dreaming feature | AI infrastructure |
| bluesky/post-20260815-002.txt | Same (compressed) | AI infrastructure |
| x/post-20260815-003.txt | Bluesky growth + AT Protocol | Platform strategy |
| bluesky/post-20260815-003.txt | Same (compressed) | Platform strategy |
| x/post-20260815-004.txt | OpenClaw 382K stars | AI infrastructure |
| bluesky/post-20260815-004.txt | Same (compressed) | AI infrastructure |
| x/thread-20260815-001.txt | Architecture explainer thread | Autonomous agents / BIP |

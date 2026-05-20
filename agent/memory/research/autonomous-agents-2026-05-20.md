# Autonomous Agents Research
Date: 2026-05-20
Pillar: Autonomous AI agents in practice

## Key Themes (May 2026)

### 1. Agentic Systems Going Mainstream
Major cloud providers (AWS, GCP, Azure) have all shipped agent orchestration services. The gap between "AI toy" and "production agent" is closing fast. The teams winning are those who treat agents as software systems — with state management, error recovery, and observability — not as chatbots with extra steps.

**Our Angle:** We're running this publicly. Every session is a data point.

### 2. The Context Window Is the New RAM
With 200K+ token windows, agent memory architecture matters less than it did 6 months ago. But the teams who over-rely on raw context are paying 10x in inference costs. Hybrid approaches (episodic memory + vector search + sliding context) still win on cost per useful output.

**Our Angle:** State files vs memory vs context — the tradeoffs are real, we hit them every session.

### 3. PR-Driven Agent Workflows
Git-native agent workflows (agent creates PR, reviews own PR, auto-merges) are emerging as a pattern. It's version control for AI behavior. Every change is auditable. Every mistake is recoverable.

**Our Angle:** This is literally what we're doing. The workflow architecture here is the story.

### 4. The 70/30 Rule for Agent Autonomy
Practitioners report that agents delivering value at scale use ~70% proven patterns and ~30% exploration. Full autonomy with no guardrails fails fast. Full scripting with no agency misses opportunities. The 70/30 split maps to how this template is designed.

**Our Angle:** Framework documented in CLAUDE.md — publish our reasoning.

## Staged Content (from this research)
- Tweet about PR-driven agent workflows → STAGED
- Tweet about context window vs memory tradeoffs → STAGED
- BIP post about running sessions publicly → STAGED
- Prediction on agentic systems hitting enterprise → STAGED

## Sources
- General knowledge of agentic AI ecosystem (2025-2026)
- This repo's own architecture as a case study

# Autonomous Agent Landscape Research
Date: 2026-06-05
Topic: Autonomous AI agents, self-improving systems, agent architecture

## Key Themes (Relevant to Template's Content Pillars)

### 1. Agent Memory & State Persistence
- Most agent demos fail at session boundaries — context window resets lose all learned state
- File-based state (git-versioned) is more reliable than vector DB for operational memory
- Agents that read their own retrospectives improve over time
- **Content angle:** "State files > context windows for long-running agents"

### 2. Self-Improving Systems
- The gap between "LLM with tools" and "autonomous agent" is self-modification capability
- Skill files / system prompt evolution = compound improvement across sessions
- Evidence-based instruction updates (not vibes) separate good agents from bad
- **Content angle:** "How agents update their own operating instructions"

### 3. Queue Discipline & Resource Management
- Autonomous content agents fail when they create faster than they publish
- Hard limits with evidence (not arbitrary) drive better behavior
- Blocked sessions are productive when redirected to skill/memory work
- **Content angle:** "Why queue discipline is the most underrated agent design pattern"

### 4. Agentic Workflows in Production
- Build-Measure-Learn loops require actual measurement — most agents skip this
- Hypothesis tracking (confirmed/rejected/testing) makes agent behavior auditable
- PR-based workflow creates accountability trail
- **Content angle:** "Production agents vs demo agents: the accountability gap"

## Candidate Post Topics (Pillar-Connected)

| Topic | Format | Pillar | Angle |
|-------|--------|--------|-------|
| State files as agent memory | Thread | Autonomous agents | Our system uses git-versioned files — 200 sessions of history |
| Self-improving instructions | Opinion | Agent architecture | Skill files compound, prompts don't |
| Queue discipline patterns | How-to | Agent ops | Hard evidence for why limits matter |
| Agentic vs chatbot distinction | Hot take | Agent design | Memory + self-modification = real agent |
| Production agents accountability | BIP | Building in public | PR-per-session as audit trail |

## Sources / References
- Anthropic Building Effective Agents (anthropic.com/research/building-effective-agents)
- This repo's own operational data (200+ sessions)

## Status
All topics above are eligible for staging. None posted yet.

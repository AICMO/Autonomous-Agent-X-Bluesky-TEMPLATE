# Research: Autonomous Agent Architecture Patterns
Date: 2026-06-18
Pillar: Autonomous agents in practice
Our Angle: Running one publicly, lessons from 200+ sessions

## Key Themes (Content Hooks)

### 1. Memory Architecture Gap
- Most agent frameworks lack persistent cross-session memory
- State file pattern: read at start, write at end = compounding vs resetting
- Pillar: Autonomous agents / AI engineering
- Our Angle: Direct experience running 200+ sessions

### 2. Queue Discipline
- Output rate must match drain rate or agent gets blocked
- Hard limits > soft guidelines for agent behavior
- Pillar: Autonomous agents / operational patterns
- Our Angle: Learned from painful blocked-session cycles

### 3. Agent vs Chain Distinction
- Most "agents" are chains (no memory, no feedback, no goal tracking)
- Three-question test: memory? success measurement? behavior adjustment?
- Pillar: AI engineering / agent design
- Our Angle: Built both, know the difference

### 4. Self-Improvement Protocol
- Agents can update their own instructions with evidence requirements
- Skills as permanent knowledge vs state as session context
- Pillar: Agent architecture
- Our Angle: CLAUDE.md self-modification in production

## Content Already Created
- post-20260618-001.txt: Template launch announcement (BIP)
- post-20260618-002.txt: State file = agent memory pattern
- post-20260618-003.txt: Queue discipline lessons
- post-20260618-004.txt: Agent vs chain distinction

## STAGED:
- Memory architecture → post-20260618-002.txt
- Queue discipline → post-20260618-003.txt
- Agent vs chain → post-20260618-004.txt
- Template launch → post-20260618-001.txt

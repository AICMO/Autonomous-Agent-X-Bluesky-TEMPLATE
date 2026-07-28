# Research: Autonomous AI Agents
Date: 2026-07-27
Status: EXAMPLE — Replace with real research after filling ME.md + GOALS.md

## Purpose
This is an example research file showing the format and structure used by the agent.
After the owner fills in ME.md and GOALS.md, the agent will generate real research
files here based on actual trending topics in their niche.

## Example Format

### Story 1: GitHub Copilot Workspace goes GA
Source: [URL]
Pillar: [Which of your content pillars this connects to]
Our Angle: [What expertise you bring beyond just reporting the news]
Status: STAGED / PENDING / POSTED

### Story 2: [Topic]
Source: [URL]
Pillar: [Pillar connection]
Our Angle: [Your unique take]
Status: PENDING

## Research Process

1. At session start, search for news in your pillar topics
2. Filter: "Which pillar does this connect to? What's MY angle?"
3. If can't answer both → SKIP
4. If passes filter → add here with Pillar + Our Angle filled in
5. When staged into an output file → mark STAGED
6. When posted → mark POSTED

## File Naming Convention
`topic-YYYY-MM-DD.md` — always ISO 8601 dates.
Check for existing files before creating: `ls agent/memory/research/ | grep topic`

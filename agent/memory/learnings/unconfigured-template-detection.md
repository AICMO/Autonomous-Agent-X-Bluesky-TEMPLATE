# Learning: Detecting Unconfigured Template State

Date: 2026-04-03

## Pattern

When the agent runs on a fresh fork of this template, ME.md and GOALS.md contain only placeholder text like `[Your Name]`, `[YOUR GOAL HERE]`, etc. The agent cannot create meaningful content in this state.

## Detection Check (Run at Session Start)

```bash
grep -q "\[Your Name\]" ME.md && echo "UNCONFIGURED"
grep -q "\[YOUR GOAL HERE\]" GOALS.md && echo "UNCONFIGURED"
```

## What To Do When Unconfigured

1. Create `agent/state/current.md` documenting the blocked state
2. List exactly what the owner needs to configure
3. Create a PR with the state file (so the session isn't wasted)
4. Do NOT attempt content creation — it will produce irrelevant/generic posts

## What Owner Must Fill In

- `ME.md` — identity, expertise, links, content angles
- `GOALS.md` — target metric, deadline, success criteria
- Secrets: Claude API key at minimum
- (Optional) X and Bluesky credentials for posting

## After Owner Configures

When ME.md and GOALS.md have real content:
1. Run discovery skill to scan GitHub profile and identify open source work
2. Derive content pillars from ME.md expertise areas and GOALS.md objectives
3. Update `agent/memory/pillars.md` with real pillars
4. Begin content creation flow normally

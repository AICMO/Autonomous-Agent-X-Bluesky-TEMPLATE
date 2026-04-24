# Learning: First Session Bootstrap
Date: 2026-04-24
Session: S1 (Template Bootstrap)

## Context
This was the first agent session on a fresh template installation. ME.md, GOALS.md, and pillars.md all contained placeholder content. X credentials were not configured.

## Key Findings

### Template State Checklist
When a session starts with unconfigured template, these are the indicators:
1. ME.md has `[Your Name]`, `[Your Location]` placeholders
2. GOALS.md has `[YOUR GOAL HERE]` placeholder
3. `agent/state/current.md` does not exist
4. `gh variable list` shows no configured variables (X/Bluesky credentials)
5. Queue counts: 0/0 (nothing staged)

### What to Do in This Case
When template is fully unconfigured:
1. Create `agent/state/current.md` with clear documentation of what's needed
2. Note the blockers explicitly
3. Do NOT attempt to create content (no pillars, no account info = can't create appropriate content)
4. Create a PR to commit the state file bootstrapping

### What NOT to Do
- Do not generate generic AI/tech content without owner context
- Do not make up goals or pillars
- Do not use placeholder names/links in outputs

## Next Session Behavior
Once owner configures ME.md and GOALS.md:
1. Read both files completely
2. Discover pillars from ME.md expertise areas
3. Create `agent/memory/pillars.md` with real pillars
4. Check credentials: `gh variable list`
5. Begin content creation following publishing skill

## Resolution Criteria
Template is "configured" when:
- ME.md has real name, expertise, and at least one project
- GOALS.md has real target metric and deadline
- At least one set of credentials is configured (X or Bluesky)

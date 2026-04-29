# Example Research File
Date: 2026-04-29
Status: EXAMPLE — replace with real research once ME.md is configured

## Purpose
This file demonstrates the expected format for research files stored in `agent/memory/research/`.

Real research files are created each session by:
1. Web-searching for news in the owner's expertise pillars
2. Filtering stories to only those that connect to a pillar
3. Noting the "our angle" — what the owner's experience adds beyond reporting

## Example Format

| Story | Pillar | Our Angle | Source | Status |
|-------|--------|-----------|--------|--------|
| Example: OpenAI releases new model | AI/ML | "We built X with the previous model, here's what changes" | techcrunch.com | STAGED |
| Example: Startup raises $50M for AI infra | Infrastructure | "We faced this exact problem, here's how we solved it cheaper" | example.com | DRAFT |

## Notes
- Stories older than 72 hours lose relevance fast
- News is only a hook — pillar expertise is the real value
- Mark stories as STAGED once moved to `agent/outputs/`
- Delete this file once all stories are staged or stale

## Next Research Sessions
Once ME.md is configured with real expertise, research will focus on:
- [Pillar 1] news
- [Pillar 2] news
- Building-in-public milestones from the owner's actual projects

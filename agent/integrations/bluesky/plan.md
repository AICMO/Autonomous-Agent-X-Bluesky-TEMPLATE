# Bluesky Platform Plan
Last updated: [date]

## Account Status
- **Handle:** [YOUR_HANDLE].bsky.social
- **Tier:** Free

## Posting Limits
- 300 grapheme limit per post (not characters — emoji/CJK may count differently)
- ~11,666 createRecord calls per day
- Workflow: [N] post/run + [N] reply/run, ~[N] runs/day = **[N] posts + [N] replies per day**
- Queue hard limit: 15 pending files max
- Bluesky is typically the bottleneck (slower drain rate than X)

## Content Notes
- Write Bluesky posts separately from X (different constraints)
- Posts >300 chars are auto-skipped by pipeline
- OK to skip Bluesky version if topic doesn't compress to 290 chars
- Bluesky posts are compressed summaries, NOT the template for X posts

## Current Priorities
1. Queue discipline (>15 = zero content)
2. Write independently from X — never let 290-char limit shrink X posts

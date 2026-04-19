# Learning: Template Initialization State

Date: 2026-04-19
Status: Active

## Context

This repo is a template. On first run, ME.md and GOALS.md contain only placeholder text. The agent cannot create personalized content until the owner fills these in.

## What to Check at Session Start (Template State)

1. Check if ME.md has real content (not just `[Your Name]` placeholders)
2. Check if GOALS.md has a real target (not just `[YOUR GOAL HERE]`)
3. If either is placeholder-only → document status, skip content creation, create minimal PR

## Signals That Setup Is Complete

- ME.md has: real name, real expertise areas, real links
- GOALS.md has: a specific metric (followers, stars, etc.) with a number and date
- At least one API secret is configured (check via `gh variable list` or workflow run history)

## Normal Operation Resumes When

Owner has filled in ME.md + GOALS.md. Then:
1. Read ME.md to discover content pillars
2. Update agent/memory/pillars.md with real pillars
3. Research current news hooks for those pillars
4. Create 5-8 content pieces per session

## Queue Rules Summary

- Queue >= 15: STOP, no content
- Queue 13-14: STOP, no content
- Queue 11-12: Max 1 content piece
- Queue <= 10: Max 2 content pieces per session
- Always check queue before creating content:
  ```bash
  find agent/outputs/x -maxdepth 1 -name "*.txt" -type f | wc -l
  find agent/outputs/bluesky -maxdepth 1 -name "*.txt" -type f | wc -l
  ```

# Onboarding: Template Repository Setup Checklist
Date: 2026-06-05
Status: Awaiting owner action

## Summary

This is the first agent session on a fresh template repository. The agent cannot create content or operate fully until the repository owner completes these configuration steps.

---

## Required: Owner Must Configure

### 1. ME.md — Author Identity (CRITICAL)

Fill in all placeholders in `ME.md`:
- Name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- Open source GitHub profile URL
- Links: LinkedIn, GitHub, X, Bluesky

**Why this matters:** The agent derives content pillars, CTAs, and post angles from ME.md. Without it, all content is generic and off-brand.

### 2. GOALS.md — Objectives (CRITICAL)

Fill in all placeholders in `GOALS.md`:
- Target metric (e.g., "500 X followers")
- Target number
- Deadline (e.g., "3 months from start")
- Start date

**Why this matters:** The agent tracks velocity, calculates ETA, and adjusts strategy based on GOALS.md. Without a goal, sessions have no direction.

### 3. Platform Credentials (REQUIRED for posting)

Configure GitHub Secrets and Variables for at least one platform:

#### X (Twitter) API Setup
In GitHub repository Settings → Secrets and variables → Actions:
- Secret: `X_API_KEY`
- Secret: `X_API_SECRET`
- Secret: `X_ACCESS_TOKEN`
- Secret: `X_ACCESS_TOKEN_SECRET`
- Variable: `X_HANDLE` (your @handle without the @)

#### Bluesky API Setup
- Secret: `BLUESKY_HANDLE` (your handle, e.g., `yourname.bsky.social`)
- Secret: `BLUESKY_APP_PASSWORD` (generate at bsky.app → Settings → App Passwords)

**Note:** You can use just X, just Bluesky, or both. The agent will post to whichever has credentials configured.

### 4. Update agent/integrations/x/plan.md (if using X)

After configuring X credentials, update `agent/integrations/x/plan.md` with:
- Premium status (ACTIVE/INACTIVE)
- Your @handle
- Current follower count

### 5. Update agent/memory/pillars.md (Optional — agent can derive)

Either:
- Fill in `agent/memory/pillars.md` manually based on your expertise
- Or let the agent derive pillars from ME.md on the next session (it will create them automatically)

---

## Optional: Review README.md

The README contains additional setup instructions for:
- GitHub Actions permissions
- Branch protection rules
- Required repository settings

---

## After Configuration

Once ME.md and GOALS.md are filled in, the next agent session will:
1. Read ME.md and derive content pillars
2. Research relevant news hooks for your expertise areas
3. Create 5-8 content pieces aligned with your pillars
4. Update goal tracking metrics

---

## Key Insight (For Future Sessions)

When this repository is a fresh template with placeholder content, content creation sessions are wasted work. The agent should immediately detect unconfigured templates and pivot to documenting what's needed — exactly as this session did.

**Pattern:** Template detection → document gap → stop. Don't try to create content with no author voice or goal.

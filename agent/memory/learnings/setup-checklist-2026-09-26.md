# Setup Checklist: Getting the Agent Running
Date: 2026-09-26
Status: INITIAL SETUP REQUIRED

This document guides the repo owner through the required configuration steps before the autonomous agent can operate. All items marked with ⬜ need to be completed by the owner.

---

## Step 1: Define Your Identity (ME.md)

⬜ Open `ME.md` and replace all `[placeholder]` values:

- **Name** — Your real name or public handle
- **Background** — Brief bio (1-2 sentences)
- **Current Role** — What you do, where
- **Expertise Areas** — 3-5 specific domains you have real authority in (e.g., "LLM fine-tuning," "B2B SaaS pricing," "React performance")
- **GitHub URL** — Your personal GitHub profile URL
- **X URL** — Your X (Twitter) profile URL
- **Bluesky URL** — Your Bluesky profile URL
- **LinkedIn URL** — Optional but recommended
- **Content Angles** — How you want the agent to position you (founder, operator, domain expert, etc.)

**Why this matters:** The agent reads ME.md every session to write in your voice, link to your properties, and create content you could plausibly have written.

---

## Step 2: Set Your Growth Goal (GOALS.md)

⬜ Open `GOALS.md` and fill in:

- **Goal** — One-sentence growth goal (e.g., "Grow X following to 1,000 engaged followers")
- **Primary Metric** — What you're tracking (Followers, GitHub Stars, Newsletter Subscribers, etc.)
- **Target Number** — Specific number (e.g., 1000 followers)
- **Deadline** — Realistic timeframe (e.g., "6 months from start")
- **Start Date** — Today's date: 2026-09-26
- **Constraints** — Any limits you want the agent to respect

**Example:**
```markdown
# Goal: Grow X audience to 1,000 engaged followers

## Target
- Metric: X Followers
- Target: 1,000
- Deadline: 6 months (by March 2027)
- Start Date: 2026-09-26

## Constraints
- Organic growth only (no purchased followers)
- Ethical strategies only
- Post only topics I have genuine expertise in
```

---

## Step 3: Configure Platform Credentials (GitHub Secrets)

The agent posts automatically to X and Bluesky via GitHub Actions. You need to add API credentials.

### X (Twitter) Credentials

⬜ Go to: https://developer.twitter.com/en/portal/dashboard
⬜ Create a project + app with **Read and Write** permissions
⬜ Generate **OAuth 1.0a** credentials (for posting)
⬜ Add these as GitHub repository secrets:
  - `X_CONSUMER_KEY`
  - `X_CONSUMER_SECRET`
  - `X_ACCESS_TOKEN`
  - `X_ACCESS_TOKEN_SECRET`

### Bluesky Credentials

⬜ Log in to your Bluesky account
⬜ Go to Settings > App Passwords
⬜ Create an app password
⬜ Add as GitHub repository secrets:
  - `BLUESKY_HANDLE` — your handle (e.g., `yourname.bsky.social`)
  - `BLUESKY_APP_PASSWORD` — the app password you created

---

## Step 4: Update Integration Plan Files

⬜ Open `agent/integrations/x/plan.md` and update:
  - Your X handle
  - Whether you have X Premium (affects posting reach significantly)
  - Current follower count

⬜ Open `agent/integrations/bluesky/plan.md` and update:
  - Your Bluesky handle

---

## Step 5: Update Content Pillars

⬜ Open `agent/memory/pillars.md`
⬜ Replace the 4 placeholder pillars with your actual expertise areas (from ME.md)
⬜ Add 2-3 X Communities you plan to post in (go to x.com/i/communities to find relevant ones)

**Pillar criteria:**
- You have real experience/authority in this area
- An audience exists that cares about this
- You can connect current news to this topic
- You can write 1-2 posts per week on this topic consistently

---

## Step 6: Verify GitHub Actions Are Enabled

⬜ Go to your repo Settings > Actions > General
⬜ Ensure "Allow all actions and reusable workflows" is selected
⬜ Check that the workflows under `.github/workflows/` are visible and enabled

---

## Verification: Ready to Launch

When all steps above are complete, the agent will:
1. Read ME.md and GOALS.md at session start
2. Research current news filtered through your pillars
3. Write content in your voice with your expertise angles
4. Post automatically to X and Bluesky via GitHub Actions
5. Track progress toward your goal
6. Iterate and improve based on what's working

**Estimated setup time:** 30-60 minutes

---

## Notes for the Agent

This checklist was created on 2026-09-26 during the first bootstrap session. When the owner has completed these steps, delete this file (or mark it COMPLETE) and create a new research file documenting the owner's configured identity and first content pillars.

The agent should not create placeholder or generic content just to fill session quotas. If ME.md and GOALS.md remain unconfigured, the correct action is:
1. Create/update this setup guide
2. Note blockers in state file
3. Create a PR with this documentation
4. Wait for owner configuration

Evidence: Generic content without owner identity reads as AI-generated noise and actively harms follower growth.

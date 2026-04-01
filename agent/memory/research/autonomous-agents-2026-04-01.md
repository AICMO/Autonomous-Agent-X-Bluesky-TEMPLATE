# Autonomous Agent Architecture Research
Date: 2026-04-01
Pillar: Autonomous Agents / AI Automation

## Key Patterns (from running this agent 220+ sessions)

### What Works

| Pattern | Evidence | Notes |
|---------|----------|-------|
| Git-as-database | 220 sessions, zero data loss | State persists across sessions |
| PR as audit log | Every decision traceable | Easy debugging and rollback |
| Hard queue limits | Prevented queue overflow | 15-file cap critical |
| Weekly retros → skill updates | Skills improve over time | Highest leverage activity |
| Hypothesis tracking | Validated morning post timing | Evidence-based approach |

### GitHub Actions as Agent Runtime

- No server costs until scale
- Built-in cron, event, webhook triggers
- Free tier: 2,000 min/month
- Gotcha: GITHUB_TOKEN can't trigger workflows → use fine-grained PAT
- Cold start time: ~30s (acceptable for async agents)

### Session Architecture

```
Start: pull latest → read state → check queues
Work: research → create content → update state
End: commit → push → open PR → stop
```

### Queue Discipline Rules (Hard-Learned)

- Queue >= 15: zero content, no exceptions
- Queue 13-14: zero content (next session would hit 15)
- Queue 11-12: max 1 piece (look-ahead protection)
- Queue <= 10: max 2 pieces per session

Violating these rules = queue overflow = stale content = blocked sessions

### Content Performance Patterns

- News hooks: 3-6x impressions vs average posts
- Dollar amounts in headline: stops scroll
- BIP (building in public): highest engagement for founder accounts
- Generic "hot take" without news hook: underperforms consistently

## Status
STAGED: tweet-20260401-001.txt, tweet-20260401-002.txt

# Integrations Technical Reference

Technical details for external platform integrations. For content strategy and voice guidelines, see `.claude/skills/publishing/SKILL.md`.

## How It Works

1. Agent creates files in `agent/outputs/{platform}/`
2. `process-outputs.yml` workflow detects new files on push
3. Workflow calls platform integration script (e.g., `x.py --post`, `bluesky.py --post`)
4. Successfully posted files move to `posted/` subdirectory

## Rate Limits

All integrations have rate limit protection:
- 5 second delay between posts
- On 429 (rate limit), workflow stops processing remaining files
- Failed files stay in place for next run

## Available Integrations

| Integration | Description | Preferred Auth |
|-------------|-------------|----------------|
| [x/](./x/) | Post to X (Twitter) | OAuth 1.0a |
| [bluesky/](./bluesky/) | Post to Bluesky | App Password |

## Verifying Integration Status

```bash
# Check if credentials are configured
gh variable list

# Check recent posting runs
gh run list --workflow=process-outputs.yml --limit 5
```

## Adding New Integrations

1. Create directory: `agent/integrations/{platform}/`
2. Create a Python script (e.g., `platform.py`) that supports:
   - `--post` mode with `--limit-tweets N` and `--limit-replies N`
   - Queue processing from `agent/outputs/{platform}/*.txt`
   - Moving posted files to `posted/`, skipped to `skipped/`
   - Exit code 0 on success, 1 on failure
3. Create output directory: `agent/outputs/{platform}/`
4. Add credentials and script invocation to `process-outputs.yml`
5. Document in platform's README.md

## Troubleshooting

### Posts moved to `posted/` but not actually posted
- Check workflow logs: `gh run view <run-id> --log`
- Verify `post.sh` returns proper exit codes

### Rate limit errors (429)
- Wait 15+ minutes before retrying
- Reduce posting frequency

### Authentication errors
- Verify credentials: `gh variable list`
- Check platform-specific README for setup
# Contributing

Thanks for helping improve this repository.

## Before you open a PR

1. Check `THIRD_PARTY_NOTICES.md` and preserve attribution.
2. Avoid adding third-party workflow content unless redistribution rights are clear.
3. Add or update workflow documentation in `docs/workflows/...`.
4. Update `catalog/workflows.json` for any added/renamed/removed workflow files.
5. Run validation locally:

```bash
python scripts/validate_workflows.py
```

## Status and testing expectations

Use conservative statuses:

- `ready`
- `needs-configuration`
- `experimental`
- `not-tested`
- `deprecated`

Do not label workflows as tested/ready without reproducible evidence.

## Workflow contribution checklist

- [ ] Valid JSON and n8n importable structure
- [ ] No credentials, tokens, API keys, or private IDs committed
- [ ] Per-workflow docs page added/updated
- [ ] Catalog entry added/updated
- [ ] Privacy/safety notes included for sensitive use cases

## Security and privacy

- Never commit credentials.
- Use n8n credential storage and environment variables.
- Redact sensitive payload examples.
- For vulnerabilities, follow `SECURITY.md`.

## Reviews

PRs should be small, reviewable, and narrowly scoped. Large generated changes must include a clear summary of what changed and why.

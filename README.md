# n8n Free Templates (Community-Maintained)

A community-maintained collection of documented n8n workflow templates, with conservative status labels and setup guidance.

## Attribution and licensing context

This repository started by importing/adapting templates from [`wassupjay/n8n-free-templates`](https://github.com/wassupjay/n8n-free-templates).

- Upstream currently has **no declared GitHub license metadata**.
- Because of that, you must verify redistribution rights before reusing upstream-derived workflow JSON files.
- Attribution notices must be preserved in this repository and downstream copies.
- See [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) for details.

## Scope and positioning

This project is being improved toward production-oriented quality, but workflows are **not automatically production-ready**.

Initial focus areas:

1. **AI/ML** (`AI_ML/`)
2. **Agriculture** (`Agriculture/`)
3. **Business automation patterns** (cross-category automations in `Social_Media/`, `Media/`, `Education/`, and related folders)

Other categories remain available while documentation and validation coverage are expanded.

## Repository structure

- Workflow JSON files are grouped by category folders at repository root.
- Per-workflow documentation is in `docs/workflows/<category>/`.
- Machine-readable index is in `catalog/workflows.json`.
- Validation tooling is in `scripts/validate_workflows.py`.

## Workflow status labels

- `ready` - validated by maintainers in a documented environment
- `needs-configuration` - imports, but requires credential/config setup
- `experimental` - exploratory/incomplete behavior
- `not-tested` - no maintained import/run evidence
- `deprecated` - retained for reference/migration

Unless explicitly validated, statuses should remain conservative.

## Catalog by category

| Category | Workflow count | Focus | Folder README |
|---|---:|---|---|
| AI_ML | 10 | Primary | [AI_ML/README.md](AI_ML/README.md) |
| Agriculture | 10 | Primary | [Agriculture/README.md](Agriculture/README.md) |
| Creative_Content | 1 | Secondary | [Creative_Content/README.md](Creative_Content/README.md) |
| Education | 2 | Secondary | [Education/README.md](Education/README.md) |
| IoT | 10 | Secondary | [IoT/README.md](IoT/README.md) |
| Media | 10 | Secondary | [Media/README.md](Media/README.md) |
| Social_Media | 11 | Secondary | [Social_Media/README.md](Social_Media/README.md) |

Global catalog: [`catalog/workflows.json`](catalog/workflows.json)

## Import and configuration

1. Open n8n and import a workflow JSON file.
2. Review node parameters before first execution.
3. Configure credentials in n8n (never hard-code secrets in workflow JSON).
4. Validate third-party endpoints, index names, spreadsheet IDs, and channels.
5. Run with safe sample data first.

## Compatibility and testing policy

- Compatibility is documented as `1.x (verify in your environment)` unless a tested version is recorded.
- Do not mark a workflow as tested without import/run evidence.
- The validator checks structure, node IDs/positions, suspicious secret patterns, and doc/catalog coverage.

Run locally:

```bash
python scripts/validate_workflows.py
```

## Privacy and safety guidance

Workflows in this repository may send data to third-party services (for example AI models, vector DBs, sheets, messaging, and cloud APIs).

Before use:

- classify data and redact sensitive fields when possible
- verify provider logging, retention, training, and regional settings
- enforce least-privilege credentials and environment-level secret storage
- avoid sending unnecessary PII to external providers

Important safeguards:

- **Resume screening and customer-impacting decisions:** do not rely on AI output as sole decision authority.
- **Agriculture/IoT workflows:** add manual approvals and fail-safe controls before real-world actuation.
- **AI-generated content:** require human review before publication or policy-sensitive actions.

## Governance, contributions, and security

- Contribution guide: [`CONTRIBUTING.md`](CONTRIBUTING.md)
- Code of conduct: [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)
- Security policy: [`SECURITY.md`](SECURITY.md)
- Changelog: [`CHANGELOG.md`](CHANGELOG.md)
- Roadmap: [`ROADMAP.md`](ROADMAP.md)
- Documentation overview: [`docs/README.md`](docs/README.md)

## License scope

See [`LICENSE`](LICENSE). It is intentionally scoped to original repository documentation/scripts/metadata and does **not** claim rights over upstream-derived workflow JSON where licensing is uncertain.

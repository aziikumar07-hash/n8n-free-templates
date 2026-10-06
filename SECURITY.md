# Security Policy

## Supported security posture

This repository contains workflow templates and documentation. All workflows should be treated as requiring local review before production deployment.

## Reporting a vulnerability

Please open a private security advisory or contact maintainers privately with:

- affected file(s)
- reproducible steps
- impact assessment
- suggested mitigation

Do not publish exploit details before maintainers can respond.

## Credential and secret handling

- Never commit API keys, tokens, passwords, or private endpoint secrets.
- Use n8n credential manager and environment-level secret storage.
- Rotate any secret immediately if exposure is suspected.

## Data privacy and safety

Many templates can process PII or operational data.

- verify third-party provider privacy settings and retention
- minimize outbound data
- redact sensitive fields when possible
- keep audit logs for sensitive workflows

### High-risk use cases

- Resume screening/employment-related workflows must include human oversight.
- Customer-impacting decisions must not rely only on AI output.
- Agriculture/IoT control workflows require manual approvals and fail-safe controls.

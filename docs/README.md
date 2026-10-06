# Documentation Overview

This directory contains generated and maintained workflow documentation for this repository.

## Structure

- `docs/workflows/<category>/<workflow>.md`: one page per workflow JSON file.
- `catalog/workflows.json`: machine-readable inventory with status, providers, attribution, and doc links.

## Status model

- `ready`: maintainers have validated setup and execution in a documented environment.
- `needs-configuration`: workflow imports but requires credentials/config before use.
- `experimental`: workflow logic is incomplete or intentionally exploratory.
- `not-tested`: no maintained test/import evidence.
- `deprecated`: kept for reference; migration recommended.

This repository uses conservative defaults (`needs-configuration`) unless there is explicit validation evidence.

## Discussions

GitHub Discussions cannot be enabled from repository files. A maintainer can enable Discussions manually:

1. Open repository **Settings**.
2. Scroll to **Features**.
3. Enable **Discussions**.
4. Add a pinned welcome post with support expectations.

## Privacy and safety baseline

Before running any workflow, review the privacy/safety guidance in the root README and `SECURITY.md`, then verify all third-party provider settings in your own environment.

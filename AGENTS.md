# AGENTS.md

## Repository map

- `pyproject.toml`: package identity, Python floor, test extra and Hatch/VCS version source.
- `src/replace_me/`: passive library starter; rename it deliberately when adopting.
- `tests/`: pytest tests.
- `.github/workflows/ci.yml`: pinned shared Python CI caller.

## Development and validation

Read [CONTRIBUTING.md](CONTRIBUTING.md) for the required setup, exact local
commands and evidence requirements. Use the documented Python environment and run pytest with coverage; preserve the separate hosted coverage gate.
`hatch-vcs` derives the package version from release tags. Do not add a second static source version or commit the generated `_version.py`.

## Operating model

This repository is maintained by one developer. Automated review, tests and
security gates replace mandatory human approvals. Do not add CODEOWNERS approval
requirements, team assignments or a second-maintainer dependency. Use a focused
branch and reviewable pull request; preserve unrelated and unmerged work.

## Boundaries

Never commit credentials or sensitive data. Keep generated files reproducible.
Prefer one authoritative configuration and link to it from tool-specific files.
Preserve existing release, data, credential and privacy gates. An unavailable
check is not a pass, and a configured provider is not evidence of its execution.

Use [BOOTSTRAP.md](BOOTSTRAP.md) for adoption decisions. Keep the applicability
declarations in `.github/community-bootstrap.json` aligned with actual project
configuration; they do not substitute for observed GitHub settings.

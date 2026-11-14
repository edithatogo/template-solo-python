# Solo-maintainer Python project template

[![CI](../../actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Citation](https://img.shields.io/badge/citation-CFF-blue.svg)](CITATION.cff)

A Python 3.14 project baseline with reusable CI, real coverage, Renovate, and tag-derived package versions.

## Status

This repository is designed for one maintainer. Automated checks are required;
no second reviewer, CODEOWNERS approval, team membership, or mandatory human
approval is introduced.

## Usage

Choose **Use this template** to create a Python project, then follow the
[adoption checklist](BOOTSTRAP.md). The initial package is a placeholder module
with a smoke test; implement the project's API and regression tests before
publishing it.

1. Replace `replace-me` in `pyproject.toml` and rename `src/replace_me/`.
2. Follow [CONTRIBUTING.md](CONTRIBUTING.md) to select the CI-matching Python and
   create an isolated environment.
3. Install the test extra with `python -m pip install -e ".[test]"` in that
   environment.
4. Run `python -m pytest --cov --cov-report=xml` and inspect the test and
   coverage results.

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for setup and validation commands, and
[BOOTSTRAP.md](BOOTSTRAP.md) for the adoption checklist.

The pinned shared CI installs the test extra and runs pytest with coverage. It
is configured to upload that output through Codecov OIDC. Verify provider
activation and an actual upload in each generated repository.

## Versioning

The package version is derived from Git tags by `hatch-vcs`. Release tags are the authority; do not duplicate a static version in source or citation metadata.

## Logging

This starts as a passive library, so it does not configure global logging. Applications built from it should use the standard logging facade and configure structured handlers at the application boundary.

## Security

Follow [SECURITY.md](SECURITY.md) for private reporting and the safe contact
fallback if GitHub's **Report a vulnerability** option is unavailable. Do not
include credentials, sensitive source data or exploit details in public issues.

## Citation

See [CITATION.cff](CITATION.cff). Release-specific versions and identifiers are
added only when the release exists.

## License

Repository-authored starter material is MIT licensed; see [LICENSE](LICENSE).
Record third-party and source-data rights separately.

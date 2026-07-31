# Solo-maintainer Python project template

[![CI](../../actions/workflows/ci.yml/badge.svg)](../../actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Citation](https://img.shields.io/badge/citation-CFF-blue.svg)](CITATION.cff)

A Python 3.14 project baseline with reusable CI, real coverage, Renovate, and tag-derived package versions.

## Status

This repository is designed for one maintainer. Automated checks are required;
no second reviewer, CODEOWNERS approval, team membership, or mandatory human
approval is introduced.

## Start here

1. Replace `replace-me` and `src/replace_me` with the package identity.
2. Run `python -m pip install -e ".[test]"`.
3. Run `python -m pytest --cov`.

## Development

CI installs the test extra, runs pytest with coverage, and uploads real coverage through Codecov OIDC.

## Versioning

The package version is derived from Git tags by `hatch-vcs`. Release tags are the authority; do not duplicate a static version in source or citation metadata.

## Logging

This starts as a passive library, so it does not configure global logging. Applications built from it should use the standard logging facade and configure structured handlers at the application boundary.

## Security

Report vulnerabilities privately through GitHub Security Advisories. See
[SECURITY.md](SECURITY.md); do not disclose credentials or sensitive source data
in a public issue.

## Citation

See [CITATION.cff](CITATION.cff). Release-specific versions and identifiers are
added only when the release exists.

## License

Repository-authored starter material is MIT licensed; see [LICENSE](LICENSE).
Record third-party and source-data rights separately.
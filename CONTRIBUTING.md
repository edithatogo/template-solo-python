# Contributing

## Development

Use Python 3.15.2 to reproduce the current pinned CI. The package manifest allows Python 3.14 or newer; a compatible interpreter alone is not evidence of CI parity. Create an isolated environment from the repository root:

```sh
python3.15 -m venv .venv
.venv/bin/python -m pip install -e ".[test]"
```

On Windows, use `.venv\Scripts\python.exe` for the environment's Python commands.

Use four-space Python indentation. Keep library imports free of application-wide logging configuration. Add regression tests for changed behaviour and keep examples runnable.

See [BOOTSTRAP.md](BOOTSTRAP.md) when creating a new project from this starter.

## Validation

```sh
.venv/bin/python -m pytest --cov --cov-report=xml
```

This runs the test extra declared in `pyproject.toml` and creates real coverage output. CI additionally uploads coverage through Codecov OIDC. Report upload/provider status separately from test success.

Record the command, tool versions and outcome in the pull request. Distinguish
passed, failed, skipped and unavailable checks; include a hosted run link when
available. Required automated checks must pass before integration.

## Pull requests

Use a focused branch such as `fix/short-summary`, `feat/short-summary` or
`docs/short-summary`. Explain the problem and resulting behaviour, link related
issues, and include the validation evidence. Keep commits reviewable and update
affected documentation, examples and tests with the change. Identify any
compatibility, generated-output, release or data impact.

The repository has one maintainer. Automated review and required checks replace
mandatory human approval; do not add a second-reviewer, team or CODEOWNERS gate.
Preserve unrelated work and existing security/publication requirements.

## Security and support

Use the repository's issue chooser for reproducible bugs or scoped proposals.
For usage questions, include a minimal safe example and what you have already
tried. Follow [SECURITY.md](SECURITY.md) for vulnerabilities; do not put private
data, credentials or sensitive exploit details in public issues or logs.

Follow the account's
[code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md).
When adopting this template under a different owner, replace this link with the
new project's policy and verify its support and private-reporting routes.

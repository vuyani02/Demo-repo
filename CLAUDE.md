# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a lightweight Python demo project used to showcase common repository documentation and quality signals. All content is intentionally minimal and safe to replace in a real project.

## Commands

### Install dependencies
```bash
pip install -r requirements.txt
```

### Run tests
```bash
pytest tests/
# Run a single test file
pytest tests/test_example.py
# Run a single test by name
pytest tests/test_example.py::test_placeholder
```

### Lint and format
```bash
ruff check .          # lint
ruff check . --fix    # auto-fix lint issues
ruff format .         # format code
```

### Docker
```bash
docker build -t demo-repo .
docker compose up
```

## Architecture

The project is structured as a flat Python package with a `tests/` directory for tests and `.github/` for CI/CD workflows and templates. There is no application runtime yet — the current codebase is documentation and infrastructure scaffolding only.

- CI runs on GitHub Actions (`.github/workflows/ci.yml`) and uploads coverage to Codecov.
- Linting and formatting are handled by Ruff (`pyproject.toml`).
- Dependencies are pinned in `requirements.txt`; Dependabot keeps them updated via `.github/dependabot.yml`.

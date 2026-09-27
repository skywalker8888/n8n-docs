# CLAUDE.md — n8n Docs

## Project Overview
This repo hosts the [n8n](https://n8n.io/) documentation site, built with MkDocs using the Material for MkDocs theme. The live site is at [docs.n8n.io](https://docs.n8n.io/).

## Key Commands

```bash
# Install dependencies (use a virtual environment)
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Install the Material theme (external contributors use free version)
pip install mkdocs-material
# n8n org members with Insiders access:
# pip install _submodules/insiders

# Serve a local preview
mkdocs serve --strict

# Faster local preview (only rebuilds changed files after first build)
mkdocs serve --strict --dirty

# Skip trending-workflow data fetch (speeds up builds)
export NO_TEMPLATE=true && mkdocs serve --strict

# Lint check
# (see .github/workflows/lint.yml for exact command)
```

## Repository Structure

| Path | Purpose |
|------|---------|
| `docs/` | All documentation source files (Markdown) |
| `mkdocs.yml` | Site configuration |
| `nav.yml` | Navigation structure |
| `_snippets/` | Reusable content snippets |
| `_submodules/` | Git submodules (Insiders theme) |
| `document-templates/` | Templates for new doc pages |
| `styles/` | Custom CSS |
| `.vale.ini` | Vale prose linter config |

## Writing Conventions
- Follow the [n8n style guide](https://github.com/n8n-io/n8n-docs/wiki/Styles)
- Do not replace tabs with spaces in code samples (`.editorconfig` enforced)
- Do not add features that require the Insiders theme without a fallback
- Run `mkdocs serve --strict` locally — treat warnings as errors
- Update `nav.yml` when adding new pages

## CI
GitHub Actions runs lint and link checks on every PR. All checks must pass before merging.

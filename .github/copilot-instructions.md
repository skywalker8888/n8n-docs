# GitHub Copilot Instructions

## Project: n8n Docs

This is a **documentation site** for n8n, built with MkDocs + Material theme. All content is Markdown.

### Key Points
- Source files live in `docs/` — Markdown only
- Site config is `mkdocs.yml`; navigation is in `nav.yml`
- Reusable snippets go in `_snippets/`
- Do not modify `_submodules/` (Git submodule — Insiders theme)
- Code samples must preserve tabs (not spaces) per `.editorconfig`
- Run `mkdocs serve --strict` to validate before opening a PR
- Follow the n8n style guide for terminology and tone

### When editing docs
- Keep language clear, concise, and task-oriented
- Use the templates in `document-templates/` for new pages
- Update `nav.yml` if you add or rename pages
- Do not add Insiders-only features without checking availability in the free theme

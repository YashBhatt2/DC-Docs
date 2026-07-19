---
name: build-docs
description: Build the MkDocs site and open the result in the browser. Use when the user asks to build, preview, or check the docs site locally.
---

Run the project's actual build/preview workflow:

1. Run `mkdocs build` from the repo root (requires the `mkdocs` and `mkdocs-material` packages from `requirements.txt` — activate `venv/` first if it exists and isn't already active). `mkdocs.yml` sets `docs_dir: docs_md` and `site_dir: docs`, so this reads the real markdown source and writes straight into `docs/`, which is the committed deploy artifact served as-is by Cloudflare Pages.
2. Open the root `index.html` (the hand-built landing page, not MkDocs' own output) in the default browser, e.g. `open index.html` on macOS.
3. Report any MkDocs build warnings/errors verbatim rather than silently swallowing them.
4. `docs/` will show as modified in git after this — that's expected (it's the deploy output), not a mistake to undo.

# poe

A collection of poems by [@dvojitywendy](https://github.com/dvojitywendy).

**Live site:** https://dvojitywendy.github.io/poe/

## Structure

- `docs/` — published to GitHub Pages
  - `index.html` — single-file viewer (no build step, no dependencies)
  - `NNN.md` — one poem per file, numbered sequentially

## Adding a poem

Drop a new `.md` file in `docs/` using the next number in sequence (e.g. `093.md`). The viewer auto-discovers it on next load — no code changes needed.

Each file follows this format:

```
/**
* Copyright 2007-2025 @dvojitywendy
*/

Title goes here

Body of the poem
across multiple lines
```

## Local preview

`fetch()` doesn't work from `file://` URLs, so serve `docs/` over HTTP:

```sh
cd docs && python -m http.server 8000
```

Then open http://localhost:8000/.

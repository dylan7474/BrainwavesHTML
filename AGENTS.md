# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project Overview

BrainwavesHTML is a static, browser-only isochronic tone generator. The application is implemented in `index.html` with inline CSS and JavaScript, uses the Web Audio API for sound generation, and loads Tailwind CSS and Lucide icons from CDNs.

## Working Guidelines

- Keep the app dependency-light and easy to run as a static site.
- Do not add a build system unless the task explicitly requires one.
- Prefer small, readable changes over broad rewrites.
- Preserve the single-file app structure unless there is a clear reason to split files.
- Never put `try`/`catch` blocks around imports.
- Be careful with audio changes: test start, stop, live slider updates, preset buttons, noise controls, and timer behavior after modifying playback logic.

## Validation

For documentation-only changes, at minimum run:

```bash
git diff --check
```

For application changes, also open the app in a browser or serve it locally:

```bash
python3 -m http.server 8000
```

Then manually verify the main controls in the UI.

## Pull Request Notes

In PR summaries, mention whether changes are documentation-only or affect runtime behavior. Include the exact commands used for validation.

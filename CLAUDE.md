# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static personal portfolio site for Sai Kiran Shekolla, deployed automatically via GitHub Pages from the `main` branch at `shekolla.github.io`. No build step, no package manager, no framework.

## Structure

The entire site is a single file: `index.html`. All CSS lives inline in a `<style>` block in `<head>`. There are no external stylesheets, scripts, or dependencies.

## Previewing Changes

Open `index.html` directly in a browser — no server needed. To test locally via a server:

```bash
python3 -m http.server 8080
```

## Design System

Theming is done with CSS custom properties in `:root`. Dark mode is the default; light mode is applied via `@media (prefers-color-scheme: light)`.

| Variable    | Role              |
|-------------|-------------------|
| `--bg`      | Page background   |
| `--fg`      | Body text         |
| `--muted`   | Secondary text    |
| `--accent`  | Links / highlights|
| `--card`    | Card backgrounds  |
| `--border`  | Borders / dividers|

`.chip` elements are used for skill/tech tags; `.meta` is for dates and subtitles.

## Commit Style

Follow the project's `[Tag] message` convention visible in git log:

```
[Website] Update job title and project descriptions
[Website] Revise ETL pipeline description
```

Use the `shekolla-commit` or `shekolla-commit-push` skills when committing.

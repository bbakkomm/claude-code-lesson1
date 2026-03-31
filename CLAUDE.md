# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page frontend developer portfolio for "YulBuff" — a static HTML page with no build system or package manager.

## Stack

- **HTML**: Single file (`index.html`), written in Korean
- **CSS**: Inline `<style>` block inside `index.html` using custom utility classes (`.page`, `.section-title`, `.table-row`, `.divider`, etc.)
- **Tailwind CSS**: Loaded via CDN (`https://cdn.tailwindcss.com`) — no local installation
- **Font**: Noto Sans KR via Google Fonts

`tailwind.config.js` exists but is currently empty — Tailwind is used purely through CDN without custom configuration.

## Running the Project

Open `index.html` directly in a browser — no build step or server required. For live-reload during development, use any static file server (e.g., VS Code Live Server extension).

## Page Structure

All content lives in `index.html` inside `.page` (max-width 860px, centered). Sections follow this pattern:

```
<section>
  <div class="section-title">Label</div>
  <div class="table-row">
    <div class="table-label">Key</div>
    <div class="table-value">Value</div>
  </div>
</section>
```

Current sections: **Intro → Skills → Projects (3) → Contact**

## Styling Conventions

- Custom classes are defined in the inline `<style>` block, not in external CSS files
- Layout uses CSS Grid (`.table-row`: `grid-template-columns: 1fr 1fr`)
- Color palette: text `#111111`, muted `#555555`, divider `#d0d0d0`, section labels `#aaaaaa`
- Section spacing: `margin-bottom: 80px` on each `<section>`

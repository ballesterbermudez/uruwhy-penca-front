# Project Guidelines

## Code Style
- Use Astro components (`.astro`) with frontmatter at the top for imports and page/component logic.
- Keep page routes under `src/pages/`, shared UI under `src/components/`, and reusable wrappers under `src/layouts/`.
- Prefer scoped component styles in local `<style>` blocks unless a task clearly requires global styling.
- Follow existing naming in this repo: PascalCase component files (for example, `Welcome.astro`, `Layout.astro`).

## Architecture
- This repository is a single Astro app based on the Astro basics template.
- `src/pages/index.astro` composes the page from `src/layouts/Layout.astro` and `src/components/Welcome.astro`.
- `src/layouts/Layout.astro` owns document-level structure (`<html>`, `<head>`, metadata, favicon links) and renders content through `<slot />`.
- `public/` stores files served directly at the site root.
- `src/assets/` stores assets imported into Astro components.

## Build And Test
- Install dependencies: `npm install`
- Start local development: `npm run dev`
- Build production output: `npm run build`
- Preview production build: `npm run preview`
- Run Astro CLI subcommands: `npm run astro -- <command>`
- Environment requirement: Node.js `>=22.12.0` (from `package.json`)

## Conventions
- Keep instructions concise in code changes and avoid adding project-wide complexity unless requested.
- Respect strict TypeScript configuration inherited from `astro/tsconfigs/strict` in `tsconfig.json`.
- When changing conventions or project structure, update this file and link relevant docs.
- Link, do not duplicate: for starter usage details and command descriptions, see `README.md`.

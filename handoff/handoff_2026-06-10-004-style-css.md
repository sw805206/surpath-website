# handoff.md

Running balance of the full current state of `main`. Always reflects the latest
merged state, not just the most recent PR. Last updated 2026-06-10.

## Project
surpath-website — marketing website for Surpath (SP), a 3PL logistics company
specializing in e-Commerce fulfillment. Deploys via Cloudflare Pages watching
`main` (merge auto-triggers deployment; no separate publish step).

## Current state of `main`
First page is live in the repo. The Home page (`webpage/home.html`) is built to
the v2 style.md system, and all its CSS now lives in a single shared stylesheet
`style/style.css` (no styles are embedded in the HTML). style.md remains the
documented source of truth for design values.

### Process docs
- `process/claude.md` — universal rules (uploaded by user; `claude_2026-06-10-001`)
- `process/process.md` — project-specific process rules. Covers deployment, the
  manual style-consistency review, and the new **Shared Stylesheet** rule: all
  pages must link `style/style.css`; never embed styles in individual HTML files;
  new patterns go into style.css and are documented in style.md before building.
- `process/process_2026-06-10-001.md` — archived copy of process.md at the shared
  stylesheet update.

### Project docs
- `scope/scope.md` — project scope: services, network, differentiators, v1 pages,
  primary CTA ("Request a Free Consultation"), tone, out-of-scope items
- `style/style.md` — v2 homepage design system. Full component values (nav
  padding, stats bar columns/dividers, card grid, service lifecycle flow, spec
  bar, CTA band, footer padding), locked nav active/hover states (lime underline,
  2px thickness, 4px offset), mobile nav (≤768px hamburger), a full-width Layout
  section, and stats/footnote typography. A few items remain [PLACEHOLDER]:
  Avenir font (to confirm against the original logo source file), button hover
  states, and imagery direction.
- `style/style_2026-06-10-001.md` — archived copy of style.md at the homepage lock.
- `style/style_2026-06-10-002.md` — archived copy of style.md at the v2 update.

### Site code
- `webpage/home.html` — Home page. Nav (logo mark + wordmark, hamburger on
  mobile), hero, stats bar, "Why Surpath" cards, service lifecycle flow, spec
  bar, CTA band, footer. Loads the Tabler icon webfont (CDN) and
  `../style/style.css`. Inline `<script>` handles the mobile menu toggle.
- `style/style.css` — single shared stylesheet for all pages. Color values are
  defined as `:root` CSS custom properties (`--color-primary`, `--color-lime`,
  `--color-mid-teal`, `--color-nav-bg`, etc.) matching style.md; rules are grouped
  into commented sections (Reset & Base, Typography, Navigation, Hero, Stats Bar,
  Cards, Service Lifecycle, Spec Bar, CTA Band, Footer, Utilities, Mobile ≤768px).

### Assets
- `asset/surpath-logo-full.png` — full wordmark logo (3000×684, transparent)
- `asset/surpath-favicon.png` — square favicon icon (110×111, transparent)

### Scaffolded but empty folders
`blog/`, `tool/`.

## Milestones
- PR #1 "Initial md files and assets" — merged. Adds process.md, scope.md,
  style.md, and the two logo assets. Tagged `initial-files`.
- PR #2 "Add handoff.md and dated copy" — merged. Adds the first handoff.md and
  its dated copy. Tagged `initial-files`.
- PR #3 "Update style.md — homepage design" — merged. Replaces the TBD-heavy
  placeholder style.md with locked homepage design decisions; adds archived copy
  `style/style_2026-06-10-001.md`. Tagged `initial-style`.
- PR #5 "Update style.md — component values, nav states, layout" — merged.
  Replaces style.md with the v2 design system (expanded component values, locked
  nav active/hover states, full-width layout rule); adds archived copy
  `style/style_2026-06-10-002.md`. Tagged `style-v2`.
- PR #7 "Chore: extract shared stylesheet" — merged. Extracts all embedded CSS
  from home.html into `style/style.css` (colors as `:root` variables); links the
  stylesheet from home.html; adds the Shared Stylesheet rule to process.md plus
  archived copy `process/process_2026-06-10-001.md`. Tagged `style-css`.

## Open items / TBD
- `style/style.md`: button hover states [PLACEHOLDER]; imagery direction
  [PLACEHOLDER] (Tabler outline icons used as the v1 placeholder). Nav
  active/hover states are locked.
- Primary font (Avenir) to be confirmed against the original logo source file.
- VAS page: details TBD (to be added when the VAS page is built).
- Technology / integrations page: placeholder only in v1, details TBD.

## Out of scope (v1)
- No blog at launch.
- No Chinese-language version at launch (to be revisited).

## Next likely steps
- Build the remaining v1 pages against the v2 style.md system and the shared
  `style/style.css`: Services, Network/Locations, Technology (placeholder),
  About, Contact. Each page links `style/style.css` — no embedded styles.

## Process reminders
- Follow `process/claude.md` first, then `process/process.md`. If they conflict
  or a required file is missing, stop and ask.
- Code always works on a branch; never commits to `main`. Code never merges —
  the user reviews (browser preview / GitHub PR) and merges manually.
- All pages link the single shared stylesheet `style/style.css`; never embed
  styles in individual HTML files.
- When claude.md/scope.md/style.md/process.md/architecture.md change, create a
  dated archived copy alongside the live file.

# handoff.md

Running balance of the full current state of `main`. Always reflects the latest
merged state, not just the most recent PR. Last updated 2026-06-10.

## Project
surpath-website — marketing website for Surpath (SP), a 3PL logistics company
specializing in e-Commerce fulfillment. Deploys via Cloudflare Pages watching
`main` (merge auto-triggers deployment; no separate publish step).

## Current state of `main`
Repo is in initial setup. No site code or pages built yet — documentation and
brand assets only. style.md now holds the v2 homepage design system: the locked
decisions plus expanded component values, locked nav active/hover states, and a
full-width layout rule.

### Process docs
- `process/claude.md` — universal rules (uploaded by user; `claude_2026-06-10-001`)
- `process/process.md` — project-specific process rules (deployment, style review)

### Project docs
- `scope/scope.md` — project scope: services, network, differentiators, v1 pages,
  primary CTA ("Request a Free Consultation"), tone, out-of-scope items
- `style/style.md` — v2 homepage design system. Adds full component values (nav
  padding, stats bar columns/dividers, card grid, service lifecycle flow, spec
  bar, CTA band, footer padding), locked nav active/hover states (lime underline,
  2px thickness, 4px offset), mobile nav (≤768px hamburger), a new full-width
  Layout section, and stats/footnote typography. A few items remain [PLACEHOLDER]:
  Avenir font (to confirm against the original logo source file), button hover
  states, and imagery direction.
- `style/style_2026-06-10-001.md` — archived copy of style.md at the homepage lock.
- `style/style_2026-06-10-002.md` — archived copy of style.md at the v2 update.

### Assets
- `asset/surpath-logo-full.png` — full wordmark logo (3000×684, transparent)
- `asset/surpath-favicon.png` — square favicon icon (110×111, transparent)

### Scaffolded but empty folders
`blog/`, `tool/`, `webpage/`.

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

## Open items / TBD
- `style/style.md`: button hover states [PLACEHOLDER]; imagery direction
  [PLACEHOLDER] (Tabler outline icons used as the v1 placeholder). Nav
  active/hover states are now locked.
- Primary font (Avenir) to be confirmed against the original logo source file.
- VAS page: details TBD (to be added when the VAS page is built).
- Technology / integrations page: placeholder only in v1, details TBD.

## Out of scope (v1)
- No blog at launch.
- No Chinese-language version at launch (to be revisited).

## Next likely steps
- Begin building v1 pages, starting with Home, using the v2 style.md system:
  Home, Services, Network/Locations, Technology (placeholder), About, Contact.

## Process reminders
- Follow `process/claude.md` first, then `process/process.md`. If they conflict
  or a required file is missing, stop and ask.
- Code always works on a branch; never commits to `main`. Code never merges —
  the user reviews (browser preview / GitHub PR) and merges manually.
- When claude.md/scope.md/style.md/process.md/architecture.md change, create a
  dated archived copy alongside the live file.

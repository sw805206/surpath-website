# handoff.md

Running balance of the full current state of `main`. Always reflects the latest
merged state, not just the most recent PR. Last updated 2026-06-10.

## Project
surpath-website — marketing website for Surpath (SP), a 3PL logistics company
specializing in e-Commerce fulfillment. Deploys via Cloudflare Pages watching
`main` (merge auto-triggers deployment; no separate publish step).

## Current state of `main`
Repo is in initial setup. No site code or pages built yet — documentation and
brand assets only.

### Process docs
- `process/claude.md` — universal rules (uploaded by user; `claude_2026-06-10-001`)
- `process/process.md` — project-specific process rules (deployment, style review)

### Project docs
- `scope/scope.md` — project scope: services, network, differentiators, v1 pages,
  primary CTA ("Request a Free Consultation"), tone, out-of-scope items
- `style/style.md` — brand colors, typography, style direction; many items marked
  TBD pending the VI mock review

### Assets
- `asset/surpath-logo-full.png` — full wordmark logo (3000×684, transparent)
- `asset/surpath-favicon.png` — square favicon icon (110×111, transparent)

### Scaffolded but empty folders
`blog/`, `tool/`, `webpage/`, `handoff/` (now holds this handoff).

## Milestones
- PR #1 "Initial md files and assets" — merged. Adds process.md, scope.md,
  style.md, and the two logo assets. Tagged `initial-files`.

## Open items / TBD
- `style/style.md`: accent color, typography scale/weights/hierarchy, button/nav
  style, layout density, imagery direction — all TBD pending the VI mock review.
  When resolved, update style.md and archive a dated copy per the archiving rule
  in claude.md.
- Brand colors are estimates, to be confirmed after the VI mock.
- Primary font (Avenir) to be confirmed against the original logo source file.
- VAS page: details TBD (to be added when the VAS page is built).
- Technology / integrations page: placeholder only in v1, details TBD.

## Out of scope (v1)
- No blog at launch.
- No Chinese-language version at launch (to be revisited).

## Next likely steps
- VI mock review session to lock down style.md TBDs.
- Begin building v1 pages: Home, Services, Network/Locations, Technology
  (placeholder), About, Contact.

## Process reminders
- Follow `process/claude.md` first, then `process/process.md`. If they conflict
  or a required file is missing, stop and ask.
- Code always works on a branch; never commits to `main`. Code never merges —
  the user reviews (browser preview / GitHub PR) and merges manually.
- When claude.md/scope.md/style.md/process.md/architecture.md change, create a
  dated archived copy alongside the live file.

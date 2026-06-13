# handoff.md

Running balance of the full current state of `main`. Always reflects the latest
merged state, not just the most recent PR. Last updated 2026-06-13.

> Note: this update is written **anticipating the merge of PR #33**
> (`chore/style-consistency-pass` → `main`). PR #33 is OPEN and mergeable at time
> of writing; once merged it brings `main` to the state described here. The prior
> merged tip was `62254fc` (PR #32).

## Project
surpath-website — marketing website for Surpath (SP), a 3PL logistics company
specializing in e-Commerce fulfillment. Deploys via Cloudflare Pages watching
`main` (merge auto-triggers deployment; no separate publish step). Pages are
served from the repo root (Build output directory empty); paths are root-relative.

## Current state of `main`
Four pages are live, all built to the v2 style system and linking the single
shared stylesheet `style/style.css` (no styles embedded in any HTML file):

- **index.html** — Home. Nav, hero (slogan → H1 → body → CTA row), stats bar +
  full-bleed stats footnote, "Why Surpath" 2-column lime-bullet layout, services
  overview (4-up image cards with flow arrows), hidden placeholder clients
  section, CTA band, footer.
- **services.html** — Services. Hero (slogan → H1 → body, no CTA), interactive
  **Leaflet + Stadia dark-tiles** network map with HQ/Office/Warehouse markers and
  a legend, "Supply chain design" section whose right column is a **live iframe
  preview** of whitepaper-sample.html (scaled, click-through), core-services
  header bar, four alternating service blocks (#freight/#warehouse/#parcel/
  #assembly), multi-button CTA band, footer.
- **contact.html** — Contact. Hero (eyebrow → H1 → body — the documented
  eyebrow/no-slogan exception). Zone 1 (your details + team photo + trust card),
  Zone 2 (topic selector → dynamic per-topic question blocks → shared product
  fields → contact-preference dark band), full-width submit button. Vanilla-JS
  validation + visibility engine; submits to **placeholder** webhook/email
  endpoints (`PLACEHOLDER_APPS_SCRIPT_URL` / `PLACEHOLDER_EMAIL_ENDPOINT`) and
  swaps Zone 2 for a success message.
- **whitepaper-sample.html** — Standalone document-style sample (not in main nav),
  linked from the Services iframe preview. Line-numbered, selectively blurred
  proposal with cost tables and an inline data-flow SVG. Uses literal document
  palette, self-contained under `/* Whitepaper Sample Page */` in style.css.

Shared chrome across the three main pages: nav with logo mark (inline SVG "S") +
"surpath." wordmark, links Home / Services / **Partners (hidden, `display:none`
pending partners.html)** / Contact, and a "Get started" CTA; hamburger menu on
≤768px; footer "© 2026 Surpath Inc." (whitepaper page uses a wordmark-only nav and
its own "Contact us" CTA).

### What PR #33 (style consistency pass) changed
- **Width**: all inner wrappers (`.nav-inner`, `.hero-inner`, `.stats-inner`,
  `.container`, `.stats-footnote-inner`, `.cta-band-inner`, `.footer-inner`)
  capped at **980px** (was 1280px); `.wp-doc` stays 720px. Added `max-width: 980px`
  to `.hero h1`.
- **Hero**: standard order slogan → H1 → body (no eyebrow); CTA row only where a
  page already had one (home). Contact keeps the eyebrow / no-slogan exception.
- **Highlight classes**: `.highlight-h1` (lime #A8D44F) and `.highlight-body`
  (teal #4A9E8E) replace the former single `.highlight-keyword`; documented in
  style.md. Application is per-page by design (not yet applied in markup).
- **Color utilities**: `.text-on-dark` (#c8dde3) and `.link-teal` (#4A9E8E)
  replace all inline `style="color:…"` hardcodes (home stats footnote; the two
  Services "Alpha Grid" links).
- **Contact CSS migration**: the page's embedded `<style>` block moved into
  style.css under `/* Contact page */`; patterns documented in style.md.
- **Submit button**: now shared `.btn .btn-lime .btn-block` (full-width via the new
  `.btn-block` modifier) instead of a standalone `.submit-btn`.
- **Footer year**: © 2025 → © 2026 on all pages.
- **style.md**: Map Section rewritten to document the Leaflet implementation; the
  iframe-peek section and Contact Page section both documented; `.btn-block` added
  under Buttons.

### Process docs
- `process/claude.md` — universal rules (`claude_2026-06-10-001`): session read
  order, branch-per-task (Code never commits to `main`, never merges), stop-and-ask
  on ambiguity/conflict, file/folder discipline, handoff + archiving rules, UAT.
- `process/process.md` — project rules: Cloudflare deploy, root folder structure
  and root-relative paths, the manual style-consistency review, and the Shared
  Stylesheet rule (all pages link `style/style.css`; never embed styles; new
  patterns go to style.css + documented in style.md before building).
- `scope/scope.md` — services, specializations, network, target customers,
  differentiators, v1 page list, primary CTA, tone, out-of-scope.
- `style/style.md` — the v2 design system + per-component values, now including the
  980px width system, hero rules, keyword-highlight + color-utility classes,
  Leaflet map, Contact page patterns, iframe document preview, `.btn-block`, and
  the Whitepaper Sample page.

### Code & assets
- `style/style.css` — single shared stylesheet; colors as `:root` custom
  properties; sections for Buttons, Nav, Hero, Stats, Container, Sections, Cards,
  flows, Spec bar, Services (map, supply-chain layouts, iframe peek, whitepaper
  peek, core bar, service blocks), Contact page, Utilities, Mobile (≤768px), and
  the standalone Whitepaper Sample page.
- `asset/` — webp photography (ocean freight, container yard, warehouse, parcel,
  handyman, team photo), `surpath-logo-full.png`, `surpath-favicon.png`.
- `.gitignore` present. Scaffolded-but-empty: `blog/`, `tool/`.

## Style archives (style/)
- `style_2026-06-10-001/002` … `style_2026-06-12-001..007` — prior snapshots.
- `style_2026-06-13-001.md` — style consistency pass snapshot (PR #33).
- `style_2026-06-13-002.md` — `.btn-block` addition snapshot (PR #33).
- `style_2026-06-13-003.md` — restored iframe-feature snapshot (the 367-line
  archive originally created on `main` by PR #32 as `-001`; it was overwritten by
  the rebase add/add conflict resolution and restored here as `-003`).

## Milestones (merged PRs)
- PR #1–#7 — initial md files/assets, homepage style system, shared stylesheet
  extraction (see prior dated handoffs).
- PR #27 — index/services copy + map marker fixes.
- PR #28 — standalone whitepaper sample page.
- PR #29 — reconcile style.md with PR #27 style.css changes.
- PR #30 / #31 — Contact page added and form layout restructured.
- PR #32 — live iframe document preview in the Services supply-chain section
  (current merged tip `62254fc`).
- **PR #33 — site-wide style consistency pass (OPEN, pending merge)** — the changes
  listed above. https://github.com/sw805206/surpath-website/pull/33

## Open items / TBD
- `partners.html` not built — the Partners nav link is hidden (`display:none`) on
  all pages until it exists. (Partners is not in the scope.md v1 page list; the
  documented Network/Technology/About pages are likewise not yet built.)
- Contact form endpoints are placeholders — wire up the real Apps Script / email
  endpoints before launch.
- style.md: button hover states [PLACEHOLDER]; primary font (Avenir) to confirm
  against the logo source.
- Highlight classes (`.highlight-h1` / `.highlight-body`) exist but are not yet
  applied in any page markup.

## Out of scope (v1)
- No blog at launch; no Chinese-language version at launch.
- Technology/integrations page: placeholder only; VAS page: details TBD.

## Next likely steps
- Merge PR #33, then verify the deployed site.
- Build `partners.html` (then unhide the nav link) and the remaining v1 pages
  (Network/Locations, Technology placeholder, About).
- Apply keyword-highlight classes in copy where useful.

## Process reminders
- Follow `process/claude.md` first, then `process/process.md`; stop and ask on
  conflict or missing file.
- Code always works on a branch, never commits to `main`, never merges — the user
  reviews (browser preview / GitHub PR) and merges manually.
- All pages link the single shared stylesheet; never embed styles in HTML.
- When claude.md/scope.md/style.md/process.md/architecture.md change, create a
  dated archived copy alongside the live file.

# style.md

## Logo
- Full logo: asset/surpath-logo-full.png
- Favicon: asset/surpath-favicon.png
- Usage: surpath-favicon.png as <img> tag (32×32px, 6px border-radius) + "surpath." wordmark in nav. surpath-favicon.png also used for favicon <link rel="icon">.

## Brand Colors
- Nav background: #ffffff
- Nav text / wordmark: #2C4F5C
- Nav links: #444
- Nav active link: #2C4F5C, weight 500, text-decoration underline, color #A8D44F, thickness 2px, underline-offset 4px
- Nav hover link: #444, text-decoration underline, color #A8D44F, thickness 2px, underline-offset 4px
- Nav CTA button: #2C4F5C background, #fff text
- Hero background: #2C4F5C
- Hero text: #fff
- Slogan: #A8D44F (lime)
- Eyebrow: #4A9E8E (mid teal)
- Headline accent: #A8D44F (lime)
- Hero body text: #c8dde3
- Stats bar background: #1e3a45
- Stats numbers: #A8D44F (lime)
- Stats labels: #7aabb8
- Body section background (primary): #ffffff
- Body section background (alternate): #F5F9F0 (sage)
- Card background: #F5F9F0
- Card border: 0.5px #d4e8c8
- Body text: #1E1E1E
- Body text secondary: #555
- Icon color (cards): #3a6b1a
- Spec bar background: #2C4F5C
- Spec bar text: #c8dde3
- Spec dot: #A8D44F
- CTA band background: #2C4F5C
- CTA band title: #fff
- CTA band body: #c8dde3
- CTA band button: #A8D44F background, #2C4F5C text
- Footer background: #1e3a45
- Footer text: #7aabb8
- Keyword highlight (inline emphasis): #4A9E8E (mid teal)

## Typography
- Primary font stack: 'Avenir', 'Avenir Next', 'Nunito', sans-serif
- [PLACEHOLDER — exact font to confirm against original logo source file]
- H1: 28px / weight 500 / line-height 1.3
- H2 (section title): 21px / weight 500
- Eyebrow: 11px / weight 500 / uppercase / letter-spacing 0.1em
- Slogan: 12px / weight 500 / uppercase / letter-spacing 0.12em
- Body: 14px / weight 400 / line-height 1.7
- Caption / label: 11–12px / weight 400
- Nav links: 13px / weight 400
- Card title: 14px / weight 500
- Card body: 13px / weight 400 / line-height 1.55
- Footnote: 11px / weight 400 / #888
- Stats number: 22px / weight 500
- Stats label: 11px / weight 400

## Keyword Highlights
- Used to emphasize key words inline (e.g. "free", "8%", "Specialized", "Trusted").
- Two context-specific classes (a single class cannot serve both contexts, since the
  color differs by where the highlight appears):
  - **`.highlight-h1`** — headline (H1) context. Color #A8D44F (lime), font-weight 500.
  - **`.highlight-body`** — body-copy / bullet context. Color #4A9E8E (mid teal), font-weight 500.
- Both: no background, no underline — color only.
- Lime (#A8D44F) is reserved for the H1/headline context and for bullet dots and
  structural accents; do not use lime for inline emphasis inside body copy (use teal).
- Application is per-page by design; the classes exist in style.css ready to use.
- (Supersedes the former single `.highlight-keyword` class.)

## Color Utilities
- Small single-purpose classes that replace former inline `style="color:…"` hardcodes:
  - **`.text-on-dark`** — color #c8dde3 (var --color-text-on-dark). For text on dark
    surfaces, e.g. the home stats footnote paragraph.
  - **`.link-teal`** — color #4A9E8E (var --color-mid-teal). For inline teal links in
    body copy, e.g. the "Alpha Grid" links in the Services page service blocks.

## Slogan
"One world. Connected." — appears in hero, lime (#A8D44F), uppercase, letter-spaced.

## Layout
- Section backgrounds extend edge to edge (full viewport width)
- Content inside each section is wrapped in a .container that caps at 980px, centered with margin: 0 auto
- Section padding: 40px top/bottom, 0 left/right (padding moves to .container)
- .container padding: 0 28px left/right
- This ensures consistent content width across all screen sizes while backgrounds remain full bleed

## Navigation
- Background: #ffffff
- Padding: 14px top/bottom, 28px left/right
- Logo: icon mark + wordmark, left-aligned
- Links: 13px, #444, gap 20px
- Active link: #2C4F5C, weight 500, text-underline-color #A8D44F, text-decoration-thickness 2px, text-underline-offset 4px
- Hover link: #444, text-underline-color #A8D44F, text-decoration-thickness 2px, text-underline-offset 4px
- CTA "Get started": #2C4F5C bg, #fff text, 5px border-radius, 7px/16px padding
- Mobile (≤768px): hamburger icon (ti-menu-2, #2C4F5C), links stack vertically in dropdown, full width, #ffffff bg, 16px padding per link

## Hero Section
- Background: #2C4F5C
- Padding: 52px top/bottom, 28px left/right
- Order (standard): slogan → H1 → body. No eyebrow. CTA row only when a page already includes one by prior design decision (e.g. home).
- H1 max-width: 980px
- Hero text column max-width: 580px (.hero-text wrapper constrains H1 and body together). CTA row sits outside .hero-text.
- CTA row: gap 12px, flex-wrap

## Stats Bar
- Background: #1e3a45
- 6 equal columns, full width
- Column padding: 16px top/bottom, 18px left/right
- Dividers: 0.5px solid rgba(255,255,255,0.08), vertical, between columns
- Number: 22px / weight 500 / #A8D44F / margin-bottom 2px
- Label: 11px / #7aabb8 / line-height 1.4
- Mobile (≤768px): wraps to 3 columns (flex: 1 1 33.33%)

## Cards (Why Surpath / differentiators)
- Layout: 2×2 grid, gap 12px
- Card: #F5F9F0 bg, 0.5px #d4e8c8 border, 8px border-radius, 20px padding
- Icon: Tabler outline, 20px, #3a6b1a, margin-bottom 10px
- Title: 14px / weight 500 / #1E1E1E / margin-bottom 6px
- Body: 13px / weight 400 / #555 / line-height 1.6
- Footnote: 11px / #888 / margin-top 6px

## Service Lifecycle Flow
- Layout: 4 equal columns, horizontal, no gap between cards
- Card: #fff bg, 0.5px #d4e8c8 border, 8px border-radius, 20px/16px padding, text centered
- Emoji icon: 22px, margin-bottom 8px
- Card title: 13px / weight 500 / #1E1E1E / margin-bottom 4px
- Card body: 12px / weight 400 / #555 / line-height 1.5
- Arrows between cards: "→" character, #4A9E8E, 14px, absolutely positioned at midpoint between cards

## Spec Bar
- Background: #2C4F5C
- Padding: 14px top/bottom, 28px left/right
- Layout: flex row, space-between, flex-wrap
- Dot: 6×6px circle, #A8D44F, margin-right 6px
- Text: 12px / #c8dde3

## Section Layout
- Padding: 40px top/bottom, 28px left/right
- Pattern: eyebrow → title → subtitle → content
- Eyebrow margin-bottom: 8px
- Title margin-bottom: 8px
- Subtitle margin-bottom: 28px
- Alternating backgrounds: white → sage (#F5F9F0) → white

## Buttons
- Primary (dark): #2C4F5C bg, #fff text, 6px border-radius, 11px/24px padding, 14px / weight 500
- Primary (lime): #A8D44F bg, #2C4F5C text, same sizing
- Ghost (on dark bg): transparent bg, 1px rgba(255,255,255,0.35) border, #fff text
- Outlined (on light bg): transparent bg, 1.5px #2C4F5C border, #2C4F5C text
- Width modifier `.btn-block`: add .btn-block to make any button full-width (display: block, width: 100%)
- Hover states: [PLACEHOLDER — TBD]

## CTA Band
- Background: #2C4F5C
- Padding: 40px top/bottom, 28px left/right
- Text centered
- Title: 21px / weight 500 / #fff / margin-bottom 8px
- Body: 14px / #c8dde3 / margin-bottom 20px
- Button: lime primary style

## Footer
- Background: #1e3a45
- Padding: 16px top/bottom, 28px left/right
- Content: "© [year] Surpath Inc." only — no location line
- Layout: single line, centered
- Text: 12px / #7aabb8

## Imagery
- Service section uses real photography (webp format) stored in asset/
- Image cards: 180px height, object-fit cover, 12px border-radius
- Tabler outline icons used in Why Surpath cards
- Service image cards: object-position center on all four cards
- If a specific card image crops poorly, override with object-position: top or object-position: center top
- Third service card (parcel / last-mile) overridden to object-position: center 30% to fix its crop

## Stats Footnote
- Background: #1e3a45 (same as stats bar, sits flush below it), full-bleed
- Font size: 11px / color: #888 (home page overrides text to #c8dde3 inline)
- Link color: #888, text-decoration underline
- Text is left-aligned to the first stat column: inner wrapper max-width 980px, margin 0 auto, padding 6px 18px 10px — the 18px left padding matches the first stat's left padding so the footnote starts exactly under "10+"

## Service Image Cards
- Layout: 2-column grid, gap 16px, margin-top 2rem
- Card: 12px border-radius, white background, box-shadow 0 1px 4px rgba(0,0,0,0.08), overflow hidden
- Image: width 100%, height 180px, object-fit cover
- Card body padding: 14px top/bottom, 16px left/right
- Card title: 15px / weight 600 / #1E1E1E / margin-bottom 4px
- Card subtitle: 13px / weight 400 / #555
- Mobile (≤768px): single column
- Service block bullet lists: text-align: left (explicit — prevents inherited center alignment)

## See All Services Link
- Display: inline-flex, align-items center, gap 10px
- Font: 15px / weight 500
- Arrow span: font-size 26px / weight 700 / line-height 1

## Map Section (Services page)
- Interactive **Leaflet map** with **Stadia "alidade_smooth_dark"** raster tiles, driven by
  inline JS (replaces the earlier static inline SVG). Leaflet CSS + JS are loaded from the
  unpkg CDN; the script fails gracefully (no-op) if Leaflet (`L`) is unavailable.
- Section `.map-section`: background #1a2b3c, full-bleed. Map container `#map`: width 100%,
  height 360px.
- Map options: center [20, 155], zoom 2, `scrollWheelZoom` disabled by default and enabled
  only while the map is focused (click) / disabled on blur; constrained `maxBounds` with
  `maxBoundsViscosity` 1.0; `worldCopyJump` false. US longitudes are expressed > 180 so the
  US and Asia render on a single non-wrapping pane.
- Markers are Leaflet `circleMarker`s; each `bindPopup` shows "Name — Type":
  - HQ: fillColor #A8D44F, radius 8, stroke #1a2b3c weight 2, fillOpacity 0.95 — Brea CA, Shanghai
  - Office: fillColor #4A9E8E, radius 6, stroke #1a2b3c weight 2, fillOpacity 0.9 — Walnut CA, Shenzhen, Beijing, HCMC
  - Warehouse: fillColor #b8b8b8 (warm grey), radius 5, stroke #1a2b3c weight 1.5, fillOpacity 0.85 — ~19 US locations. #b8b8b8 (PR #27) distinguishes it from the office teal (#4A9E8E)
- Draw order (bottom→top, so HQ is never buried by a nearby cluster): warehouse, then office, then HQ.
- Legend bar `.map-legend`: background #1e3a45, padding 10px 0, content in `.container`, flex row, flex-wrap, gap 20px
  - Dot: 8px circle (lime = HQ, teal = Office, warm grey #b8b8b8 = Warehouse)
  - Label: 12px / #c8dde3 — single-word type: "Headquarter", "Office", "Warehouse"

## Section Note (sub-body under subtitle)
- Smaller body line directly below a section subtitle: 13px / weight 400 / #555 / line-height 1.7 / margin-bottom 24px

## Supply Chain Design Bullets (lime dot + title/sub)
- List: no list-style, flex column, gap 16px
- Lime dot bullet: 7px circle #A8D44F, top-aligned on each item
- Bullet title: 14px / weight 600 / #1E1E1E / margin-bottom 2px
- Bullet sub: 12px / weight 400 / #555 / line-height 1.6
- Inline sub link: #4A9E8E / 12px / text-decoration underline
- Keyword highlights inside bullets follow the Keyword Highlights spec

## Whitepaper Sneak Peek
- Container: border 0.5px #d4e8c8, border-radius 8px, padding 16px 20px, #fff bg, overflow hidden, max-height 130px, position relative, margin-top 24px
- Title: 12px / weight 500 / #2C4F5C
- Abstract: 11px / #555 / line-height 1.6
- TOC line: 11px / #888 / margin-top 6px
- Fade overlay: absolute, bottom 0, full width, height 56px, gradient transparent→#fff, content bottom-centered
- CTA button in fade: #2C4F5C bg / #fff text / 11px / padding 5px 16px / border-radius 5px

## Core Services Header Bar
- Background: #1E1E1E, full-bleed, padding 20px 0 (content wrapped in .container)
- Eyebrow: 10px / uppercase / letter-spacing 0.1em / #4A9E8E
- Title: 19px / weight 500 / #fff
- Body: 12px / #7aabb8

## Service Blocks (Services page)
- Alternating: odd = image-left / content-right on #fff; even = image-right / content-left on #F5F9F0 (band background full-bleed, content in .container)
- Row: flex, align-items stretch, min-height 240px
- Image column: 40% width; image height 360px, object-fit cover (mobile: 200px)
- Content column: flex 1, padding 32px 36px, flex column, justify-content center
- Eyebrow ("Service 01"–"04"): 10px / uppercase / letter-spacing 0.1em / #4A9E8E
- Title: 16px / weight 500 / #1E1E1E
- Description: 12px / #555 / line-height 1.65 / margin-bottom 14px
- Bullets (.svc-bullets): no list-style, teal dot (#4A9E8E) 5px circle, gap 7px, 12px / #444, text-align left
- Anchor ids: #freight, #warehouse, #parcel, #assembly
- Mobile (≤768px): stack vertically, image full width (fixed height)

## CTA Band — multi-button row
- Buttons wrapper: flex row, gap 12px, justify-content center, flex-wrap
- Used when the CTA band has more than one button (e.g. lime primary + ghost)

## Why Surpath — 2-column layout (home)
- Replaces the former 2×2 card grid for the "Why Surpath" section
- Grid: 2 columns ~35% / ~65%, gap 32px, align-items start
- Left column: section eyebrow + title + subtitle
- Right column: lime-dot bullet list reusing the Supply Chain Design Bullets pattern (.sc-bullets / .sc-bullet / .sc-bullet-title / .sc-bullet-sub)
- Mobile (≤768px): stack to a single column

## Home Service Cards — 4-up row with flow arrows
- Service image cards display as one horizontal flex row of 4 equal-width cards (no wrap on desktop)
- Between each card: "→" character, #4A9E8E, font-size 16px, vertically centered
- Mobile (≤768px): stack vertically, arrows hidden
- Image object-position: default center; 1st card (Global Freight Forwarding) nudged to 85% center (shows more of the boat); 3rd card (parcel) at center 40%

## Supply Chain Design — 2-column layout (Services page)
- Section body splits into 2 columns: ~60% bullets (left) / ~40% right column (right), via .sc-layout grid; gap 32px, align-items: stretch (PR #27) — both columns (bullet list and peek box) fill to the same height
- Right column (.sc-peek-col) wraps a preview link above the whitepaper peek box:
  - Preview link (.sc-peek-link): "Preview a sample we prepared for a client — contact us to get yours ↗" — 12px / #4A9E8E / underline / display block / margin-bottom 8px, links to contact.html
  - Whitepaper peek box below it (margin-top reset to 0 inside this layout)
  - Peek box height (PR #27): inside this layout the peek box has no fixed max-height (max-height: none, overriding the base 130px) — it stretches to match the height of the bullet list column beside it, via .sc-layout align-items: stretch and height: 100% (flex: 1) on the peek container (.sc-peek-col is flex-column)
  - This preview line is no longer inside the bullet list sub-text
- Mobile (≤768px): stack vertically, bullets first then right column

## Supply Chain Document Preview (iframe peek — Services page)
- Supersedes the static peek above for the Services supply-chain right column. The right column now shows a live, scaled-down preview of whitepaper-sample.html. (The older `.sc-layout` / `.sc-peek-col` / `.whitepaper-peek` rules remain defined in style.css but are no longer used on services.html.)
- Two-column wrapper (`.sc-doc-layout`): display flex, align-items: stretch, gap 32px. Left column (`.sc-bullets`) flex 6; right column (`.sc-doc-col`) flex 4. Mobile (≤768px): stack to a single column, gap 24px
- Right column (`.sc-doc-col`): flex column, align-items: stretch, gap 16px, `min-width: 0` (lets it shrink below the 720px iframe's intrinsic width so overflow clips). Order top→bottom: label → iframe peek (fixed height) → CTA (pinned to bottom via margin-top: auto)
- Label (`.sc-doc-label`): matches the bullet header `.sc-bullet-title` — 14px / weight 600 / body text #1E1E1E. Text: "See how we approach supply chain design."
- Iframe peek box (`.sc-doc-peek`): position relative, height 280px (fixed), overflow hidden, #fff bg, 0.5px #d4e8c8 (card) border, 8px (card) border-radius, cursor pointer. Entire box clickable — inline `onclick` opens whitepaper-sample.html (same tab)
  - Iframe (`.sc-doc-iframe`): src whitepaper-sample.html, width 720px, height 1000px, border none, pointer-events none, transform-origin top left. Scaled to fit via JS: `transform: scale(containerWidth / 720)`, recomputed on load + window resize (unique ids `#scDocPeek` / `#scDocIframe`)
  - Bottom fade (`.sc-doc-fade`): absolute, full width, height 70px, gradient transparent → #fff (var(--color-white)), pointer-events none. Same treatment as `.whitepaper-fade`, taller
  - Hover overlay (`.sc-doc-overlay`): absolute inset 0, background rgba(44,79,92,0.06), opacity 0 → 1 on `.sc-doc-peek:hover`, transition 0.2s; centers a pill label
  - Hover pill (`.sc-doc-overlay-label`): "View sample document →" — small button pattern (matches .nav-cta sizing): #2C4F5C bg / #fff / 13px / weight 500 / padding 7px 16px / border-radius 5px
- CTA (`.sc-doc-cta`): reuses the primary dark button (`.btn.btn-dark`: #2C4F5C bg, #fff, 14px / weight 500, padding 11px 24px, border-radius 6px; no hover — buttons are PLACEHOLDER) plus width 100%, margin-top auto, text-align center. Text: "Contact us to get your customized white paper", links to contact.html

## Contact Page (contact.html)
All Contact-page CSS lives in style.css under `/* Contact page */` (migrated out of the
former embedded `<style>` block so no styles are embedded in the HTML). The page reuses the
shared nav, hero (standard order: slogan → H1 → body — `.hero-slogan` "One world. Connected."), `.section`, `.container`, `.eyebrow`,
`.section-title`, `.section-subtitle`, and footer. The **submit button reuses the shared
`.btn .btn-lime`** classes (the former standalone `.submit-btn` was removed). Contact-specific
patterns:

### Zone layout
- `.zone1`: 2 equal columns (grid `1fr 1fr`), gap 24px, align-items stretch.
- `.zone2`: single column, width `calc(50% - 12px)` — matches Zone 1's left column.
- Mobile (≤768px): both collapse to a single column; `.zone1` gap 18px; `.col-right` order -1 (photo + trust card move above the form).

### Panels / cards
- `.panel`: #fff bg, 0.5px #d4e8c8 border, 8px radius, padding 22px 22px 24px.
- `.panel-title`: 15px / weight 600 / #1E1E1E / margin-bottom 16px.
- `.col-right`: flex column, gap 14px.
- `.team-photo`: flex 1, width 100%, min-height 220px, object-fit cover, 12px radius, #2C4F5C placeholder tint while loading.

### Trust card
- `.trust-card`: sage (#F5F9F0) bg, 0.5px #d4e8c8 border, 8px radius, padding 14px.
- `.trust-item`: flex, gap 10px, 12.5px / line-height 1.5 / #555; `+ .trust-item` margin-top 10px; icon #3a6b1a / 18px.

### Form fields
- `.field`: margin-bottom 16px (last-child 0).
- `.field-label`: block, 12.5px / weight 500 / #2C4F5C / margin-bottom 6px; `.req` mark #4A9E8E. **This is the single size for every field label — no field label may override 12.5px** (see Contact form typography rules).
- `.field-hint` (and its JS-driven alias `.field-hint-dynamic`): 11px / weight 400 / #888 / margin-bottom 6px. Both share one rule; `.field-hint-dynamic` carries the same values but its text content is set via JS (lives below the Additional comments label and replaces the static hint when conditions are active).
- `.text-input` (also `textarea`/`select`): width 100%, padding 9px 12px, inherit font, **13px / weight 400**, #1E1E1E, #fff bg, 1px #d4e8c8 border, 6px radius; focus → border #4A9E8E + 3px teal glow; placeholder #9aa7a3; `.invalid` → red #c0392b border (+ red glow on focus). `textarea.text-input` min-height 92px, resize vertical, line-height 1.6.
- `.field-error`: hidden by default, 11.5px / #c0392b / margin-top 5px; `.show` reveals it.

### Contact form typography rules (consistency — 2026-06-13)
Two unified rules govern text in the contact form so block headings and entry text never drift:
- **Block headings — 15px / weight 600.** Applies to `.panel-title` (#1E1E1E), `.qblock-title` (#2C4F5C, bumped from 14px), and the dynamic Zone 2 heading "Tell us more". "Tell us more" must use the **`.panel-title`** style (15px / weight 600 / #1E1E1E) — it must NOT use `.section-title` (21px), which previously caused a mismatch against "Basic information".
- **Field labels — 12.5px / weight 500 / #2C4F5C.** `.field-label` is uniform across every use (e.g. "What can we help with?", "Business type"); no instance may override the size.
- **All form entry text and selection results — 13px / weight 400.** Applies to: `.text-input` (text inputs, the timezone/select selected value, volume input values), the dropdown trigger summary text and `.dd-option` panel option text, `.vol-uom` unit labels, `.check` checkbox-chip text, and `.method-btn` method-button text (weight dropped from 500 to 400 for this rule).

### Checkbox chips
- `.checks`: flex wrap, gap 8px. `.check`: inline-flex chip, gap 7px, padding 8px 12px, 13px / #2C4F5C, sage bg, 1px #d4e8c8 border, 6px radius; checkbox `accent-color` #4A9E8E; `:has(input:checked)` → bg #e8f3dd, border #bcd9a3; hover border #bcd9a3.

### Topic selector
- `.topics`: **2-column equal-width grid** (`grid-template-columns: 1fr 1fr`), gap 10px, margin-top 14px. Each `.topic-btn` stretches to fill its column, so all buttons are equal width; the 5 buttons fill rows top→bottom, with "General inquiry" in the left column of the last row.
- `.topic-btn`: inline-flex pill, left-aligned (`justify-content: flex-start`, `text-align: left`), single-line (`white-space: nowrap`), gap 8px, padding 11px 9px, 13px / weight 500 / #2C4F5C, sage bg, 1px #d4e8c8 border, 8px radius; icon 17px (flex-shrink 0); hover border #bcd9a3; `.selected` → #2C4F5C bg / #fff text. The tightened padding/gap + nowrap keep the longest label ("Supply chain consultation") on one line within the ~197px grid column, with a uniform icon→text gap across all buttons.
- **Button text is sentence case** (first word capitalized only): "Fulfillment / warehousing", "Last mile rates", "Global forwarding", "Supply chain consultation", "General inquiry".
- **Restart link** (`.topics-restart`): a plain `<span>` (role="button", tabindex 0) in the right column of the last grid row — `justify-self: end`, `align-self: center`, 12px / #4A9E8E / underline / cursor pointer. Clicking (or Enter/Space) clears all topic-button selections, hides every dynamic question block, and clears all field values inside those blocks. It does **not** reset Zone 1 fields (name, company, email, etc.).

### Dynamic question blocks
- `.qblock`: 0.5px #d4e8c8 border, 8px radius, padding 18px 20px 20px, margin-top 16px, #fff bg. `.qblock-title`: 15px / weight 600 / #2C4F5C / margin-bottom 14px (15px per the Contact form typography rules).
- `[hidden] { display: none !important; }` — global rule (in the Contact section) enforcing the `hidden` attribute over flex/grid; drives the JS show/hide of blocks and fields.

### Contact preference (dark band)
- `.pref-band`: #2C4F5C bg, 8px radius, padding 16px, margin-top 20px. `.pref-intro`: 13px / #c8dde3. `.pref-label`: block, 12.5px / weight 500 / #c8dde3; `.req` mark lime #A8D44F.
- `.methods` / `.method-btn`: ghost buttons on the dark band — transparent bg, 1px rgba(255,255,255,0.35) border, #fff text; hover border lime; `.selected` → lime bg / #2C4F5C text.
- `.pref-conditional`: margin-top 14px; its labels are #c8dde3 with lime req marks; `.field-error` inside the band is light pink #ffd2cc.

### Success message
- `.success-msg`: 0.5px #d4e8c8 border, 8px radius, sage bg, padding 32px 28px, centered; icon 34px #3a6b1a; text 15px / #1E1E1E. Injected in place of the form's Zone 2 on successful submit.
- **Icon color override (2026-06-13):** the injected checkmark `<i>` carries an inline `style="color:#2C4F5C"` (dark teal) so it overrides the global `.success-msg i` green for this page only — the global rule is left untouched so other `.success-msg` uses are unaffected.

### Contact form rewrite — new patterns (2026-06-13)
The contact form was rewritten to a fully state-driven `updateVisibility()` model. New
CSS patterns added to style.css under the Contact page section:

#### Volume fields (number input + inline UOM label) — `.vol-*` (supersedes `.volume-*`, 2026-06-13)
Renamed from the former `.volume-row` / `.volume-unit` (those classes were removed from style.css).
- `.vol-row`: flex, align-items center, gap 10px — pairs a number input with a unit-of-measure label rendered **outside** the input box.
- `.vol-input`: `flex: 0 0 160px` (fixed width, not full-width). Used as `type="number"` (e.g. `min="0" step="1"`), with native spinner arrows suppressed: `-webkit-appearance: none` on the `::-webkit-inner/outer-spin-button` and `-moz-appearance: textfield`. Carries `.text-input` for its border/padding/13px appearance; `flex: 0 0 160px` overrides the default 100% width.
- `.vol-uom`: 13px / weight 400 / #555 (var --color-text-secondary) / flex-shrink 0. Unit text e.g. "loads / month", "packages / month", "pallets / month".
- Mobile (≤768px): `.vol-input` narrows to `flex: 0 0 130px`.

#### Shipping Rates sub-selections
- Carriers and Package size reuse `.checks` / `.check` (multi-select chips). Sub-group headers use `.field-label`.
- "Where will goods ship from?" is a **single-select radio** group, also rendered with `.checks` / `.check` (radio inputs inherit the chip styling and teal `accent-color`).
- The "AHS required" package-size chip carries a `title="Additional Handling Service"` tooltip.

#### Phone input (dark pref band) — updated 2026-06-14
- The phone field is a **single `.text-input`** (`type="tel"`, no label) with placeholder "Include country code, e.g. +86 138 0000 0000". The former country-code dropdown (`.phone-cc` select) and the paired `.phone-row` layout were removed (those classes are deleted from style.css). Shown only when Phone is selected (`#field-phone`); required validation preserved when Phone is selected.

#### Timezone field & inline notes (dark pref band) — updated 2026-06-14
- The timezone `select` is now **conditional**: shown only when **Phone or Zoom** is selected, hidden for Email. It carries the `.field-label` "Your time zone*".
- The select has **exactly 2 options**: (1) the **detected timezone**, "[label] — UTC±X", derived dynamically from the browser's Intl API (`Intl.DateTimeFormat` long `timeZoneName` + `getTimezoneOffset`) and inserted as the first option, pre-selected; (2) "Others — see comments". All former fixed US/Asia options were removed. "Others — see comments" is a valid selection (no extra reminder).
- `.field-note`: small inline note (11px / line-height 1.5 / margin-top 4px). Inside the pref band it is colored var(--color-text-on-dark) (#c8dde3). Used for "We'll do our best to reach you during your business hours." (a note, not a `.field-hint`) — it sits inside the timezone block, so it shows/hides with the timezone field (Phone or Zoom only).
- The `.tz-mismatch` element and all JS driving it were **removed** (2026-06-14): the class is deleted from style.css and no longer exists on the page.

### Custom Dropdown — multi-select (2026-06-13)
A styled dropdown for multi-select fields (Business type, Fulfillment service needs, Package
sizes, Global Forwarding). Opens on trigger click; closes on outside click or Escape (JS toggles
the `.open` class on trigger and panel). CSS lives in style.css under the Contact page section.
- **`.dd-wrap`**: position relative, width 100% — anchors the absolutely-positioned panel.
- **`.dd-trigger`**: full-width button with `.text-input` appearance (same border, radius, bg, 9px 12px padding), 13px / weight 400. Flex row, space-between: selected-summary text left-aligned (`.dd-summary`, ellipsis-truncated), chevron right-aligned (`.dd-chevron`). Focus → teal border + 3px teal glow. `.dd-trigger.open` → border-color #4A9E8E. When open the chevron rotates 180° (`.dd-trigger.open .dd-chevron`).
- **Selected summary text** (in `.dd-summary`): "Select…" when nothing selected; the single item's label when one is selected; "FirstItem +N" when multiple are selected.
- **`.dd-panel`**: absolute below the trigger (top calc(100% + 4px), left/right 0), white bg, 0.5px #d4e8c8 border, 8px radius, box-shadow 0 2px 8px rgba(0,0,0,0.08), z-index 100, max-height 260px, overflow-y auto. `display: none` by default; `.dd-panel.open` → display block.
- **`.dd-option`**: a `<label>` wrapping a hidden checkbox + the custom checkbox span (`.dd-cb`) + visible text, **in that order**. Flex row, justify-content flex-start, gap 10px, padding 10px 14px, 13px / #1E1E1E, cursor pointer. Hover → #F5F9F0 bg. Checked (`:has(input:checked)`) → #F5F9F0 bg.
- **`.dd-option input`** (the real checkbox): visually hidden (clip rect) — it remains the form value and the `:has()` state source.
- **`.dd-cb`** (left-aligned custom checkbox — **replaces the former trailing `.dd-check` ✓ icon**, 2026-06-13): a 16×16px styled `<span>` placed **before** the label text. Display flex, centered, flex-shrink 0. Unchecked: #fff (white) fill, 3px border-radius, 1.5px solid #d4e8c8 (card border). Checked (`.dd-option:has(input:checked) .dd-cb`): #2C4F5C (primary) fill + #2C4F5C border. Inside it a white `ti-check` icon (`.dd-cb i`: 11px / #fff) sits `opacity: 0` by default and `opacity: 1` only when the option is checked (`.dd-option:has(input:checked) .dd-cb i`). The custom span is purely the visual indicator; the native `<input>` carries state.
- **`.dd-option.dd-sep`**: 0.5px #d4e8c8 top border — visually separates the trailing "Others" option from the list above it.

### Contact preference (dark band) — updated 2026-06-13
- The standalone `.pref-label` ("Contact method*") and the method `.field-error` were **removed** — Email is pre-selected by default, so an empty-method state is impossible and the selector needs no label.
- The `.pref-intro` is now just "What's the best way to reach you?" (the "within 2 business days" sentence was dropped).
- `.pref-intro` typography (updated 2026-06-13): **15px / weight 600 / #c8dde3 (on-dark)** — matches `.qblock-title` sizing and weight, adapted to the dark band (the on-dark color is kept; #2C4F5C is light-background only). The former 13px / line-height 1.6 / margin-bottom 14px overrides were removed so it follows the qblock-title rhythm.
- Order inside `.pref-band` (updated 2026-06-14): intro → method selector → phone input (when Phone selected) → timezone field + its `.field-note` (when Phone or Zoom selected). The DOM order is intro → methods → `#field-phone` → `#field-timezone`, which renders as:
  - **Phone:** intro → methods → phone input → timezone dropdown → "We'll do our best…" note
  - **Zoom:** intro → methods → timezone dropdown → "We'll do our best…" note
  - **Email:** intro → methods (timezone and note both hidden)

## Whitepaper Sample Page (standalone — whitepaper-sample.html)
A standalone document-style page, not in the main nav. Linked from the Services
page "Preview a sample…" line (`.sc-peek-link` → whitepaper-sample.html). Mimics
a leaked client proposal: a line-numbered document with most lines blurred and a
few left clear. All CSS lives in style.css under `/* Whitepaper Sample Page */`;
the page uses literal hex values from the document palette (not the site tokens)
so the section is self-contained and leaves existing styles untouched.

### Header & footer (reused)
- Header reuses `.nav` / `.nav-inner` with only a `.nav-wordmark` ("surpath.",
  links to index.html) on the left and a `.nav-cta` ("Contact us", links to
  contact.html) on the right. No nav menu and no hamburger toggle (so the mobile
  nav rules are inert on this page).
- Footer reuses `.footer` / `.footer-inner` ("© 2025 Surpath Inc.").

### Page backdrop & document container
- `.wp-page`: light backdrop #eef1f4, padding 32px 16px (mobile: 20px 0) — sets
  the white document off as a floating page.
- `.wp-doc`: max-width 720px, centered, background #fff, padding 48px 36px 48px
  80px (extra left padding houses the line-number gutter), box-shadow
  0 1px 6px rgba(0,0,0,0.10), border-radius 2px. `counter-reset: wpline`.
  Mobile (≤768px): padding 32px 18px 32px 52px, border-radius 0.

### Document header block
- `.wp-badge`: inline-block, bg #2C4F5C, color #A8D44F, Avenir 13px, padding
  6px 12px, border-radius 4px. Text "surpath."
- `.wp-doc-title`: Avenir 20px / weight 700 / #1E1E1E / margin-top 14px.
- `.wp-doc-meta`: 11px / #888 / margin-top 4px ("Surpath Inc. · 2025").
- `.wp-divider`: thin rule — border-top 1px solid #e0e0e0, margin 18px 0. Reused
  between blocks throughout the document.

### Line numbers & body lines
- `.wp-line`: body text — Georgia 12px / line-height 1.75 / #1E1E1E /
  margin 8px 0 0 / position relative.
- `.wp-line::before`: auto-incrementing gutter number via `counter-increment:
  wpline; content: counter(wpline)`. Absolute, left -44px (mobile -34px),
  width 30px (mobile 24px), right-aligned, monospace 10px / #ccc. Display-only:
  `user-select: none; pointer-events: none`. Only `.wp-line` elements increment
  the counter — titles, tables, and page breaks are unnumbered.

### Blur
- `.wp-blur` (line-level) and `.wp-cell-blur` (table-cell-level): `filter:
  blur(2.5px); color:#bbb; user-select:none; pointer-events:none`. The gutter
  number on a blurred line stays crisp (the ::before is not blurred).

### Section & sub-section titles (always clear)
- `.wp-section-title`: Avenir 14px / weight 700 / #1E1E1E / margin-top 24px.
- `.wp-subtitle`: Avenir 12.5px / weight 700 / #1E1E1E / margin-top 14px.

### [client] redaction token
- `.wp-client`: color #4A9E8E, font-style italic. Inside a blurred line,
  `.wp-blur .wp-client` overrides the color to #ccc.

### Numbered action list
- `.wp-ol`: ol, margin 4px 0 0 18px; `.wp-ol li` margin 2px 0. Sits inside a
  single `.wp-line` (gets one gutter number for the whole list).

### Page-break markers (visual only)
- `.wp-pagebreak`: dashed top border (1px dashed #c8c8c8), margin 28px 0,
  padding-top 6px, Avenir 9px / uppercase / letter-spacing 0.08em / #aaa.
  Label text e.g. "Page 2". Not a print page break.

### Cost tables
- `.wp-table-label`: Avenir 11px / weight 700 / #555 / margin 16px 0 4px.
- `.wp-table-wrap`: overflow-x auto (wide 5-column tables scroll on mobile).
- `.wp-table`: width 100%, border-collapse, Georgia 11px. Cells: 1px solid
  #e0e0e0 border, padding 4px 8px, right-aligned, nowrap. `th`: Avenir 700,
  background #f7f9fa, #1E1E1E. First column (th + td) left-aligned and wrapping.
- `.wp-cell-blur`: per-cell blur (see Blur).
- `.wp-cell-tariff`: clear red #c0392b / weight 700 — keeps tariff rows legible
  amid blurred data (e.g. 145% rows).
- `.wp-cell-red`: clear red #c0392b — optimized "new unit cost" values.
- `.wp-row-green`: optimized-cost highlight row — `td` bg #2C4F5C / #fff;
  first `td` (label) #A8D44F.

### Data-flow diagram
- `.wp-diagram`: inline SVG, viewBox 0 0 560 310, display block, width 100%,
  height auto, margin 10px 0 4px. Styled with SVG presentation attributes:
  nodes are rect fill #f0f4f8 / stroke #c8dde3 / rx 4 with Avenir 9px labels and
  7.5px #666 sub-labels; "Plan to Stock" node filled lime #A8D44F. Connectors:
  teal #4A9E8E arrows (marker `#wpArrow`) plus one dashed lime arrow (marker
  `#wpArrowLime`) from Plan to Stock to Warehouse. Bottom band: rect fill #444
  in three segments — "PO Management | Global Inbound | Outbound Fulfillment" in
  white. Diagram layout is an in-repo reconstruction of the approved data-flow
  mock with all specified nodes, colors, and the bottom band.

### Bottom CTA
- `.wp-cta-wrap`: text-align center, margin-top 32px.
- `.wp-cta`: inline-block, bg #2C4F5C, #fff, Avenir 12px, padding 10px 24px,
  border-radius 6px. Links to contact.html ("Contact us to get your customized
  white paper").

## Notes
- Locked values are final. [PLACEHOLDER] values are pending decision.
- New style patterns from each page build should be added here before the page prompt is written.
- When this file is updated, create an archived copy per claude.md archiving rules.

# style.md

## Logo
- Full logo: asset/surpath-logo-full.png
- Favicon: asset/surpath-favicon.png
- Usage: icon mark (32×32px, #4A9E8E background, 6px border-radius) + "surpath." wordmark in nav. Icon mark alone for favicon and compact use.

## Brand Colors
- Nav background: #F2F2F2
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

## Slogan
"One world. Connected." — appears in hero, lime (#A8D44F), uppercase, letter-spaced.

## Layout
- Section backgrounds extend edge to edge (full viewport width)
- Content inside each section is wrapped in a .container that caps at 1280px, centered with margin: 0 auto
- Section padding: 40px top/bottom, 0 left/right (padding moves to .container)
- .container padding: 0 28px left/right
- This ensures consistent content width across all screen sizes while backgrounds remain full bleed

## Navigation
- Background: #F2F2F2
- Padding: 14px top/bottom, 28px left/right
- Logo: icon mark + wordmark, left-aligned
- Links: 13px, #444, gap 20px
- Active link: #2C4F5C, weight 500, text-underline-color #A8D44F, text-decoration-thickness 2px, text-underline-offset 4px
- Hover link: #444, text-underline-color #A8D44F, text-decoration-thickness 2px, text-underline-offset 4px
- CTA "Get started": #2C4F5C bg, #fff text, 5px border-radius, 7px/16px padding
- Mobile (≤768px): hamburger icon (ti-menu-2, #2C4F5C), links stack vertically in dropdown, full width, #F2F2F2 bg, 16px padding per link

## Hero Section
- Background: #2C4F5C
- Padding: 52px top/bottom, 28px left/right
- Order: slogan → eyebrow → H1 → body → CTA row
- Body text max-width: 500px
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
- Third service card (parcel / last-mile) overridden to object-position: center bottom to fix its crop

## Stats Footnote
- Background: #1e3a45 (same as stats bar, sits flush below it)
- Font size: 11px / color: #888
- Padding: 6px top, 28px left/right, 10px bottom
- Link color: #888, text-decoration underline

## Service Image Cards
- Layout: 2-column grid, gap 16px, margin-top 2rem
- Card: 12px border-radius, white background, box-shadow 0 1px 4px rgba(0,0,0,0.08), overflow hidden
- Image: width 100%, height 180px, object-fit cover
- Card body padding: 14px top/bottom, 16px left/right
- Card title: 15px / weight 600 / #1E1E1E / margin-bottom 4px
- Card subtitle: 13px / weight 400 / #555
- Mobile (≤768px): single column

## See All Services Link
- Display: inline-flex, align-items center, gap 10px
- Font: 15px / weight 500
- Arrow span: font-size 26px / weight 700 / line-height 1

## Notes
- Locked values are final. [PLACEHOLDER] values are pending decision.
- New style patterns from each page build should be added here before the page prompt is written.
- When this file is updated, create an archived copy per claude.md archiving rules.

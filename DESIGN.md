---
name: Copper Thistle (Total CMS restaurant starter)
description: A restaurant site set as a printed two-ink bill of fare with a copper accent, laid on a colored cover, rebranded from four dials.
colors:
  cover: "oklch(0.34 0.084 165)"
  cover-night: "oklch(0.2 0.054 165)"
  on-cover: "oklch(0.97 0.015 165)"
  on-cover-night: "oklch(0.9 0.02 165)"
  spot: "oklch(0.44 0.12 165)"
  spot-night: "oklch(0.8 0.12 165)"
  spot-strong: "oklch(0.34 0.12 165)"
  spot-strong-night: "oklch(0.88 0.096 165)"
  copper: "oklch(0.5 0.125 50)"
  copper-night: "oklch(0.74 0.125 50)"
  copper-strong: "oklch(0.42 0.115 50)"
  copper-strong-night: "oklch(0.82 0.105 50)"
  copper-cover: "oklch(0.76 0.115 50)"
  copper-cover-strong: "oklch(0.84 0.09 50)"
  stock: "oklch(0.995 0.004 60)"
  stock-night: "oklch(0.155 0.01 60)"
  ink: "oklch(0.2 0.015 60)"
  ink-night: "oklch(0.93 0.01 60)"
  ink-muted: "oklch(0.43 0.015 60)"
  ink-muted-night: "oklch(0.74 0.012 60)"
  rule: "color-mix(in oklch, oklch(0.2 0.015 60) 22%, transparent)"
typography:
  display:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "Yeti billboard, lg to 13rem, proportional to name length"
    fontWeight: 850
    lineHeight: 0.86
    letterSpacing: "-0.01em"
    fontVariation: "'wdth' 62"
  display-page:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(2.75rem, 9cqi, 6rem)"
    fontWeight: 850
    lineHeight: 0.86
    letterSpacing: "-0.01em"
    fontVariation: "'wdth' 62"
  headline:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-md)"
    fontWeight: 700
    letterSpacing: "0.2em"
    fontVariation: "'wdth' 118"
  title:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-md)"
    fontWeight: 650
    letterSpacing: "0.06em"
  body:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-md)"
    fontWeight: 400
    fontFeature: "'tnum' 1"
  lede:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-md)"
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: "0.08em"
    fontVariation: "'wdth' 110"
  label:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-sm)"
    fontWeight: 600
    letterSpacing: "0.12em"
  brand:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "var(--yeti-text-lg)"
    fontWeight: 800
    letterSpacing: "0.02em"
    fontVariation: "'wdth' 70"
rounded:
  none: "0"
spacing:
  xs: "var(--yeti-space-xs)"
  sm: "var(--yeti-space-sm)"
  md: "var(--yeti-space-md)"
  lg: "var(--yeti-space-lg)"
  xl: "var(--yeti-space-xl)"
  2xl: "var(--yeti-space-2xl)"
  3xl: "var(--yeti-space-3xl)"
  frame-inset: "clamp(.4rem, 1.2vw, .9rem)"
  cover-margin: "clamp(.375rem, 2vw, 2rem)"
  card-block: "clamp(2.5rem, 6vw, 5rem)"
  plate: "clamp(.3rem, .8vw, .55rem)"
  today-box: "clamp(1.25rem, 3vw, 2.25rem)"
components:
  button-primary:
    backgroundColor: "{colors.spot}"
    textColor: "{colors.stock}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: ".9em 1.6em"
  button-primary-hover:
    backgroundColor: "{colors.spot-strong}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: ".9em 1.6em"
  button-cover:
    backgroundColor: "{colors.stock}"
    textColor: "{colors.cover}"
    rounded: "{rounded.none}"
    padding: ".6em 1.2em"
  nav-bar:
    backgroundColor: "{colors.cover}"
    textColor: "{colors.on-cover}"
    typography: "{typography.label}"
  bill-card:
    backgroundColor: "{colors.stock}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "{spacing.card-block}"
  today-box:
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "{spacing.today-box}"
  plate:
    backgroundColor: "{colors.stock}"
    rounded: "{rounded.none}"
    padding: "{spacing.plate}"
---

# Design System: Copper Thistle

## Overview

**Creative North Star: "The Bill of Fare"**

Every page is the restaurant's printed menu card for today. A bright white card (not cream) lies on a deep cover in the brand hue, which shows around it on every side and carries the top bar and the footer. The card is printed in two inks only: a warm near-black for text and one spot ink in the brand hue for the masthead, the rules, the printed frame and today's marks. Corners are square, depth comes from paper on cover rather than shadow, and the one typeface (Archivo, using its width axis) does every job from the extra-condensed masthead to the wide letterspaced section heads.

The card is dated. A dateline between two spot rules opens it with today's date and whether the kitchen is open, today's row in the hours list prints in the spot ink, and current specials sit in the boxed "Today" insert. Menu lines read the way a printed menu does: the dish name in caps, a dotted leader, and a right-aligned tabular price. Photos are printed plates: square, with a small white margin and a hairline border.

The system is a starter that has to survive a rebrand. All color comes from four dials in `css/theme.css` (`--yeti-hue-primary`, `--yeti-hue-secondary`, `--yeti-hue-neutral`, `--yeti-chroma`) through `light-dark()` OKLCH formulas, so a new hue reprints the cover, spot ink and buttons in light and dark mode at once. The confirmed visual rejections: fine-dining luxe (black and gold, hairline-weight type), loud chain-restaurant styling (saturated red and yellow, promo banners, starbursts, coupon badges), and generic SaaS styling (gradient heroes, glassmorphism, grids of icon tiles).

**Key Characteristics:**
- White card stock on a deep brand-hue cover; the cover is the page background, the top bar and the footer.
- Two inks, near-black and one spot ink, plus copper as a small accent on the logo, divider rules and Book a table buttons.
- One grotesque family (Archivo), used across its width axis from 62% to 118%.
- Square corners everywhere except buttons (a leaf cut) and the Today box (8px), with a double rule inset inside the card edge as the frame.
- Dotted leaders to tabular prices; dietary notes set as small letterspaced capitals, not badges.
- Motion happens once: the card rises into place and the dateline rules draw across.

## Colors

The page is a two-ink print job on white stock, laid on a cover in the same hue as the spot ink. Every value is a formula from the four dials (canonical formulas live in `.impeccable/design.json`); the frontmatter values are those formulas resolved at the shipped dials (hue 165, neutral hue 60, chroma 0.12). Each token has a `-night` sibling for dark mode.

### Primary
- **Evergreen Cover** (`cover`): the deep field behind and around the card, plus the sticky top bar, the mobile menu panel and the footer. At dark mode it drops to a near-black green (`cover-night`).
- **Cover Light** (`on-cover`): text, links, the menu icon and the footer's rules on the cover. The footer's own text uses it, with the other inks following its forced dark scheme, so the footer prints in one light ink.
- **Evergreen Spot Ink** (`spot`): the second ink on the card. Used at full strength for the masthead name, focus rings, the caret and text selection. In dark mode it lifts to a light green (`spot-night`).
- **Copper** (`copper`, `copper-cover`): the accent, from `--yeti-hue-secondary`. A deep burnt copper on white stock and a bright copper on the dark card, for the divider rules, today's hours row and the masthead Book a table button. `copper-cover` is a single bright value for the cover, which is dark in both modes: the logo and the top-bar button.
- **Deep Spot** (`spot-strong`): the primary button's hover state only.

### Neutral
- **Card Stock** (`stock`): the card surface, plate margins and text on spot-ink buttons. A white with the faintest warmth (chroma 0.004); in dark mode it becomes a warm near-black (`stock-night`).
- **Press Black** (`ink`): body text, dish names, prices and the outline button. Warm near-black, never pure black.
- **Faded Ink** (`ink-muted`): dietary notes and other secondary text.
- **Hairline Rule** (`rule`): plate borders, table and card borders, at 22% of the ink. Dotted leaders use the ink at 40%.

### Named Rules
**The Two Inks and a Metal Rule.** The card prints in ink and spot ink. Copper (`--yeti-hue-secondary`) is the one accent, and it is hardware only: the logo and the Today box's thistle, the divider rules beside the dateline and section heads, the Book a table buttons and today's row in the hours. It never colors the restaurant name or body text, and it never fills a region. Any fourth color breaks the print job.

**The Four Dials Rule.** Rebrand by changing `--yeti-hue-primary`, `--yeti-hue-secondary`, `--yeti-hue-neutral` and `--yeti-chroma`, never by hard-coding a color. Every surface and ink is derived from those dials in both modes.

**The Spot Means Today Rule.** Inside the body of the card, spot ink marks the masthead at full strength. The card's frame and the Today box's line use it at 30%, faint on purpose, so they hold the page without competing with it. Ordinary text and prices stay in ink. Divider rules and today's hours row are copper; the Today box head prints in ink.

## Typography

**Display Font:** Archivo variable (with system-ui, sans-serif), self-hosted from `fonts/` under the OFL
**Body Font:** Archivo (same family)

**Character:** One grotesque family stretched across its width axis, condensed and heavy for the name and wide and letterspaced for the section heads, the way a jobbing printer sets a menu from a single type case. Headings are uppercase throughout; body text uses tabular figures so prices line up.

### Hierarchy
- **Display** (850, Yeti `billboard` with `data-fit="lg-display"`, ceiling 13rem, line-height 0.86, width 62%): the restaurant name on the home masthead, in spot ink. It fills the card on one line at about 96% of the width. A billboard does not measure text, so `index.twig` passes the name's letter count as `--bill-name-length` and `theme.css` sets `--yeti-fit-width` from it, with a floor of 6 letters. A name too wide for one line wraps, balanced.
- **Display, page size** (850, `clamp(2.75rem, 9cqi, 6rem)`, width 62%): the same masthead a size down for the title of each inner page.
- **Headline** (700, text-md, 0.2em tracking, width 118%, caps): section heads, centered between two spot rules. On screens under 30rem the width drops to 100% and the tracking to 0.1em so a two-word head stays on one line.
- **Title** (650, text-md, 0.06em tracking, caps): dish and special names on a menu line; 0.9x size and 0.04em tracking in the featured row.
- **Body** (400, text-md, tabular figures): descriptions, address, hours. Prices are 700.
- **Lede** (500, text-md, 0.08em tracking, width 110%, caps, line-height 1.5, max 44ch): the tagline under the masthead.
- **Label** (600, text-sm, 0.12em tracking, caps): nav links, footer heads (text-sm h2), dietary notes (0.9x text-sm, in faded ink), and the dateline (width 112%, 0.16em tracking). Buttons use the same style at 700 and 0.1em.
- **Brand** (800, text-lg, width 70%, caps): the restaurant name in the top bar, on one line beside the logo. Below 24rem the name is visually hidden and the logo stands alone.

### Named Rules
**The One Case Rule.** Every role is Archivo. Contrast between roles comes from width, weight and tracking, not from a second family. To change the font, swap the files and the two `--yeti-font-*` lines.

**The Leader Rule.** A priced line is name, dotted leader, price: the leader fills the gap and the price stays on the last line of a wrapped name. Prices are never set apart from their dish.

## Layout

The page is a shell of cover around one card. The cover shows `clamp(.375rem, 2vw, 2rem)` at the sides and bottom of the card; the top bar runs full width on the cover and is sticky. The card is at most 84rem wide, centered, with block padding `clamp(2.5rem, 6vw, 5rem)` and inline padding equal to the frame inset plus `clamp(.75rem, 3vw, 2rem)`, so content clears the printed frame on a phone.

Inside the card, content sits in centered Yeti `center` columns (2xl for the masthead and hero plate, xl for specials and featured dishes, lg for hours and location) stacked with Yeti's spacing scale, mostly at xl and 2xl gaps. The masthead is a centered single-column grid that is also a size container, so the name, dateline and tagline scale to the card rather than the viewport.

Responsive behavior: the dateline stacks the date over the hours and drops the dot when its container is under 34rem. Featured dishes are a small plate beside each menu line on a phone and become up to four plates across from 48rem. The menu page flows its sections into two newspaper columns from 64rem, with sections kept whole. The nav folds into a popover behind a menu button below Yeti's md threshold.

## Elevation & Depth

The system is flat. There are no shadows anywhere; depth comes only from white stock lying on the darker cover, the Today box's paper tint, and from printed lines: the double frame inside the card's edge, the Today box's inset line, and the hairline borders around plates.

### Named Rules
**The Paper on Cover Rule.** Separation is paper against cover or a printed rule, never a shadow, blur or gradient.

## Shapes

Every corner is square except on buttons and the Today box: `--yeti-radius-md`, `--yeti-radius-lg` and the badge radius are 0, images are never rounded, and `--yeti-button-radius` is `.6em .12em / .42em .12em`: a leaf cut, with two opposite corners swept and two nearly square, so a button reads as something to press and echoes the thistle's leaves. It is plain `border-radius`, so it works in every browser. Every medium-emphasis button takes `.bill-flip`, which mirrors the cut (`--bill-button-radius-flip`), so a pair beside a solid button is book-matched. Remove the class from a button to give it the normal cut. Lines carry the form language: a 3px double outline in spot ink inset `clamp(.4rem, 1.2vw, .9rem)` from the card's edge, 1px spot rules either side of section heads and the dateline, a 1px border plus an inset 1px outline (5px in) for the Today box, 1px hairlines around plates, and 2px dotted leaders. The current nav link is marked with a 2px printed underline offset 0.45em, not a color change.

## Components

### Buttons
Slips of copper or ink, set in letterspaced capitals.
- **Shape:** a leaf cut (`.6em .12em / .42em .12em`), in em so the small top-bar button scales with it.
- **Primary:** copper fill with card-stock text, 700 text-sm caps at 0.1em, padding 0.9em by 1.6em. Used for Book a table on the masthead.
- **Hover / Focus:** fill deepens to Deep Spot; focus ring in spot ink.
- **Outline (medium emphasis):** transparent with a black-ink border and text, a 7% ink tint on hover. Used for See the menu, See the full menu, Get directions.
- **Cover button:** in the top bar, Book a table is a small (0.6em by 1.2em, 0.72rem) bright copper slip with cover-colored text.

### Cards / Containers
- **The card:** white stock, square, framed by the inset double rule in spot ink at 30%, fades in and rises 0.75rem on load through Yeti's `.enter` (0.9s, `cubic-bezier(.16, 1, .3, 1)`), only when reduced motion is not requested.
- **The Today box:** specials only. A warm paper tint (6% spot ink in card stock) with 8px corners, the same curve as a button's swept corner, and no border. A single 1px outline sits 6px inside the edge, in spot ink at 30%, kept faint on purpose so the eye goes to the food and not the frame. Padding is `clamp(1.25rem, 3vw, 2.25rem)` with 1.25rem extra on top. The head is in ink with copper rules, specials sit in a two-up grid, and photos keep white mats. A 3.5rem copper thistle (`.bill-seal`) sits upright in a gap in the top edge. Hidden when no special is current.
- **Shadow Strategy:** none (see Elevation & Depth).

### Navigation

The logo is a thistle in `builder/partials/logo.twig`: one-color SVG, 2.5rem tall, in `copper-cover`, with its scales cut out as negative space. In the top bar it is lifted 10% so the thistle's head, not its box, sits on the line of the name and links. A page that shows it twice passes a different `logoId`. The links fold behind the menu button under 48rem (`data-threshold="lg"`), because the logo, name, links and button need that width on one line.
- **Style:** cover-colored bar with light text. Brand at the left in condensed 800 caps; links in 600 text-sm caps at 0.12em; a 12% light tint on hover; the current page underlined 2px. On a phone the links open in a cover-colored popover with a close button; Book a table stays in the bar.

### Dateline (signature)
Today's date and open hours, computed on each visit from the Hours record, set in 600 text-sm caps at 0.16em between two 1px spot rules that draw outward from the center once on load (1.1s, 0.15s delay). Says "Closed today" on a closed day.

### Menu line (signature)
Dish name (Title), a 2px dotted leader at 40% ink raised 0.3em to the baseline, and a 700 tabular price, aligned on the last baseline. Description below in body text, then dietary notes in Label style in faded ink, joined by middots.

### Plate
A figure with a stock margin of `clamp(.3rem, .8vw, .55rem)` (0.25rem for featured thumbnails on a phone) inside a 1px hairline. With no photo uploaded, it holds a flat panel of spot ink at 14% on stock.

### Hours list
One row per day: day, dotted leader, hours. Today's row is 700 in spot ink, with its leader in spot ink too.

### Footer (back cover)
Sits on the cover with no card. The footer sets `color-scheme: dark`, because the cover is dark in both modes, so every ink takes its dark value without being remapped. Heads are text-sm in the section-head style.

## Do's and Don'ts

### Do:
- **Do** derive every color from the four dials through the `light-dark()` OKLCH formulas, so light and dark mode follow a rebrand.
- **Do** keep the card to two inks plus copper hardware: Press Black and Evergreen Spot Ink on Card Stock, with copper only on the logo, rules, Book a table and today's hours row.
- **Do** use spot ink for the masthead, and spot ink at 30% for the card's frame and the Today box's line.
- **Do** set priced lines as name, dotted leader, tabular price.
- **Do** set section heads as wide letterspaced caps centered between two 1px spot rules.
- **Do** print photos as square plates with a stock margin and a hairline border.
- **Do** keep motion to the single print-in on load, and only when reduced motion is not requested.

### Don't:
- **Don't** round corners on cards, buttons, plates or images.
- **Don't** add shadows, blur, glassmorphism or gradient heroes; depth is paper on cover.
- **Don't** add a fourth color, or spend copper on the restaurant name, text or large areas.
- **Don't** go fine-dining luxe: no black and gold, no hairline-weight type.
- **Don't** go chain-restaurant loud: no saturated red and yellow, promo banners, starbursts or coupon badges. Dietary notes stay as small capitals, not pill badges.
- **Don't** build grids of icon tiles.
- **Don't** add a second typeface; get contrast from Archivo's width, weight and tracking.

### Open items (known gaps in the shipped build, not rules)
- On a phone the dateline's spot rules shrink to short stubs (1.25rem minimum) beside the stacked date and hours.
- Dish names are set in full caps, not true small caps as the direction intended.

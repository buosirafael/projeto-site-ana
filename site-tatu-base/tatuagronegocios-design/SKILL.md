---
name: tatuagronegocios-design
description: Design system skill for tatuagronegocios. Activate when building UI components, pages, or any visual elements. Provides exact color tokens, typography scale, spacing grid, component patterns, and craft rules. Read references/DESIGN.md before writing any CSS or JSX.
---

# tatuagronegocios Design System

You are building UI for **tatuagronegocios**. Dark-themed, cool palette, sans-serif typography (Times), compact density on a 4px grid, expressive motion.

## Visual Reference

**IMPORTANT**: Study ALL screenshots below before writing any UI. Match colors, typography, spacing, layout, and motion exactly as shown.

### Homepage

![tatuagronegocios Homepage](screenshots/homepage.png)

> Read `references/DESIGN.md` for full token details.

## Design Philosophy

- **Layered depth** — use shadow tokens to create a sense of physical layering. Each elevation level has a specific shadow.
- **Gradient accents** — gradients are used thoughtfully for emphasis, not decoration.
- **Type pairing** — Times for body/UI text, object-fit: contain for headings/display. Never introduce a third typeface.
- **compact density** — 4px base grid. Every dimension is a multiple of 4.
- **cool palette** — the color temperature runs cool, matching the sans-serif typography.
- **Restrained accent** — `#005bd1` is the only pop of color. Used exclusively for CTAs, links, focus rings, and active states.
- **Expressive motion** — animations are an integral part of the experience. Use spring physics and layout animations.

## Color System

### Core Palette

| Role | Token | Hex | Use |
|------|-------|-----|-----|
| Background | `--background` | `#121212` | Page/app background |
| Surface | `--surface` | `#362413` | Cards, panels, modals |
| Text Primary | `--text-primary` | `#ffffff` | Headings, body text |
| Text Muted | `--text-muted` | `#666666` | Captions, placeholders |
| Accent | `--accent` | `#005bd1` | CTAs, links, focus rings |
| Border | `--border` | `#1c1c1c` | Dividers, card borders |

### Status Colors

| Status | Hex | Use |
|--------|-----|-----|
| Success | `#097a5e` | Confirmations, positive trends |
| Warning | `#f79e1b` | Caution states, pending items |
| Danger | `#ec2a7b` | Errors, destructive actions |

### Extended Palette

- **gradient-background:** `#000000` — Gradient stop for decorative background or accent
- `#333333`
- `#0000ee`
- **gradient-background:** `#f5f5f5` — Gradient stop for decorative background or accent
- `#142fbd`
- `#999999`
- `#e74c3c` — Warm accent — hover glow or decorative highlight
- `#707070`

### CSS Variable Tokens

```css
--alpha-button-background: 1;
--alpha-button-border: 1;
--alpha-badge-border: .1;
--border-radius: var(--product-card-corner-radius);
--border-width: var(--product-card-border-width);
--border-opacity: var(--product-card-border-opacity);
--border-radius: var(--collection-card-corner-radius);
--border-width: var(--collection-card-border-width);
--border-opacity: var(--collection-card-border-opacity);
--border-radius: var(--blog-card-corner-radius);
--border-width: var(--blog-card-border-width);
--border-opacity: var(--blog-card-border-opacity);
--border-radius: var(--text-boxes-radius);
--border-width: var(--text-boxes-border-width);
--border-opacity: var(--text-boxes-border-opacity);
--border-radius: var(--media-radius);
--border-width: var(--media-border-width);
--border-opacity: var(--media-border-opacity);
--alpha-button-background: 0;
--alpha-button-border: .2;
```

## Typography

### Font Stack

- **Times** — Heading 1, Heading 2, Heading 3
- **object-fit: contain** — Body, Caption

### Font Sources

```css
@font-face {
  font-family: "Poppins";
  src: url("fonts/Poppins-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Poppins";
  src: url("fonts/Poppins-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Open Sans";
  src: url("fonts/OpenSans-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Open Sans";
  src: url("fonts/OpenSans-Regular.ttf") format("truetype");
  font-weight: 400;
}
```

### Type Scale

| Role | Family | Size | Weight |
|------|--------|------|--------|
| Heading 1 | Times | calc(var(--font-heading-scale)*6.2rem) | 700 |
| Heading 2 | Times | clamp(calc(var(--font-heading-scale)*5.6rem),14vw,calc(var(--font-heading-scale)*7.2rem)) | 700 |
| Heading 3 | Times | calc(var(--font-heading-scale)*5.2rem) | 700 |
| Body | object-fit: contain | 1.4rem | 400 |
| Caption | object-fit: contain | 1.2rem | 400 |

### Typography Rules

- Body/UI: **Times**, Headings: **object-fit: contain** — these are the only display fonts
- Max 3-4 font sizes per screen
- Headings: weight 600-700, body: weight 400
- Use color and opacity for text hierarchy, not additional font sizes
- Line height: 1.5 for body, 1.2 for headings

## Spacing & Layout

### Base Grid: 4px

Every dimension (margin, padding, gap, width, height) must be a multiple of **4px**.

### Spacing Scale

`2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24` px

### Spacing as Meaning

| Spacing | Use |
|---------|-----|
| 4-8px | Tight: related items (icon + label, avatar + name) |
| 12-16px | Medium: between groups within a section |
| 24-32px | Wide: between distinct sections |
| 48px+ | Vast: major page section breaks |

### Border Radius

Scale: `.25rem, .4rem, 1.61875px, 1.88906px, 2.6rem, 4px, 8px, 10px, 12px, 12px 0px 0px 12px, 20px, 25px, 27px, 40px, 50px, 100%, 999px`
Default: `12px`

### Container

Max-width: `990px`, centered with auto margins.

### Breakpoints

| Name | Value |
|------|-------|
| md | 749px |
| md | 750px |
| md | 768px |
| lg | 900px |
| lg | 989px |
| lg | 990px |
| 2xl | 1400px |

Mobile-first: design for small screens, layer on responsive overrides.

## Component Patterns

### Card

```css
.card {
  background: #362413;
  border: 1px solid #1c1c1c;
  border-radius: 12px;
  padding: 16px;
  box-shadow: var(--popup-shadow-horizontal-offset) var(--popup-shadow-vertical-offset) var(--popup-shadow-blur-radius) rgba(var(--color-shadow),var(--popup-shadow-opacity));
}
```

```html
<div class="card">
  <h3>Card Title</h3>
  <p>Card content goes here.</p>
</div>
```

### Button

```css
/* Primary */
.btn-primary {
  background: #005bd1;
  color: #ffffff;
  border-radius: 12px;
  padding: 8px 16px;
  font-weight: 500;
  transition: opacity 150ms ease;
}
.btn-primary:hover { opacity: 0.9; }

/* Ghost */
.btn-ghost {
  background: transparent;
  border: 1px solid #1c1c1c;
  color: #ffffff;
  border-radius: 12px;
  padding: 8px 16px;
}
```

```html
<button class="btn-primary">Get Started</button>
<button class="btn-ghost">Learn More</button>
```

### Input

```css
.input {
  background: #121212;
  border: 1px solid #1c1c1c;
  border-radius: 12px;
  padding: 8px 12px;
  color: #ffffff;
  font-size: 14px;
}
.input:focus { border-color: #005bd1; outline: none; }
```

```html
<input class="input" type="text" placeholder="Search..." />
```

### Badge / Chip

```css
.badge {
  display: inline-flex;
  align-items: center;
  padding: 4px 8px;
  border-radius: 9999px;
  font-size: 12px;
  font-weight: 500;
  background: #362413;
  color: #666666;
}
```

```html
<span class="badge">New</span>
<span class="badge">Beta</span>
```

### Modal / Dialog

```css
.modal-backdrop { background: rgba(0, 0, 0, 0.6); }
.modal {
  background: #362413;
  border: 1px solid #1c1c1c;
  border-radius: 999px;
  padding: 24px;
  max-width: 480px;
  width: 90vw;
  box-shadow: 0 2px 12px #0000000f;
}
```

```html
<div class="modal-backdrop">
  <div class="modal">
    <h2>Dialog Title</h2>
    <p>Dialog content.</p>
    <button class="btn-primary">Confirm</button>
    <button class="btn-ghost">Cancel</button>
  </div>
</div>
```

### Table

```css
.table { width: 100%; border-collapse: collapse; }
.table th {
  text-align: left;
  padding: 8px 12px;
  font-weight: 500;
  font-size: 12px;
  color: #666666;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  border-bottom: 1px solid #1c1c1c;
}
.table td {
  padding: 12px;
  border-bottom: 1px solid #1c1c1c;
}
```

```html
<table class="table">
  <thead><tr><th>Name</th><th>Status</th><th>Date</th></tr></thead>
  <tbody>
    <tr><td>Item One</td><td>Active</td><td>Jan 1</td></tr>
    <tr><td>Item Two</td><td>Pending</td><td>Jan 2</td></tr>
  </tbody>
</table>
```

### Navigation

```css
.nav {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 12px 16px;
  border-bottom: 1px solid #1c1c1c;
}
.nav-link {
  color: #666666;
  padding: 8px 12px;
  border-radius: 12px;
  transition: color 150ms;
}
.nav-link:hover { color: #ffffff; }
.nav-link.active { color: #005bd1; }
```

```html
<nav class="nav">
  <a href="/" class="nav-link active">Home</a>
  <a href="/about" class="nav-link">About</a>
  <a href="/pricing" class="nav-link">Pricing</a>
  <button class="btn-primary" style="margin-left: auto">Get Started</button>
</nav>
```

### Extracted Components

These components were found in the codebase:

**Button** (`html`)

**Card** (`html`)
- Variants: `-collection`, `-standard`, `wrapper`, `-media`, `-text`

**Navigation** (`html`)

**Badge** (`html`)

**Modal** (`html`)

**List** (`html`)

## Page Structure

The following page sections were detected:

- **Navigation** — Top navigation bar (9 items)
- **Hero** — Hero/banner section with headline and CTAs
- **Faq** — FAQ/accordion section
- **Footer** — Page footer with links and info (8 items)
- **Cards** — Grid of 81 card elements (81 items)

When building pages, follow this section order and structure.

## Animation & Motion

This project uses **expressive motion**. Animations are part of the design language.

### CSS Animations

- `translateAnnouncementSlideIn`
- `translateAnnouncementSlideOut`
- `animateMenuOpen`
- `animateAmbient`
- `slideIn`

### Motion Tokens

- **Duration scale:** `0ms`, `100ms`, `150ms`, `200ms`, `300ms`, `400ms`, `6000ms`
- **Easing functions:** `ease`, `ease-in-out`, `cubic-bezier(.25,.46,.45,.94)`, `ease-out`, `cubic-bezier(.52,0,.61,.99)`, `linear`, `cubic-bezier(.29,.63,.44,1)`
- **Animated properties:** `opacity`, `visibility`

### Motion Guidelines

- **Duration:** Use values from the duration scale above. Short (0ms) for micro-interactions, long (6000ms) for page transitions
- **Easing:** Use `ease` as the default easing curve
- **Direction:** Elements enter from bottom/right, exit to top/left
- **Reduced motion:** Always respect `prefers-reduced-motion` — disable animations when set

## Depth & Elevation

### Shadow Tokens

- Subtle: `0 0 0 calc(var(--buttons-border-width) + var(--border-offset)) rgba(var(--color-button-text),var(--border-opacity)),0 0 0 calc(var(--buttons-border-width) + 1px) rgba(var(--color-button),var(--alpha-button-background))`
- Subtle: `0 1px 2px #0003`
- Subtle: `0 0 2px #00000047`
- Subtle: `rgb(222, 222, 222) 0px 0px 0px 1px inset`
- Subtle: `rgb(0, 91, 209) 0px 0px 0px 1px`
- Raised (cards, buttons): `var(--popup-shadow-horizontal-offset) var(--popup-shadow-vertical-offset) var(--popup-shadow-blur-radius) rgba(var(--color-shadow),var(--popup-shadow-opacity))`

### Z-Index Scale

`0, 1, 2, 3, 4, 5, 9, 99, 100, 101, 1000, 9999, 99999, 99999999`

Use these exact values — never invent z-index values.

## Anti-Patterns (Never Do)

- **No blur effects** — no backdrop-blur, no filter: blur()
- **No zebra striping** — tables and lists use borders for separation
- **No invented colors** — every hex value must come from the palette above
- **No arbitrary spacing** — every dimension is a multiple of 4px
- **No extra fonts** — only Times and object-fit: contain are allowed
- **No arbitrary border-radius** — use the scale: .25rem, .4rem, 1.61875px, 1.88906px, 2.6rem, 4px, 8px, 10px, 12px, 20px
- **No opacity for disabled states** — use muted colors instead

## Workflow

1. **Read** `references/DESIGN.md` before writing any UI code
2. **Pick colors** from the Color System section — never invent new ones
3. **Set typography** — Times, object-fit: contain only, using the type scale
4. **Build layout** on the 4px grid — check every margin, padding, gap
5. **Match components** to patterns above before creating new ones
6. **Apply elevation** — use shadow tokens
7. **Validate** — every value traces back to a design token. No magic numbers.

## Brand Spec

- **Favicon:** `//tatuagronegocios.com.br/cdn/shop/files/fav.png`
- **Site URL:** `https://tatuagronegocios.com.br/`
- **Brand color:** `#005bd1`
- **Brand typeface:** Times

## Quick Reference

```
Background:     #121212
Surface:        #362413
Text:           #ffffff / #666666
Accent:         #005bd1
Border:         #1c1c1c
Font:           Times
Spacing:        4px grid
Radius:         12px
Components:     10 detected
```

## When to Trigger

Activate this skill when:
- Creating new components, pages, or visual elements for tatuagronegocios
- Writing CSS, Tailwind classes, styled-components, or inline styles
- Building page layouts, templates, or responsive designs
- Reviewing UI code for design consistency
- The user mentions "tatuagronegocios" design, style, UI, or theme
- Generating mockups, wireframes, or visual prototypes

---

# Full Reference Files

> Every output file is embedded below. Claude has full design system context from /skills alone.

## Design System Tokens (DESIGN.md)

# tatuagronegocios DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 2 · Components: 10
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![tatuagronegocios Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a cool tone. Depth is expressed through layered shadows and subtle surface color variation. Typography pairs **object-fit: contain** for display/headings with **Times** for body text, creating clear visual hierarchy through type contrast. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 14, 16px. The accent color **#005bd1** anchors interactive elements (buttons, links, focus rings). Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| background | `#121212` | background | Page background, darkest surface |
| gradient-background | `#362413` | surface | Card and panel backgrounds |
| gradient-background | `#ffffff` | text-primary | Headings and body text |
| text-muted | `#666666` | text-muted | Captions, placeholders, secondary info |
| border | `#1c1c1c` | border | Dividers, card borders, outlines |
| accent | `#005bd1` | accent | CTAs, links, focus rings, active states |
| danger | `#ec2a7b` | danger | Error states, destructive actions |
| gradient-background | `#097a5e` | success | Success states, positive indicators |
| warning | `#f79e1b` | warning | Warning states, caution indicators |
| info | `#0000ee` | info | Informational highlights |
| gradient-background | `#000000` | unknown | Palette color |
| unknown | `#333333` | unknown | Palette color |
| gradient-background | `#f5f5f5` | unknown | Palette color |
| unknown | `#142fbd` | unknown | Palette color |
| unknown | `#999999` | unknown | Palette color |
| unknown | `#e74c3c` | unknown | Palette color |
| unknown | `#707070` | unknown | Palette color |
| unknown | `#0071ce` | unknown | Palette color |
| unknown | `#eb001b` | unknown | Palette color |
| unknown | `#ff5f00` | unknown | Palette color |

### CSS Variable Tokens

```css
--alpha-button-background: 1;
--alpha-button-border: 1;
--alpha-badge-border: .1;
--border-radius: var(--product-card-corner-radius);
--border-width: var(--product-card-border-width);
--border-opacity: var(--product-card-border-opacity);
--border-radius: var(--collection-card-corner-radius);
--border-width: var(--collection-card-border-width);
--border-opacity: var(--collection-card-border-opacity);
--border-radius: var(--blog-card-corner-radius);
--border-width: var(--blog-card-border-width);
--border-opacity: var(--blog-card-border-opacity);
--border-radius: var(--text-boxes-radius);
--border-width: var(--text-boxes-border-width);
--border-opacity: var(--text-boxes-border-opacity);
--border-radius: var(--media-radius);
--border-width: var(--media-border-width);
--border-opacity: var(--media-border-opacity);
--alpha-button-background: 0;
--alpha-button-border: .2;
```


---

## 3. Typography Rules

**Font Stack:**
- **Times** — Heading 1, Heading 2, Heading 3
- **object-fit: contain** — Body, Caption

**Font Sources:**

```css
@font-face {
  font-family: "Poppins";
  src: url("https://tatuagronegocios.com.br/cdn/fonts/poppins/poppins_n4.0ba78fa5af9b0e1a374041b3ceaadf0a43b41362.woff2") format("woff2");
  font-weight: 400;
}
@font-face {
  font-family: "Poppins";
  src: url("https://tatuagronegocios.com.br/cdn/fonts/poppins/poppins_n7.56758dcf284489feb014a026f3727f2f20a54626.woff2") format("woff2");
  font-weight: 700;
}
@font-face {
  font-family: "Open Sans";
  src: url("https://tatuagronegocios.com.br/cdn/fonts/open_sans/opensans_n4.c32e4d4eca5273f6d4ee95ddf54b5bbb75fc9b61.woff2") format("woff2");
  font-weight: 400;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Times | calc(var(--font-heading-scale)*6.2rem) | 700 |
| Heading 2 | Times | clamp(calc(var(--font-heading-scale)*5.6rem),14vw,calc(var(--font-heading-scale)*7.2rem)) | 700 |
| Heading 3 | Times | calc(var(--font-heading-scale)*5.2rem) | 700 |
| Body | object-fit: contain | 1.4rem | 400 |
| Caption | object-fit: contain | 1.2rem | 400 |

**Typographic Rules:**
- Limit to 2 font families max per screen
- Use **Times** for body/UI text, **object-fit: contain** for display/headings
- Maintain consistent hierarchy: no more than 3-4 font sizes per screen
- Headings use bold (600-700), body uses regular (400)
- Line height: 1.5 for body text, 1.2 for headings
- Use color and opacity for secondary hierarchy, not additional font sizes


---

## 4. Component Stylings

### Layout (1)

**Footer** — `html`

### Navigation (1)

**Navigation** — `html`

### Data Display (3)

**Card** — `html`
- Variants: `-collection`, `-standard`, `wrapper`, `-media`, `-text`

**Badge** — `html`

**List** — `html`

### Data Input (2)

**Button** — `html`
- Animation: 

**Input** — `html`
- State: :focus, :placeholder

### Overlay (1)

**Modal** — `html`

### Media (2)

**Image** — `html`

**Icon** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24
- **Border radius:** .25rem, .4rem, 1.61875px, 1.88906px, 2.6rem, 4px, 8px, 10px, 12px, 12px 0px 0px 12px, 20px, 25px, 27px, 40px, 50px, 100%, 999px
- **Max content width:** 990px

**Spacing as Meaning:**
| Spacing | Use |
|---|---|
| 4-8px | Tight: related items within a group |
| 12-16px | Medium: between groups |
| 24-32px | Wide: between sections |
| 48px+ | Vast: major section breaks |


---

## 6. Depth & Elevation

### Flat — subtle depth hints

- `0 0 0 calc(var(--buttons-border-width) + var(--border-offset)) rgba(var(--color-button-text),var(--border-opacity)),0 0 0 calc(var(--buttons-border-width) + 1px) rgba(var(--color-button),var(--alpha-button-background))`
- `0 1px 2px #0003`
- `0 0 2px #00000047`

### Raised — cards, buttons, interactive elements

- `var(--popup-shadow-horizontal-offset) var(--popup-shadow-vertical-offset) var(--popup-shadow-blur-radius) rgba(var(--color-shadow),var(--popup-shadow-opacity))`
- `inherit`
- `0 0 .2rem rgba(var(--color-foreground),.3),var(--popup-shadow-horizontal-offset) var(--popup-shadow-vertical-offset) var(--popup-shadow-blur-radius) rgba(var(--color-shadow),var(--popup-shadow-opacity))`

### Floating — dropdowns, popovers, modals

- `0 2px 12px #0000000f`
- `0 2px 12px #0000000a`
- `-2px 0 10px rgba(0,0,0,0.1)`

### Z-Index Scale

`0, 1, 2, 3, 4, 5, 9, 99, 100, 101, 1000, 9999, 99999, 99999999`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes translateAnnouncementSlideIn`
- `@keyframes translateAnnouncementSlideOut`
- `@keyframes animateMenuOpen`
- `@keyframes animateAmbient`
- `@keyframes slideIn`
- `@keyframes fadeIn`
- `@keyframes rotator`
- `@keyframes dash`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#005bd1` for interactive elements (buttons, links, focus rings)
- Use `#121212` as the primary page background
- Pair **Times** (body) with **object-fit: contain** (display) — these are the only allowed fonts
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: .25rem, .4rem, 1.61875px, 1.88906px, 2.6rem
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't introduce additional font families beyond Times and object-fit: contain
- Don't use arbitrary spacing values — stick to multiples of 4px
- Don't create custom box-shadow values outside the system tokens
- Don't use arbitrary border-radius values — pick from the defined scale
- Don't duplicate component patterns — check Section 4 first
- Don't use backdrop-blur or blur effects

### Anti-Patterns (detected from codebase)

- No blur or backdrop-blur effects
- No zebra striping on tables/lists


---

## 9. Responsive Behavior

| Name | Value | Source |
|---|---|---|
| md | 749px | css |
| md | 750px | css |
| md | 768px | css |
| lg | 900px | css |
| lg | 989px | css |
| lg | 990px | css |
| 2xl | 1400px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #362413
Border: 1px solid #1c1c1c
Radius: 12px
Padding: 16px
Font: Times
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg #005bd1, text white
Ghost: bg transparent, border #1c1c1c
Padding: 8px 16px
Radius: 12px
Hover: opacity 0.9 or lighter shade
Focus: ring with #005bd1
```

### Build a Page Layout

```
Background: #121212
Max-width: 990px, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #362413
Label: #666666 (muted, 12px, uppercase)
Value: #ffffff (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #121212
Input border: 1px solid #1c1c1c
Focus: border-color #005bd1
Label: #666666 12px
Spacing: 16px between fields
Radius: 12px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Times, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```

## Bundled Fonts (fonts/)

The following font files are bundled in the `fonts/` directory:

- `fonts/OpenSans-Bold.ttf`
- `fonts/OpenSans-ExtraBold.ttf`
- `fonts/OpenSans-Light.ttf`
- `fonts/OpenSans-Medium.ttf`
- `fonts/OpenSans-Regular.ttf`
- `fonts/OpenSans-SemiBold.ttf`
- `fonts/Poppins-Black.ttf`
- `fonts/Poppins-Bold.ttf`
- `fonts/Poppins-ExtraBold.ttf`
- `fonts/Poppins-ExtraLight.ttf`
- `fonts/Poppins-Light.ttf`
- `fonts/Poppins-Medium.ttf`
- `fonts/Poppins-Regular.ttf`
- `fonts/Poppins-SemiBold.ttf`
- `fonts/Poppins-Thin.ttf`

Use these local font files in `@font-face` declarations instead of fetching from Google Fonts.

## Homepage Screenshots (screenshots/)

![homepage.png](screenshots/homepage.png)


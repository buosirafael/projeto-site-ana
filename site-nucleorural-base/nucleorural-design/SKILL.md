---
name: nucleorural-design-design
description: Design system skill for nucleorural-design. Activate when building UI components, pages, or any visual elements. Provides exact color tokens, typography scale, spacing grid, component patterns, and craft rules. Read references/DESIGN.md before writing any CSS or JSX. Includes ultra-mode visual journey: read references/ANIMATIONS.md, references/LAYOUT.md, references/COMPONENTS.md, and references/INTERACTIONS.md for full motion and layout details.
---

# nucleorural-design Design System

You are building UI for **nucleorural-design**. Light-themed, cool palette, sans-serif typography (Pe-icon-7-stroke), standard density on a 5px grid, expressive motion.

## Visual Reference

**IMPORTANT**: Study ALL screenshots below before writing any UI. Match colors, typography, spacing, layout, and motion exactly as shown.

### Homepage

![nucleorural-design Homepage](screenshots/homepage.png)

### Scroll Journey (Cinematic Visual States)

> These screenshots capture the website at different scroll depths. The design changes dramatically as you scroll — each frame shows a different cinematic state. Replicate these exact visual transitions.

#### 0% — Hero / Above the fold

![Scroll 0%](screens/scroll/scroll-000.png)

#### 17% — Mid-page at 17% scroll

![Scroll 17%](screens/scroll/scroll-017.png)

#### 33% — Mid-page at 33% scroll

![Scroll 33%](screens/scroll/scroll-033.png)

#### 50% — Mid-page at 50% scroll

![Scroll 50%](screens/scroll/scroll-050.png)

#### 67% — Mid-page at 67% scroll

![Scroll 67%](screens/scroll/scroll-067.png)

#### 83% — Mid-page at 83% scroll

![Scroll 83%](screens/scroll/scroll-083.png)

#### 100% — Footer / End of page

![Scroll 100%](screens/scroll/scroll-100.png)

> Read `references/DESIGN.md` for full token details. Read `references/ANIMATIONS.md` for motion specs. Read `references/LAYOUT.md` for layout structure. Read `references/COMPONENTS.md` for component patterns.

## Ultra Reference Files

This package includes extended documentation. **Read these files before implementing:**

| File | Contents |
|------|----------|
| `references/DESIGN.md` | Full design system tokens, colors, typography, spacing |
| `references/VISUAL_GUIDE.md` | **START HERE** — Master visual guide with all screenshots embedded |
| `references/ANIMATIONS.md` | CSS keyframes, scroll triggers, motion library stack, video specs |
| `references/LAYOUT.md` | Flex/grid containers, page structure, spacing relationships |
| `references/COMPONENTS.md` | DOM component patterns, HTML structure, class fingerprints |
| `references/INTERACTIONS.md` | Hover/focus states with before/after style diffs |
| `screens/scroll/` | 7 scroll journey screenshots showing cinematic states |

## Design Philosophy

- **Layered depth** — use shadow tokens to create a sense of physical layering. Each elevation level has a specific shadow.
- **Gradient accents** — gradients are used thoughtfully for emphasis, not decoration.
- **Type pairing** — Pe-icon-7-stroke for body/UI text, AgrikoleIcons for headings/display. Never introduce a third typeface.
- **standard density** — 5px base grid. Every dimension is a multiple of 5.
- **cool palette** — the color temperature runs cool, matching the sans-serif typography.
- **Restrained accent** — `#00d084` is the only pop of color. Used exclusively for CTAs, links, focus rings, and active states.
- **Expressive motion** — animations are an integral part of the experience. Use spring physics and layout animations.

## Color System

### Core Palette

| Role | Token | Hex | Use |
|------|-------|-----|-----|
| Background | `--background` | `#ffffff` | Page/app background |
| Surface | `--surface` | `#f5f0e9` | Cards, panels, modals |
| Text Primary | `--text-primary` | `#043038` | Headings, body text |
| Text Muted | `--text-muted` | `#878986` | Captions, placeholders |
| Accent | `--accent` | `#00d084` | CTAs, links, focus rings |
| Border | `--border` | `#404a3d` | Dividers, card borders |

### Status Colors

| Status | Hex | Use |
|--------|-----|-----|
| Success | `#83c75d` | Confirmations, positive trends |
| Warning | `#eddd5e` | Caution states, pending items |
| Danger | `#ff4539` | Errors, destructive actions |

### Extended Palette

- `#5b8c51`
- `#c5c9c4`
- **wp--preset--color--black:** `#000000` — Deep background layer or shadow color
- `#313131`
- **wp-editor-canvas-background:** `#dddddd`
- `#128c7e`
- **wp--preset--color--vivid-cyan-blue:** `#0693e3`
- **wndb--color--primary:** `#0000ff`

### CSS Variable Tokens

```css
--wp-editor-canvas-background: #ddd;
--wp-admin-border-width-focus: 2px;
--wp-admin-border-width-focus: 1.5px;
--wndb--color--borders: var(--wndb--color--subtle);
--wndb--border--radius--sm: 0.25rem;
--wndb--border--radius--md: 0.5rem;
--wndb--border--radius--lg: 0.75rem;
--wndb--border--radius--xl: 1rem;
--wndb--border--radius: 0;
--wndb--border--radius: var(--wndb--border--radius--sm);
--wndb--border--radius: var(--wndb--border--radius--md);
--wndb--border--radius: var(--wndb--border--radius--lg);
--wndb--border--radius: var(--wndb--border--radius--xl);
--wndb--border--radius: 9999px;
--wndb--color--primary: #00f;
--wndb--color--secondary: #00f;
--wndb--color--borders: var(--wndb-gray-150);
--wndb--color--borders-light: var(--wndb-gray-100);
--wndb--color--borders-strong: var(--wndb--color--text--faded);
--wndb--color--borders: var(--wndb-gray-150);
```

## Typography

### Font Stack

- **Pe-icon-7-stroke** — Heading 1, Heading 2, Heading 3
- **AgrikoleIcons** — Body, Caption

### Font Sources

```css
@font-face {
  font-family: "Montserrat";
  src: url("fonts/Montserrat-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Montserrat";
  src: url("fonts/Montserrat-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Barlow";
  src: url("fonts/Barlow-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Barlow";
  src: url("fonts/Barlow-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Roboto";
  src: url("fonts/Roboto-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Roboto";
  src: url("fonts/Roboto-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "AgrikoleIcons";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "Pe-icon-7-stroke";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.eot?d7yf1v");
  font-weight: 400;
}
@font-face {
  font-family: "ElegantIcons";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "vcpb-plugin-icons";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "vc_grid_v1";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.eot?-9hbgac");
  font-weight: 400;
}
@font-face {
  font-family: "Core Icon";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.eot?d7yf1v");
  font-weight: 400;
}
@font-face {
  font-family: "ytpregular";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../../../../../plugins/wprt-addons/assets/font/ytp-regular.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "revicons";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.eot?5510888") format("embedded-opentype");
  font-weight: 400;
}
```

### Type Scale

| Role | Family | Size | Weight |
|------|--------|------|--------|
| Heading 1 | Pe-icon-7-stroke | 70px | 700 |
| Heading 2 | Pe-icon-7-stroke | 50px | 700 |
| Heading 3 | Pe-icon-7-stroke | 40px | 700 |
| Body | AgrikoleIcons | 16px | 400 |
| Caption | AgrikoleIcons | 18px | 400 |

### Typography Rules

- Body/UI: **Pe-icon-7-stroke**, Headings: **AgrikoleIcons** — these are the only display fonts
- Max 3-4 font sizes per screen
- Headings: weight 600-700, body: weight 400
- Use color and opacity for text hierarchy, not additional font sizes
- Line height: 1.5 for body, 1.2 for headings

## Spacing & Layout

### Base Grid: 5px

Every dimension (margin, padding, gap, width, height) must be a multiple of **5px**.

### Spacing Scale

`5, 10, 15, 20, 25, 30, 35, 40, 50, 60, 70, 80` px

### Spacing as Meaning

| Spacing | Use |
|---------|-----|
| 2.5-5px | Tight: related items within a group |
| 10px | Medium: between groups |
| 15-20px | Wide: between sections |
| 30px+ | Vast: major section breaks |

### Border Radius

Scale: `0px 0px 5px, 0px 0px 5px 5px, 0px 5px 0px 0px, .5rem, 2px, 3px, 4px, 5px, 8px, 22px, 24px, 26px, 30px, 32px, 100%, 999px`
Default: `8px`

### Container

Max-width: `1024px`, centered with auto margins.

### Breakpoints

| Name | Value |
|------|-------|
| sm | 600px |
| md | 767px |
| md | 768px |
| lg | 782px |
| lg | 991px |
| lg | 992px |
| lg | 1024px |
| xl | 1025px |
| xl | 1199px |
| xl | 1200px |
| xl | 1230px |
| 2xl | 1440px |

Mobile-first: design for small screens, layer on responsive overrides.

## Component Patterns

### Card

```css
.card {
  background: #f5f0e9;
  border: 1px solid #404a3d;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2.5em 0-1.3em rgba(235,235,235,.75);
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
  background: #00d084;
  color: #043038;
  border-radius: 8px;
  padding: 10px 20px;
  font-weight: 500;
  transition: opacity 150ms ease;
}
.btn-primary:hover { opacity: 0.9; }

/* Ghost */
.btn-ghost {
  background: transparent;
  border: 1px solid #404a3d;
  color: #043038;
  border-radius: 8px;
  padding: 10px 20px;
}
```

```html
<button class="btn-primary">Get Started</button>
<button class="btn-ghost">Learn More</button>
```

### Input

```css
.input {
  background: #ffffff;
  border: 1px solid #404a3d;
  border-radius: 8px;
  padding: 10px 15px;
  color: #043038;
  font-size: 14px;
}
.input:focus { border-color: #00d084; outline: none; }
```

```html
<input class="input" type="text" placeholder="Search..." />
```

### Badge / Chip

```css
.badge {
  display: inline-flex;
  align-items: center;
  padding: 5px 10px;
  border-radius: 9999px;
  font-size: 12px;
  font-weight: 500;
  background: #f5f0e9;
  color: #878986;
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
  background: #f5f0e9;
  border: 1px solid #404a3d;
  border-radius: 999px;
  padding: 30px;
  max-width: 480px;
  width: 90vw;
  box-shadow: 0 15px 15px 0 rgba(0,0,0,.03);
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
  padding: 10px 15px;
  font-weight: 500;
  font-size: 12px;
  color: #878986;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  border-bottom: 1px solid #404a3d;
}
.table td {
  padding: 15px;
  border-bottom: 1px solid #404a3d;
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
  gap: 10px;
  padding: 15px 20px;
  border-bottom: 1px solid #404a3d;
}
.nav-link {
  color: #878986;
  padding: 10px 15px;
  border-radius: 8px;
  transition: color 150ms;
}
.nav-link:hover { color: #043038; }
.nav-link.active { color: #00d084; }
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

**Input** (`html`)

## Page Structure

The following page sections were detected:

- **Navigation** — Top navigation bar (5 items)
- **Hero** — Hero section (detected from heading structure)
- **Footer** — Page footer with links and info (11 items)
- **Stats** — Statistics/metrics display

When building pages, follow this section order and structure.

## Animation & Motion

This project uses **expressive motion**. Animations are part of the design language.

### CSS Animations

- `progress-bar-stripes`
- `load7`
- `wpb_ttb`
- `wpb_btt`
- `wpb_ltr`

### Motion Tokens

- **Duration scale:** `0ms`, `.3s`, `.35s`, `.75s`, `1s`, `1.5s`, `2s`, `25ms`, `80ms`, `81ms`, `150ms`, `200ms`, `300ms`, `350ms`, `400ms`, `500ms`, `600ms`, `1000ms`
- **Easing functions:** `cubic-bezier(.215,.61,.355,1)`, `cubic-bezier(.755,.05,.855,.06)`, `ease-out`, `ease-in`, `ease-in-out`, `cubic-bezier(.55,.055,.675,.19)`, `cubic-bezier(.175,.885,.32,1)`, `ease`, `cubic-bezier(.35,.7,.35,1)`, `cubic-bezier(.86,0,.07,1)`, `linear`

### Motion Guidelines

- **Duration:** Use values from the duration scale above. Short (0ms) for micro-interactions, long (1000ms) for page transitions
- **Easing:** Use `cubic-bezier(.215,.61,.355,1)` as the default easing curve
- **Direction:** Elements enter from bottom/right, exit to top/left
- **Reduced motion:** Always respect `prefers-reduced-motion` — disable animations when set

## Depth & Elevation

### Shadow Tokens

- Subtle: `0 0 2px 2px rgba(0,0,0,.6)`
- Subtle: `0 1px 2px 0 rgba(0,0,0,.3)`
- Subtle: `rgba(0, 0, 0, 0.3) 0px 1px 2px 0px`
- Raised (cards, buttons): `0 2.5em 0-1.3em rgba(235,235,235,.75)`
- Raised (cards, buttons): `0 2.5em 0 0 rgba(235,235,235,.75)`
- Raised (cards, buttons): `0 2px 6px 0 rgba(0,0,0,.5)`

### Z-Index Scale

`1, 2, 10, 11, 12, 13, 20, 99, 100, 150, 9000, 9999, 100000`

Use these exact values — never invent z-index values.

## Anti-Patterns (Never Do)

- **No blur effects** — no backdrop-blur, no filter: blur()
- **No zebra striping** — tables and lists use borders for separation
- **No invented colors** — every hex value must come from the palette above
- **No arbitrary spacing** — every dimension is a multiple of 5px
- **No extra fonts** — only Pe-icon-7-stroke and AgrikoleIcons are allowed
- **No arbitrary border-radius** — use the scale: .5rem, 2px, 3px, 4px, 5px, 8px, 22px, 24px, 26px, 30px
- **No opacity for disabled states** — use muted colors instead

## Workflow

1. **Read** `references/DESIGN.md` before writing any UI code
2. **Pick colors** from the Color System section — never invent new ones
3. **Set typography** — Pe-icon-7-stroke, AgrikoleIcons only, using the type scale
4. **Build layout** on the 5px grid — check every margin, padding, gap
5. **Match components** to patterns above before creating new ones
6. **Apply elevation** — use shadow tokens
7. **Validate** — every value traces back to a design token. No magic numbers.

## Brand Spec

- **Favicon:** `https://nucleorural.com.br/wp-content/uploads/2024/08/cropped-Copia-de-WhatsApp_Image_2024-05-27_at_09.00.43-removebg-preview-32x32.png`
- **Site URL:** `https://nucleorural.com.br/`
- **Brand color:** `#00d084`
- **Brand typeface:** Pe-icon-7-stroke

## Quick Reference

```
Background:     #ffffff
Surface:        #f5f0e9
Text:           #043038 / #878986
Accent:         #00d084
Border:         #404a3d
Font:           Pe-icon-7-stroke
Spacing:        5px grid
Radius:         8px
Components:     7 detected
```

## When to Trigger

Activate this skill when:
- Creating new components, pages, or visual elements for nucleorural-design
- Writing CSS, Tailwind classes, styled-components, or inline styles
- Building page layouts, templates, or responsive designs
- Reviewing UI code for design consistency
- The user mentions "nucleorural-design" design, style, UI, or theme
- Generating mockups, wireframes, or visual prototypes

---

# Full Reference Files

> Every output file is embedded below. Claude has full design system context from /skills alone.

## Design System Tokens (DESIGN.md)

# nucleorural-design DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 2 · Components: 7
> Icon library: not detected · State: not detected
> Primary theme: light · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![nucleorural-design Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **light-themed** interface with a cool, approachable feel. The light background emphasizes content clarity. Typography pairs **AgrikoleIcons** for display/headings with **Pe-icon-7-stroke** for body text, creating clear visual hierarchy through type contrast. Spacing follows a **5px base grid** (standard density), with scale: 5, 10, 15, 20, 25, 30, 35, 40px. The accent color **#00d084** anchors interactive elements (buttons, links, focus rings). Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| wp--preset--color--white | `#ffffff` | background | Page background, darkest surface |
| surface | `#f5f0e9` | surface | Card and panel backgrounds |
| text-primary | `#043038` | text-primary | Headings and body text |
| text-muted | `#878986` | text-muted | Captions, placeholders, secondary info |
| border | `#404a3d` | border | Dividers, card borders, outlines |
| wp--preset--color--vivid-green-cyan | `#00d084` | accent | CTAs, links, focus rings, active states |
| danger | `#ff4539` | danger | Error states, destructive actions |
| success | `#83c75d` | success | Success states, positive indicators |
| warning | `#eddd5e` | warning | Warning states, caution indicators |
| wp--preset--color--vivid-cyan-blue | `#0693e3` | info | Informational highlights |
| unknown | `#5b8c51` | unknown | Palette color |
| unknown | `#c5c9c4` | unknown | Palette color |
| wp--preset--color--black | `#000000` | unknown | Palette color |
| unknown | `#313131` | unknown | Palette color |
| wp-editor-canvas-background | `#dddddd` | unknown | Palette color |
| unknown | `#128c7e` | unknown | Palette color |
| wndb--color--primary | `#0000ff` | unknown | Palette color |
| unknown | `#25d366` | unknown | Palette color |
| unknown | `#4a4a4a` | unknown | Palette color |
| unknown | `#252a24` | unknown | Palette color |

### CSS Variable Tokens

```css
--wp-editor-canvas-background: #ddd;
--wp-admin-border-width-focus: 2px;
--wp-admin-border-width-focus: 1.5px;
--wndb--color--borders: var(--wndb--color--subtle);
--wndb--border--radius--sm: 0.25rem;
--wndb--border--radius--md: 0.5rem;
--wndb--border--radius--lg: 0.75rem;
--wndb--border--radius--xl: 1rem;
--wndb--border--radius: 0;
--wndb--border--radius: var(--wndb--border--radius--sm);
--wndb--border--radius: var(--wndb--border--radius--md);
--wndb--border--radius: var(--wndb--border--radius--lg);
--wndb--border--radius: var(--wndb--border--radius--xl);
--wndb--border--radius: 9999px;
--wndb--color--primary: #00f;
--wndb--color--secondary: #00f;
--wndb--color--borders: var(--wndb-gray-150);
--wndb--color--borders-light: var(--wndb-gray-100);
--wndb--color--borders-strong: var(--wndb--color--text--faded);
--wndb--color--borders: var(--wndb-gray-150);
```


---

## 3. Typography Rules

**Font Stack:**
- **Pe-icon-7-stroke** — Heading 1, Heading 2, Heading 3
- **AgrikoleIcons** — Body, Caption

**Font Sources:**

```css
@font-face {
  font-family: "Montserrat";
  src: url("fonts/Montserrat-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Montserrat";
  src: url("fonts/Montserrat-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Barlow";
  src: url("fonts/Barlow-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Barlow";
  src: url("fonts/Barlow-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Roboto";
  src: url("fonts/Roboto-Bold.ttf") format("truetype");
  font-weight: 700;
}
@font-face {
  font-family: "Roboto";
  src: url("fonts/Roboto-Regular.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "AgrikoleIcons";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "Pe-icon-7-stroke";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.eot?d7yf1v");
  font-weight: 400;
}
@font-face {
  font-family: "ElegantIcons";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "vcpb-plugin-icons";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "vc_grid_v1";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.eot?-9hbgac");
  font-weight: 400;
}
@font-face {
  font-family: "Core Icon";
  src: url("https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.eot?d7yf1v");
  font-weight: 400;
}
@font-face {
  font-family: "ytpregular";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../../../../../plugins/wprt-addons/assets/font/ytp-regular.eot") format("embedded-opentype");
  font-weight: 400;
}
@font-face {
  font-family: "revicons";
  src: url("https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.eot?5510888") format("embedded-opentype");
  font-weight: 400;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Pe-icon-7-stroke | 70px | 700 |
| Heading 2 | Pe-icon-7-stroke | 50px | 700 |
| Heading 3 | Pe-icon-7-stroke | 40px | 700 |
| Body | AgrikoleIcons | 16px | 400 |
| Caption | AgrikoleIcons | 18px | 400 |

**Typographic Rules:**
- Limit to 2 font families max per screen
- Use **Pe-icon-7-stroke** for body/UI text, **AgrikoleIcons** for display/headings
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

- **Base spacing unit:** 5px
- **Spacing scale:** 5, 10, 15, 20, 25, 30, 35, 40, 50, 60, 70, 80
- **Border radius:** 0px 0px 5px, 0px 0px 5px 5px, 0px 5px 0px 0px, .5rem, 2px, 3px, 4px, 5px, 8px, 22px, 24px, 26px, 30px, 32px, 100%, 999px
- **Max content width:** 1024px

**Spacing as Meaning:**
| Spacing | Use |
|---|---|
| 2.5-5px | Tight: related items within a group |
| 10px | Medium: between groups |
| 15-20px | Wide: between sections |
| 30px+ | Vast: major section breaks |


---

## 6. Depth & Elevation

### Flat — subtle depth hints

- `0 0 2px 2px rgba(0,0,0,.6)`
- `0 1px 2px 0 rgba(0,0,0,.3)`
- `rgba(0, 0, 0, 0.3) 0px 1px 2px 0px`

### Raised — cards, buttons, interactive elements

- `0 2.5em 0-1.3em rgba(235,235,235,.75)`
- `0 2.5em 0 0 rgba(235,235,235,.75)`
- `0 2px 6px 0 rgba(0,0,0,.5)`

### Floating — dropdowns, popovers, modals

- `0 15px 15px 0 rgba(0,0,0,.03)`
- `0 10px 10px 0 rgba(0,0,0,.03)`
- `6px 6px 20px rgba(0,0,0,.2)`

### Overlay — full-screen overlays, top-level dialogs

- `1px 6px 24px 0 rgba(7,94,84,.24)`
- `rgba(7, 94, 84, 0.24) 1px 6px 24px 0px`

### Z-Index Scale

`1, 2, 10, 11, 12, 13, 20, 99, 100, 150, 9000, 9999, 100000`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes progress-bar-stripes`
- `@keyframes load7`
- `@keyframes wpb_ttb`
- `@keyframes wpb_btt`
- `@keyframes wpb_ltr`
- `@keyframes wpb_rtl`
- `@keyframes wpb_appear`
- `@keyframes vc_woo-add-cart-load`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#00d084` for interactive elements (buttons, links, focus rings)
- Use `#ffffff` as the primary page background
- Pair **Pe-icon-7-stroke** (body) with **AgrikoleIcons** (display) — these are the only allowed fonts
- Follow the **5px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: 0px 0px 5px, 0px 0px 5px 5px, 0px 5px 0px 0px, .5rem, 2px
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't introduce additional font families beyond Pe-icon-7-stroke and AgrikoleIcons
- Don't use arbitrary spacing values — stick to multiples of 5px
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
| sm | 600px | css |
| md | 767px | css |
| md | 768px | css |
| lg | 782px | css |
| lg | 991px | css |
| lg | 992px | css |
| lg | 1024px | css |
| xl | 1025px | css |
| xl | 1199px | css |
| xl | 1200px | css |
| xl | 1230px | css |
| 2xl | 1440px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #f5f0e9
Border: 1px solid #404a3d
Radius: 8px
Padding: 20px
Font: Pe-icon-7-stroke
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg #00d084, text white
Ghost: bg transparent, border #404a3d
Padding: 10px 20px
Radius: 8px
Hover: opacity 0.9 or lighter shade
Focus: ring with #00d084
```

### Build a Page Layout

```
Background: #ffffff
Max-width: 1024px, centered
Grid: 5px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #f5f0e9
Label: #878986 (muted, 12px, uppercase)
Value: #043038 (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #ffffff
Input border: 1px solid #404a3d
Focus: border-color #00d084
Label: #878986 12px
Spacing: 20px between fields
Radius: 8px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Pe-icon-7-stroke, type scale from Section 3
4. Spacing: 5px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```

## Visual Guide — Screenshots (VISUAL_GUIDE.md)

# nucleorural-design — Visual Guide

> Master visual reference. Study every screenshot carefully before implementing any UI.
> Match colors, layout, typography, spacing, and motion states exactly.

## Scroll Journey

The page has cinematic scroll animations. Each screenshot below shows the exact visual state at that scroll depth.
**Replicate these transitions precisely** — the design changes dramatically as you scroll.

### Hero — Above the fold

*Scroll position: 0px of 6144px total*

![Hero — Above the fold](../screens/scroll/scroll-000.png)

### 17% scroll depth

*Scroll position: 891px of 6144px total*

![17% scroll depth](../screens/scroll/scroll-017.png)

### 33% scroll depth

*Scroll position: 1731px of 6144px total*

![33% scroll depth](../screens/scroll/scroll-033.png)

### 50% scroll depth

*Scroll position: 2622px of 6144px total*

![50% scroll depth](../screens/scroll/scroll-050.png)

### 67% scroll depth

*Scroll position: 3447px of 6144px total*

![67% scroll depth](../screens/scroll/scroll-067.png)

### 83% scroll depth

*Scroll position: 3447px of 6144px total*

![83% scroll depth](../screens/scroll/scroll-083.png)

### Footer — End of page

*Scroll position: 3447px of 6144px total*

![Footer — End of page](../screens/scroll/scroll-100.png)

## Full Page Screenshots

### Núcleo Rural: suplementos para gado de corte e leite

*URL: `https://nucleorural.com.br/`*

![Núcleo Rural: suplementos para gado de corte e leite](../screens/pages/home.png)

### Blog Núcleo Rural: Dicas Práticas para Pecuária de Alta Performance

*URL: `https://nucleorural.com.br/blog/`*

![Blog Núcleo Rural: Dicas Práticas para Pecuária de Alta Performance](../screens/pages/blog.png)

### Contato - Núcleo Rural

*URL: `https://nucleorural.com.br/contato/`*

![Contato - Núcleo Rural](../screens/pages/contato.png)

### Eliminação de Parasitas do Gado com Master S3 - Núcleo Rural

*URL: `https://nucleorural.com.br/project/aumento-na-producao-de-carne/`*

![Eliminação de Parasitas do Gado com Master S3 - Núcleo Rural](../screens/pages/project-aumento-na-producao-de-carne.png)

### Eliminação de Parasitas do Gado

*URL: `https://nucleorural.com.br/project/eliminacao-de-parasitas-do-gado/`*

![Eliminação de Parasitas do Gado](../screens/pages/project-eliminacao-de-parasitas-do-gado.png)

## Section Screenshots

Clipped sections showing individual components in context.

### Section 1 — `section`

*1440×460px*

![Section 1](../screens/sections/home-section-1.png)

### Section 2 — `section`

*1440×749px*

![Section 2](../screens/sections/home-section-2.png)

### Section 1 — `section`

*1440×609px*

![Section 1](../screens/sections/contato-section-1.png)

### Section 2 — `article`

*1440×806px*

![Section 2](../screens/sections/contato-section-2.png)

### Section 1 — `section`

*1440×267px*

![Section 1](../screens/sections/project-aumento-na-producao-de-carne-section-1.png)

### Section 2 — `section`

*1440×523px*

![Section 2](../screens/sections/project-aumento-na-producao-de-carne-section-2.png)

## Animations & Motion (ANIMATIONS.md)

# Animation Reference

> Cinematic motion design extracted from live DOM. Follow these specs exactly to recreate the experience.

## Motion Technology Stack

Pure CSS animations — no external animation libraries detected.

## Scroll Journey

The page is **6.144px** tall. Each frame below shows what the user sees at that scroll depth.

> **Use these screenshots to understand WHAT animates, WHEN it animates, and HOW it moves.**

### 0% — Top / Hero
Scroll position: 0px

![Scroll 0%](../screens/scroll/scroll-000.png)

### 17% — Opening Section
Scroll position: 891px

![Scroll 17%](../screens/scroll/scroll-017.png)

### 33% — First Feature Section
Scroll position: 1.731px

![Scroll 33%](../screens/scroll/scroll-033.png)

### 50% — Mid-Page
Scroll position: 2.622px

![Scroll 50%](../screens/scroll/scroll-050.png)

### 67% — Lower Content
Scroll position: 3.447px

![Scroll 67%](../screens/scroll/scroll-067.png)

### 83% — Near Footer
Scroll position: 3.447px

![Scroll 83%](../screens/scroll/scroll-083.png)

### 100% — Bottom / Footer
Scroll position: 3.447px

![Scroll 100%](../screens/scroll/scroll-100.png)

## Scroll Animation Patterns

| Pattern | Library | Element Count | Duration | Delay | Easing |
|---------|---------|---------------|----------|-------|--------|
| scroll-trigger | GSAP | 2 | — | — | — |
| parallax / sticky scroll | CSS | 7 | — | — | — |

### GSAP Implementation

```javascript
// GSAP ScrollTrigger
gsap.registerPlugin(ScrollTrigger);

gsap.from('.element', {
  opacity: 0,
  y: 60,
  duration: 0.8,
  ease: 'power2.out',
  scrollTrigger: {
    trigger: '.element',
    start: 'top 80%',
    end: 'bottom 20%',
  }
});
```

### CSS Implementation

## CSS Keyframes (362 extracted)

### `@keyframes joinchat_show`

Duration: `0.5s` · Easing: `cubic-bezier(0.18, 0.89, 0.32, 1.28)` · Delay: `10ms` · Iteration: `1` · Fill: `both`

Used by: `.joinchat`, `.joinchat__bubble`

```css
@keyframes joinchat_show {
  0% {
    transform: scale3d(0, 0, 0);
  }
  100% {
    transform: scaleX(1);
  }
}
```

> Transform/motion animation

### `@keyframes progress-bar-stripes`

Duration: `2s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.vc_progress_bar .vc_single_bar .vc_bar.animated`

```css
@keyframes progress-bar-stripes {
  0% {
    background-position-x: 40px;
    background-position-y: 0px;
  }
  100% {
    background-position-x: 0px;
    background-position-y: 0px;
  }
}
```

> Background color/gradient shift · Background position (shimmer/scroll)

### `@keyframes reveal-from-left`

Used by: `.agrikole-simple-image.reveal.lr.animated::after`

```css
@keyframes reveal-from-left {
  0% {
    transform-origin: left top;
    transform: scale(0, 1);
  }
  66.6% {
    transform-origin: left center;
    transform: scale(1, 1);
  }
  66.7% {
    transform-origin: right center;
    transform: scale(1, 1);
  }
  100% {
    transform-origin: right center;
    transform: scale(0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes reveal-from-right`

Used by: `.agrikole-simple-image.reveal.rl.animated::after`

```css
@keyframes reveal-from-right {
  0% {
    transform-origin: right top;
    transform: scale(0, 1);
  }
  66.6% {
    transform-origin: right center;
    transform: scale(1, 1);
  }
  66.7% {
    transform-origin: left center;
    transform: scale(1, 1);
  }
  100% {
    transform-origin: left center;
    transform: scale(0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes flip`

Used by: `.animated.flip`

```css
@keyframes flip {
  0% {
    transform: perspective(400px) rotate3d(0, 1, 0, -360deg);
    animation-timing-function: ease-out;
  }
  40% {
    transform: perspective(400px) translate3d(0px, 0px, 150px) rotate3d(0, 1, 0, -190deg);
    animation-timing-function: ease-out;
  }
  50% {
    transform: perspective(400px) translate3d(0px, 0px, 150px) rotate3d(0, 1, 0, -170deg);
    animation-timing-function: ease-in;
  }
  80% {
    transform: perspective(400px) scale3d(0.95, 0.95, 0.95);
    animation-timing-function: ease-in;
  }
  100% {
    transform: perspective(400px);
    animation-timing-function: ease-in;
  }
}
```

> Transform/motion animation

### `@keyframes cbp-rotation`

Duration: `0.8s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.cbp::after, .cbp-lazyload::after, .cbp-popup-loadingBox::after, .cbp-popup-sing`

```css
@keyframes cbp-rotation {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes cbp-rotation`

Duration: `0.8s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.cbp::after, .cbp-lazyload::after, .cbp-popup-loadingBox::after, .cbp-popup-sing`

```css
@keyframes cbp-rotation {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes scroll-slider-slide`

Duration: `1s` · Easing: `ease` · Delay: `1s` · Iteration: `1` · Fill: `forwards`

Used by: `.nfd-scroll-slider-horizontal.nfd-scroll-slider-animate > .wp-block-cover:first-`

```css
@keyframes scroll-slider-slide {
  0% {
    margin-left: 0px;
  }
  100% {
    margin-left: -100vw;
  }
}
```

### `@keyframes pmFadeIn`

Duration: `500ms` · Easing: `ease` · Delay: `0s` · Iteration: `1` · Fill: `none`

Used by: `.perfmatters-lazy.pmloaded, .perfmatters-lazy.pmloaded > img, .perfmatters-lazy `

```css
@keyframes pmFadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes load7`

```css
@keyframes load7 {
  0%, 100%, 80% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px -1.3em;
  }
  40% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px 0px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes wpb_ttb`

```css
@keyframes wpb_ttb {
  0% {
    transform: translate(0px, -10%);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_btt`

```css
@keyframes wpb_btt {
  0% {
    transform: translate(0px, 10%);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_ltr`

```css
@keyframes wpb_ltr {
  0% {
    transform: translate(-10%, 0px);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_rtl`

```css
@keyframes wpb_rtl {
  0% {
    transform: translate(10%, 0px);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_appear`

```css
@keyframes wpb_appear {
  0% {
    transform: scale(0.5);
    opacity: 0.1;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes vc_woo-add-cart-load`

```css
@keyframes vc_woo-add-cart-load {
  0%, 100%, 80% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px -1.3em;
  }
  40% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px 0px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes hide-show`

```css
@keyframes hide-show {
  0%, 66.6% {
    opacity: 0;
    visibility: hidden;
  }
  100%, 66.7% {
    opacity: 1;
    visibility: visible;
  }
}
```

> Opacity fade

### `@keyframes bounce`

```css
@keyframes bounce {
  0%, 20%, 53%, 80%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
    transform: translate3d(0px, 0px, 0px);
  }
  40%, 43% {
    animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
    transform: translate3d(0px, -30px, 0px);
  }
  70% {
    animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
    transform: translate3d(0px, -15px, 0px);
  }
  90% {
    transform: translate3d(0px, -4px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes flash`

```css
@keyframes flash {
  0%, 50%, 100% {
    opacity: 1;
  }
  25%, 75% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes pulse`

```css
@keyframes pulse {
  0% {
    transform: scale3d(1, 1, 1);
  }
  50% {
    transform: scale3d(1.05, 1.05, 1.05);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rubberBand`

```css
@keyframes rubberBand {
  0% {
    transform: scale3d(1, 1, 1);
  }
  30% {
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes shake`

```css
@keyframes shake {
  0%, 100% {
    transform: translate3d(0px, 0px, 0px);
  }
  10%, 30%, 50%, 70%, 90% {
    transform: translate3d(-10px, 0px, 0px);
  }
  20%, 40%, 60%, 80% {
    transform: translate3d(10px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes headShake`

```css
@keyframes headShake {
  0% {
    transform: translateX(0px);
  }
  6.5% {
    transform: translateX(-6px) rotateY(-9deg);
  }
  18.5% {
    transform: translateX(5px) rotateY(7deg);
  }
  31.5% {
    transform: translateX(-3px) rotateY(-5deg);
  }
  43.5% {
    transform: translateX(2px) rotateY(3deg);
  }
  50% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes swing`

```css
@keyframes swing {
  20% {
    transform: rotate3d(0, 0, 1, 15deg);
  }
  40% {
    transform: rotate3d(0, 0, 1, -10deg);
  }
  60% {
    transform: rotate3d(0, 0, 1, 5deg);
  }
  80% {
    transform: rotate3d(0, 0, 1, -5deg);
  }
  100% {
    transform: rotate3d(0, 0, 1, 0deg);
  }
}
```

> Transform/motion animation

### `@keyframes tada`

```css
@keyframes tada {
  0% {
    transform: scale3d(1, 1, 1);
  }
  10%, 20% {
    transform: scale3d(0.9, 0.9, 0.9) rotate3d(0, 0, 1, -3deg);
  }
  30%, 50%, 70%, 90% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, 3deg);
  }
  40%, 60%, 80% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, -3deg);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes wobble`

```css
@keyframes wobble {
  0% {
    transform: none;
  }
  15% {
    transform: translate3d(-25%, 0px, 0px) rotate3d(0, 0, 1, -5deg);
  }
  30% {
    transform: translate3d(20%, 0px, 0px) rotate3d(0, 0, 1, 3deg);
  }
  45% {
    transform: translate3d(-15%, 0px, 0px) rotate3d(0, 0, 1, -3deg);
  }
  60% {
    transform: translate3d(10%, 0px, 0px) rotate3d(0, 0, 1, 2deg);
  }
  75% {
    transform: translate3d(-5%, 0px, 0px) rotate3d(0, 0, 1, -1deg);
  }
  100% {
    transform: none;
  }
}
```

> Transform/motion animation

### `@keyframes jello`

```css
@keyframes jello {
  0%, 11.1%, 100% {
    transform: none;
  }
  22.2% {
    transform: skewX(-12.5deg) skewY(-12.5deg);
  }
  33.3% {
    transform: skewX(6.25deg) skewY(6.25deg);
  }
  44.4% {
    transform: skewX(-3.125deg) skewY(-3.125deg);
  }
  55.5% {
    transform: skewX(1.5625deg) skewY(1.5625deg);
  }
  66.6% {
    transform: skewX(-0.78125deg) skewY(-0.78125deg);
  }
  77.7% {
    transform: skewX(0.390625deg) skewY(0.390625deg);
  }
  88.8% {
    transform: skewX(-0.195312deg) skewY(-0.195312deg);
  }
}
```

> Transform/motion animation

### `@keyframes bounceIn`

```css
@keyframes bounceIn {
  0%, 20%, 40%, 60%, 80%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  20% {
    transform: scale3d(1.1, 1.1, 1.1);
  }
  40% {
    transform: scale3d(0.9, 0.9, 0.9);
  }
  60% {
    opacity: 1;
    transform: scale3d(1.03, 1.03, 1.03);
  }
  80% {
    transform: scale3d(0.97, 0.97, 0.97);
  }
  100% {
    opacity: 1;
    transform: scale3d(1, 1, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInDown`

```css
@keyframes bounceInDown {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(0px, -3000px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(0px, 25px, 0px);
  }
  75% {
    transform: translate3d(0px, -10px, 0px);
  }
  90% {
    transform: translate3d(0px, 5px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInLeft`

```css
@keyframes bounceInLeft {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(-3000px, 0px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(25px, 0px, 0px);
  }
  75% {
    transform: translate3d(-10px, 0px, 0px);
  }
  90% {
    transform: translate3d(5px, 0px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInRight`

```css
@keyframes bounceInRight {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(3000px, 0px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(-25px, 0px, 0px);
  }
  75% {
    transform: translate3d(10px, 0px, 0px);
  }
  90% {
    transform: translate3d(-5px, 0px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInUp`

```css
@keyframes bounceInUp {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(0px, 3000px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(0px, -20px, 0px);
  }
  75% {
    transform: translate3d(0px, 10px, 0px);
  }
  90% {
    transform: translate3d(0px, -5px, 0px);
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOut`

```css
@keyframes bounceOut {
  20% {
    transform: scale3d(0.9, 0.9, 0.9);
  }
  50%, 55% {
    opacity: 1;
    transform: scale3d(1.1, 1.1, 1.1);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutDown`

```css
@keyframes bounceOutDown {
  20% {
    transform: translate3d(0px, 10px, 0px);
  }
  40%, 45% {
    opacity: 1;
    transform: translate3d(0px, -20px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutLeft`

```css
@keyframes bounceOutLeft {
  20% {
    opacity: 1;
    transform: translate3d(20px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(-2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutRight`

```css
@keyframes bounceOutRight {
  20% {
    opacity: 1;
    transform: translate3d(-20px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutUp`

```css
@keyframes bounceOutUp {
  20% {
    transform: translate3d(0px, -10px, 0px);
  }
  40%, 45% {
    opacity: 1;
    transform: translate3d(0px, 20px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeInDown`

```css
@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translate3d(0px, -20px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInDownBig`

```css
@keyframes fadeInDownBig {
  0% {
    opacity: 0;
    transform: translate3d(0px, -1000px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInLeft`

```css
@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translate3d(-20px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInLeftBig`

```css
@keyframes fadeInLeftBig {
  0% {
    opacity: 0;
    transform: translate3d(-1000px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInRight`

```css
@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translate3d(20px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInRightBig`

```css
@keyframes fadeInRightBig {
  0% {
    opacity: 0;
    transform: translate3d(1000px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInUp`

```css
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translate3d(0px, 20px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInUpBig`

```css
@keyframes fadeInUpBig {
  0% {
    opacity: 0;
    transform: translate3d(0px, 1000px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut`

```css
@keyframes fadeOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOutDown`

```css
@keyframes fadeOutDown {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 100%, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutDownBig`

```css
@keyframes fadeOutDownBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutLeft`

```css
@keyframes fadeOutLeft {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(-100%, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutLeftBig`

```css
@keyframes fadeOutLeftBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(-2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutRight`

```css
@keyframes fadeOutRight {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(100%, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutRightBig`

```css
@keyframes fadeOutRightBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutUp`

```css
@keyframes fadeOutUp {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -100%, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutUpBig`

```css
@keyframes fadeOutUpBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipInX`

```css
@keyframes flipInX {
  0% {
    transform: perspective(400px) rotate3d(1, 0, 0, 90deg);
    animation-timing-function: ease-in;
    opacity: 0;
  }
  40% {
    transform: perspective(400px) rotate3d(1, 0, 0, -20deg);
    animation-timing-function: ease-in;
  }
  60% {
    transform: perspective(400px) rotate3d(1, 0, 0, 10deg);
    opacity: 1;
  }
  80% {
    transform: perspective(400px) rotate3d(1, 0, 0, -5deg);
  }
  100% {
    transform: perspective(400px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipInY`

```css
@keyframes flipInY {
  0% {
    transform: perspective(400px) rotate3d(0, 1, 0, 90deg);
    animation-timing-function: ease-in;
    opacity: 0;
  }
  40% {
    transform: perspective(400px) rotate3d(0, 1, 0, -20deg);
    animation-timing-function: ease-in;
  }
  60% {
    transform: perspective(400px) rotate3d(0, 1, 0, 10deg);
    opacity: 1;
  }
  80% {
    transform: perspective(400px) rotate3d(0, 1, 0, -5deg);
  }
  100% {
    transform: perspective(400px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOutX`

```css
@keyframes flipOutX {
  0% {
    transform: perspective(400px);
  }
  30% {
    transform: perspective(400px) rotate3d(1, 0, 0, -20deg);
    opacity: 1;
  }
  100% {
    transform: perspective(400px) rotate3d(1, 0, 0, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOutY`

```css
@keyframes flipOutY {
  0% {
    transform: perspective(400px);
  }
  30% {
    transform: perspective(400px) rotate3d(0, 1, 0, -15deg);
    opacity: 1;
  }
  100% {
    transform: perspective(400px) rotate3d(0, 1, 0, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes lightSpeedIn`

```css
@keyframes lightSpeedIn {
  0% {
    transform: translate3d(100%, 0px, 0px) skewX(-30deg);
    opacity: 0;
  }
  60% {
    transform: skewX(20deg);
    opacity: 1;
  }
  80% {
    transform: skewX(-5deg);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes lightSpeedOut`

```css
@keyframes lightSpeedOut {
  0% {
    opacity: 1;
  }
  100% {
    transform: translate3d(100%, 0px, 0px) skewX(30deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateIn`

```css
@keyframes rotateIn {
  0% {
    transform-origin: center center;
    transform: rotate3d(0, 0, 1, -200deg);
    opacity: 0;
  }
  100% {
    transform-origin: center center;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInDownLeft`

```css
@keyframes rotateInDownLeft {
  0% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
  100% {
    transform-origin: left bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInDownRight`

```css
@keyframes rotateInDownRight {
  0% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
  100% {
    transform-origin: right bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInUpLeft`

```css
@keyframes rotateInUpLeft {
  0% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
  100% {
    transform-origin: left bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInUpRight`

```css
@keyframes rotateInUpRight {
  0% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, -90deg);
    opacity: 0;
  }
  100% {
    transform-origin: right bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOut`

```css
@keyframes rotateOut {
  0% {
    transform-origin: center center;
    opacity: 1;
  }
  100% {
    transform-origin: center center;
    transform: rotate3d(0, 0, 1, 200deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutDownLeft`

```css
@keyframes rotateOutDownLeft {
  0% {
    transform-origin: left bottom;
    opacity: 1;
  }
  100% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutDownRight`

```css
@keyframes rotateOutDownRight {
  0% {
    transform-origin: right bottom;
    opacity: 1;
  }
  100% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutUpLeft`

```css
@keyframes rotateOutUpLeft {
  0% {
    transform-origin: left bottom;
    opacity: 1;
  }
  100% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutUpRight`

```css
@keyframes rotateOutUpRight {
  0% {
    transform-origin: right bottom;
    opacity: 1;
  }
  100% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes hinge`

```css
@keyframes hinge {
  0% {
    transform-origin: left top;
    animation-timing-function: ease-in-out;
  }
  20%, 60% {
    transform: rotate3d(0, 0, 1, 80deg);
    transform-origin: left top;
    animation-timing-function: ease-in-out;
  }
  40%, 80% {
    transform: rotate3d(0, 0, 1, 60deg);
    transform-origin: left top;
    animation-timing-function: ease-in-out;
    opacity: 1;
  }
  100% {
    transform: translate3d(0px, 700px, 0px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes jackInTheBox`

```css
@keyframes jackInTheBox {
  0% {
    opacity: 0;
    transform: scale(0.1) rotate(30deg);
    transform-origin: center bottom;
  }
  50% {
    transform: rotate(-10deg);
  }
  70% {
    transform: rotate(3deg);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes rollIn`

```css
@keyframes rollIn {
  0% {
    opacity: 0;
    transform: translate3d(-100%, 0px, 0px) rotate3d(0, 0, 1, -120deg);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes rollOut`

```css
@keyframes rollOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(100%, 0px, 0px) rotate3d(0, 0, 1, 120deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomIn`

```css
@keyframes zoomIn {
  0% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInDown`

```css
@keyframes zoomInDown {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, -1000px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, 60px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInLeft`

```css
@keyframes zoomInLeft {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(-1000px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(10px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInRight`

```css
@keyframes zoomInRight {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(1000px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(-10px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInUp`

```css
@keyframes zoomInUp {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, 1000px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, -60px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOut`

```css
@keyframes zoomOut {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutDown`

```css
@keyframes zoomOutDown {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, -60px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, 2000px, 0px);
    transform-origin: center bottom;
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutLeft`

```css
@keyframes zoomOutLeft {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(42px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: scale(0.1) translate3d(-2000px, 0px, 0px);
    transform-origin: left center;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutRight`

```css
@keyframes zoomOutRight {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(-42px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: scale(0.1) translate3d(2000px, 0px, 0px);
    transform-origin: right center;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutUp`

```css
@keyframes zoomOutUp {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, 60px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, -2000px, 0px);
    transform-origin: center bottom;
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideInDown`

```css
@keyframes slideInDown {
  0% {
    transform: translate3d(0px, -100%, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInLeft`

```css
@keyframes slideInLeft {
  0% {
    transform: translate3d(-100%, 0px, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInRight`

```css
@keyframes slideInRight {
  0% {
    transform: translate3d(100%, 0px, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInUp`

```css
@keyframes slideInUp {
  0% {
    transform: translate3d(0px, 100%, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutDown`

```css
@keyframes slideOutDown {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(0px, 100%, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutLeft`

```css
@keyframes slideOutLeft {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(-100%, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutRight`

```css
@keyframes slideOutRight {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(100%, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutUp`

```css
@keyframes slideOutUp {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(0px, -100%, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading`

```css
@keyframes animsition-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading`

```css
@keyframes animsition-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading-reverse`

```css
@keyframes animsition-loading-reverse {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading-reverse`

```css
@keyframes animsition-loading-reverse {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes fade-in`

```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade-in`

```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade-out`

```css
@keyframes fade-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fade-out`

```css
@keyframes fade-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fade-in-up`

```css
@keyframes fade-in-up {
  0% {
    transform: translateY(500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up`

```css
@keyframes fade-in-up {
  0% {
    transform: translateY(500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up`

```css
@keyframes fade-out-up {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up`

```css
@keyframes fade-out-up {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-sm`

```css
@keyframes fade-in-up-sm {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-sm`

```css
@keyframes fade-in-up-sm {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-sm`

```css
@keyframes fade-out-up-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-sm`

```css
@keyframes fade-out-up-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-lg`

```css
@keyframes fade-in-up-lg {
  0% {
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-lg`

```css
@keyframes fade-in-up-lg {
  0% {
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-lg`

```css
@keyframes fade-out-up-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-lg`

```css
@keyframes fade-out-up-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down`

```css
@keyframes fade-in-down {
  0% {
    transform: translateY(-500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down`

```css
@keyframes fade-in-down {
  0% {
    transform: translateY(-500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down`

```css
@keyframes fade-out-down {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down`

```css
@keyframes fade-out-down {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down-sm`

```css
@keyframes fade-in-down-sm {
  0% {
    transform: translateY(-100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down-sm`

```css
@keyframes fade-in-down-sm {
  0% {
    transform: translateY(-100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-sm`

```css
@keyframes fade-out-down-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-sm`

```css
@keyframes fade-out-down-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-lg`

```css
@keyframes fade-out-down-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-lg`

```css
@keyframes fade-out-down-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left`

```css
@keyframes fade-in-left {
  0% {
    transform: translateX(-500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left`

```css
@keyframes fade-in-left {
  0% {
    transform: translateX(-500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left`

```css
@keyframes fade-out-left {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left`

```css
@keyframes fade-out-left {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-sm`

```css
@keyframes fade-in-left-sm {
  0% {
    transform: translateX(-100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-sm`

```css
@keyframes fade-in-left-sm {
  0% {
    transform: translateX(-100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-sm`

```css
@keyframes fade-out-left-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-sm`

```css
@keyframes fade-out-left-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-lg`

```css
@keyframes fade-in-left-lg {
  0% {
    transform: translateX(-1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-lg`

```css
@keyframes fade-in-left-lg {
  0% {
    transform: translateX(-1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-lg`

```css
@keyframes fade-out-left-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-lg`

```css
@keyframes fade-out-left-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right`

```css
@keyframes fade-in-right {
  0% {
    transform: translateX(500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right`

```css
@keyframes fade-in-right {
  0% {
    transform: translateX(500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right`

```css
@keyframes fade-out-right {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right`

```css
@keyframes fade-out-right {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-sm`

```css
@keyframes fade-in-right-sm {
  0% {
    transform: translateX(100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-sm`

```css
@keyframes fade-in-right-sm {
  0% {
    transform: translateX(100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-sm`

```css
@keyframes fade-out-right-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-sm`

```css
@keyframes fade-out-right-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-lg`

```css
@keyframes fade-in-right-lg {
  0% {
    transform: translateX(1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-lg`

```css
@keyframes fade-in-right-lg {
  0% {
    transform: translateX(1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-lg`

```css
@keyframes fade-out-right-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-lg`

```css
@keyframes fade-out-right-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in`

```css
@keyframes rotate-in {
  0% {
    transform: rotate(-90deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in`

```css
@keyframes rotate-in {
  0% {
    transform: rotate(-90deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out`

```css
@keyframes rotate-out {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(90deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out`

```css
@keyframes rotate-out {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(90deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-sm`

```css
@keyframes rotate-in-sm {
  0% {
    transform: rotate(-45deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-sm`

```css
@keyframes rotate-in-sm {
  0% {
    transform: rotate(-45deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-sm`

```css
@keyframes rotate-out-sm {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(45deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-sm`

```css
@keyframes rotate-out-sm {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(45deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-lg`

```css
@keyframes rotate-in-lg {
  0% {
    transform: rotate(-180deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-lg`

```css
@keyframes rotate-in-lg {
  0% {
    transform: rotate(-180deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-lg`

```css
@keyframes rotate-out-lg {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(180deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-lg`

```css
@keyframes rotate-out-lg {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(180deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x`

```css
@keyframes flip-in-x {
  0% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x`

```css
@keyframes flip-in-x {
  0% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x`

```css
@keyframes flip-out-x {
  0% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x`

```css
@keyframes flip-out-x {
  0% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-nr`

```css
@keyframes flip-in-x-nr {
  0% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-nr`

```css
@keyframes flip-in-x-nr {
  0% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-nr`

```css
@keyframes flip-out-x-nr {
  0% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-nr`

```css
@keyframes flip-out-x-nr {
  0% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-fr`

```css
@keyframes flip-in-x-fr {
  0% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-fr`

```css
@keyframes flip-in-x-fr {
  0% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-fr`

```css
@keyframes flip-out-x-fr {
  0% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-fr`

```css
@keyframes flip-out-x-fr {
  0% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y`

```css
@keyframes flip-in-y {
  0% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y`

```css
@keyframes flip-in-y {
  0% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y`

```css
@keyframes flip-out-y {
  0% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y`

```css
@keyframes flip-out-y {
  0% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-nr`

```css
@keyframes flip-in-y-nr {
  0% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-nr`

```css
@keyframes flip-in-y-nr {
  0% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-nr`

```css
@keyframes flip-out-y-nr {
  0% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-nr`

```css
@keyframes flip-out-y-nr {
  0% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-fr`

```css
@keyframes flip-in-y-fr {
  0% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-fr`

```css
@keyframes flip-in-y-fr {
  0% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-fr`

```css
@keyframes flip-out-y-fr {
  0% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-fr`

```css
@keyframes flip-out-y-fr {
  0% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in`

```css
@keyframes zoom-in {
  0% {
    transform: scale(0.7);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in`

```css
@keyframes zoom-in {
  0% {
    transform: scale(0.7);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out`

```css
@keyframes zoom-out {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.7);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out`

```css
@keyframes zoom-out {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.7);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-sm`

```css
@keyframes zoom-in-sm {
  0% {
    transform: scale(0.95);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-sm`

```css
@keyframes zoom-in-sm {
  0% {
    transform: scale(0.95);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-sm`

```css
@keyframes zoom-out-sm {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.95);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-sm`

```css
@keyframes zoom-out-sm {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.95);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-lg`

```css
@keyframes zoom-in-lg {
  0% {
    transform: scale(0.4);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-lg`

```css
@keyframes zoom-in-lg {
  0% {
    transform: scale(0.4);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-lg`

```css
@keyframes zoom-out-lg {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.4);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-lg`

```css
@keyframes zoom-out-lg {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.4);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes overlay-slide-in-top`

```css
@keyframes overlay-slide-in-top {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-top`

```css
@keyframes overlay-slide-in-top {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-top`

```css
@keyframes overlay-slide-out-top {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-top`

```css
@keyframes overlay-slide-out-top {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-bottom`

```css
@keyframes overlay-slide-in-bottom {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-bottom`

```css
@keyframes overlay-slide-in-bottom {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-bottom`

```css
@keyframes overlay-slide-out-bottom {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-bottom`

```css
@keyframes overlay-slide-out-bottom {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-left`

```css
@keyframes overlay-slide-in-left {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-left`

```css
@keyframes overlay-slide-in-left {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-left`

```css
@keyframes overlay-slide-out-left {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-left`

```css
@keyframes overlay-slide-out-left {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-right`

```css
@keyframes overlay-slide-in-right {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-right`

```css
@keyframes overlay-slide-in-right {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-right`

```css
@keyframes overlay-slide-out-right {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-right`

```css
@keyframes overlay-slide-out-right {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes fa-spin`

```css
@keyframes fa-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(359deg);
  }
}
```

> Transform/motion animation

### `@keyframes fa-spin`

```css
@keyframes fa-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(359deg);
  }
}
```

> Transform/motion animation

### `@keyframes blink`

```css
@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes blink`

```css
@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes rev-ani-mouse`

```css
@keyframes rev-ani-mouse {
  0% {
    opacity: 1;
    top: 0%;
  }
  30% {
    opacity: 1;
    top: 30%;
  }
  70% {
    opacity: 0;
    top: 30%;
  }
  100% {
    opacity: 0;
    top: 0%;
  }
}
```

> Opacity fade

### `@keyframes circle-fade-inf`

```css
@keyframes circle-fade-inf {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(1.08);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_open_text`

```css
@keyframes joinchat_open_text {
  0% {
    max-width: 0px;
    opacity: 0;
  }
  60% {
    max-width: var(--mw);
    opacity: 0;
  }
  100% {
    max-width: var(--mw);
    opacity: 1;
  }
}
```

> Opacity fade · Dimension expand/collapse

### `@keyframes joinchat_badge_in`

```css
@keyframes joinchat_badge_in {
  0% {
    opacity: 0;
    transform: translate3d(0px, 50px, 0px);
  }
  100% {
    opacity: 1;
    transform: translateZ(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_badge_out`

```css
@keyframes joinchat_badge_out {
  0% {
    opacity: 1;
    transform: translateZ(0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -20px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_send_svg`

```css
@keyframes joinchat_send_svg {
  0%, 50%, 100% {
    stroke-dashoffset: var(--stroke);
  }
  5%, 45% {
    stroke-dashoffset: 0;
  }
}
```

> SVG stroke animation

### `@keyframes joinchat_image_loop`

```css
@keyframes joinchat_image_loop {
  0% {
    opacity: 0;
  }
  3%, 20% {
    opacity: 1;
  }
  25%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes joinchat_tootlip`

```css
@keyframes joinchat_tootlip {
  0% {
    opacity: 0;
    transform: scaleY(0);
  }
  1%, 20% {
    opacity: 1;
    transform: scaleX(1);
  }
  25%, 100% {
    opacity: 0;
    transform: scaleX(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut`

```css
@keyframes fadeOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes quicksand-off`

```css
@keyframes quicksand-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-off`

```css
@keyframes quicksand-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-on`

```css
@keyframes quicksand-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-on`

```css
@keyframes quicksand-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut-off`

```css
@keyframes fadeOut-off {
  0% {
    opacity: 1;
  }
  80%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-off`

```css
@keyframes fadeOut-off {
  0% {
    opacity: 1;
  }
  80%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-on`

```css
@keyframes fadeOut-on {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-on`

```css
@keyframes fadeOut-on {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes flipOut-out`

```css
@keyframes flipOut-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateY(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-out`

```css
@keyframes flipOut-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateY(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-in`

```css
@keyframes flipOut-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateY(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-in`

```css
@keyframes flipOut-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateY(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-out`

```css
@keyframes flipBottom-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateX(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-out`

```css
@keyframes flipBottom-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateX(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-in`

```css
@keyframes flipBottom-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateX(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-in`

```css
@keyframes flipBottom-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateX(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-out`

```css
@keyframes scaleSides-out {
  50%, 100% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-out`

```css
@keyframes scaleSides-out {
  50%, 100% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-in`

```css
@keyframes scaleSides-in {
  0%, 50% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-in`

```css
@keyframes scaleSides-in {
  0%, 50% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-off`

```css
@keyframes skew-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(20deg, 0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-off`

```css
@keyframes skew-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(20deg, 0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-on`

```css
@keyframes skew-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(0deg, 20deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-on`

```css
@keyframes skew-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(0deg, 20deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-out`

```css
@keyframes fadeOutTop-out {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  50%, 100% {
    transform: translateY(-30px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-out`

```css
@keyframes fadeOutTop-out {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  50%, 100% {
    transform: translateY(-30px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-in`

```css
@keyframes fadeOutTop-in {
  0%, 50% {
    transform: translateY(-30px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-in`

```css
@keyframes fadeOutTop-in {
  0%, 50% {
    transform: translateY(-30px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-out`

```css
@keyframes slideLeft-out {
  0% {
    opacity: 1;
    transform: scale(1);
  }
  25% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
  100% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-out`

```css
@keyframes slideLeft-out {
  0% {
    opacity: 1;
    transform: scale(1);
  }
  25% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
  100% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-in`

```css
@keyframes slideLeft-in {
  0%, 25% {
    opacity: 0.75;
    transform: scale(0.8) translateX(200%);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateX(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-in`

```css
@keyframes slideLeft-in {
  0%, 25% {
    opacity: 0.75;
    transform: scale(0.8) translateX(200%);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateX(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out`

```css
@keyframes flip-out {
  100% {
    opacity: 0;
    transform: rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out`

```css
@keyframes flip-out {
  100% {
    opacity: 0;
    transform: rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in`

```css
@keyframes flip-in {
  0% {
    opacity: 0;
    transform: rotateY(-90deg);
  }
  100% {
    opacity: 1;
    transform: rotateY(0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in`

```css
@keyframes flip-in {
  0% {
    opacity: 0;
    transform: rotateY(-90deg);
  }
  100% {
    opacity: 1;
    transform: rotateY(0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideDelay-out`

```css
@keyframes slideDelay-out {
  100% {
    transform: translateX(-100%);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-out`

```css
@keyframes slideDelay-out {
  100% {
    transform: translateX(-100%);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-in`

```css
@keyframes slideDelay-in {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-in`

```css
@keyframes slideDelay-in {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes rotateSides-out`

```css
@keyframes rotateSides-out {
  100% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-out`

```css
@keyframes rotateSides-out {
  100% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-in`

```css
@keyframes rotateSides-in {
  0% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
  40% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-in`

```css
@keyframes rotateSides-in {
  0% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
  40% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-out`

```css
@keyframes foldLeft-out {
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-out`

```css
@keyframes foldLeft-out {
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-in`

```css
@keyframes foldLeft-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-in`

```css
@keyframes foldLeft-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-out`

```css
@keyframes unfold-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-out`

```css
@keyframes unfold-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-in`

```css
@keyframes unfold-in {
  0% {
    opacity: 0;
    transform: translateX(100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-in`

```css
@keyframes unfold-in {
  0% {
    opacity: 0;
    transform: translateX(100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-out`

```css
@keyframes scaleDown-out {
  100% {
    opacity: 0;
    transform: scale(0.8);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-out`

```css
@keyframes scaleDown-out {
  100% {
    opacity: 0;
    transform: scale(0.8);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-in`

```css
@keyframes scaleDown-in {
  0% {
    transform: translateX(100%);
  }
}
```

> Transform/motion animation

### `@keyframes scaleDown-in`

```css
@keyframes scaleDown-in {
  0% {
    transform: translateX(100%);
  }
}
```

> Transform/motion animation

### `@keyframes frontRow-out`

```css
@keyframes frontRow-out {
  100% {
    transform: translateX(-60%) scale(0.8);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-out`

```css
@keyframes frontRow-out {
  100% {
    transform: translateX(-60%) scale(0.8);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-in`

```css
@keyframes frontRow-in {
  0% {
    transform: translateX(100%) scale(0.8);
  }
  100% {
    opacity: 1;
    transform: translateX(0%) scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-in`

```css
@keyframes frontRow-in {
  0% {
    transform: translateX(100%) scale(0.8);
  }
  100% {
    opacity: 1;
    transform: translateX(0%) scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-out`

```css
@keyframes rotateRoom-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-out`

```css
@keyframes rotateRoom-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-in`

```css
@keyframes rotateRoom-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-in`

```css
@keyframes rotateRoom-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-out`

```css
@keyframes bounceBottom-out {
  100% {
    transform: translateY(100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-out`

```css
@keyframes bounceBottom-out {
  100% {
    transform: translateY(100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-in`

```css
@keyframes bounceBottom-in {
  0% {
    transform: translateY(100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-in`

```css
@keyframes bounceBottom-in {
  0% {
    transform: translateY(100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-out`

```css
@keyframes bounceLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-out`

```css
@keyframes bounceLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-in`

```css
@keyframes bounceLeft-in {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-in`

```css
@keyframes bounceLeft-in {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-out`

```css
@keyframes bounceTop-out {
  100% {
    transform: translateY(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-out`

```css
@keyframes bounceTop-out {
  100% {
    transform: translateY(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-in`

```css
@keyframes bounceTop-in {
  0% {
    transform: translateY(-100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-in`

```css
@keyframes bounceTop-in {
  0% {
    transform: translateY(-100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-out`

```css
@keyframes moveLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-out`

```css
@keyframes moveLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-in`

```css
@keyframes moveLeft-in {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-in`

```css
@keyframes moveLeft-in {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInBottomToTop`

```css
@keyframes fadeInBottomToTop {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInBottomToTop`

```css
@keyframes fadeInBottomToTop {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeInToTop`

```css
@keyframes fadeInToTop {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInToTop`

```css
@keyframes fadeInToTop {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes kenburns`

```css
@keyframes kenburns {
  0% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes kenburns`

```css
@keyframes kenburns {
  0% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownLeft`

```css
@keyframes kenburnsDownLeft {
  0% {
    transform: scale(1.5) translate(10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownLeft`

```css
@keyframes kenburnsDownLeft {
  0% {
    transform: scale(1.5) translate(10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownRight`

```css
@keyframes kenburnsDownRight {
  0% {
    transform: scale(1.5) translate(-10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownRight`

```css
@keyframes kenburnsDownRight {
  0% {
    transform: scale(1.5) translate(-10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDown`

```css
@keyframes kenburnsDown {
  0% {
    transform: scale(1.5) translate(0px, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDown`

```css
@keyframes kenburnsDown {
  0% {
    transform: scale(1.5) translate(0px, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsLeft`

```css
@keyframes kenburnsLeft {
  0% {
    transform: scale(1.5) translate(10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsLeft`

```css
@keyframes kenburnsLeft {
  0% {
    transform: scale(1.5) translate(10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsRight`

```css
@keyframes kenburnsRight {
  0% {
    transform: scale(1.5) translate(-10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsRight`

```css
@keyframes kenburnsRight {
  0% {
    transform: scale(1.5) translate(-10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpLeft`

```css
@keyframes kenburnsUpLeft {
  0% {
    transform: scale(1.5) translate(10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpLeft`

```css
@keyframes kenburnsUpLeft {
  0% {
    transform: scale(1.5) translate(10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpRight`

```css
@keyframes kenburnsUpRight {
  0% {
    transform: scale(1.5) translate(-10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpRight`

```css
@keyframes kenburnsUpRight {
  0% {
    transform: scale(1.5) translate(-10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUp`

```css
@keyframes kenburnsUp {
  0% {
    transform: scale(1.5) translate(0px, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUp`

```css
@keyframes kenburnsUp {
  0% {
    transform: scale(1.5) translate(0px, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes fade`

```css
@keyframes fade {
  0% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade`

```css
@keyframes fade {
  0% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes rev-ani-mouse`

```css
@keyframes rev-ani-mouse {
  0% {
    opacity: 1;
    top: 29%;
  }
  15% {
    opacity: 1;
    top: 70%;
  }
  50% {
    opacity: 0;
    top: 70%;
  }
  100% {
    opacity: 0;
    top: 29%;
  }
}
```

> Opacity fade

### `@keyframes tp-rotateplane`

```css
@keyframes tp-rotateplane {
  0% {
    transform: perspective(120px) rotateX(0deg) rotateY(0deg);
  }
  50% {
    transform: perspective(120px) rotateX(-180.1deg) rotateY(0deg);
  }
  100% {
    transform: perspective(120px) rotateX(-180deg) rotateY(-179.9deg);
  }
}
```

> Transform/motion animation

### `@keyframes tp-scaleout`

```css
@keyframes tp-scaleout {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes tp-bouncedelay`

```css
@keyframes tp-bouncedelay {
  0%, 80%, 100% {
    transform: scale(0);
  }
  40% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes tp-rotate`

```css
@keyframes tp-rotate {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes tp-bounce`

```css
@keyframes tp-bounce {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-6`

```css
@keyframes rs-revealer-6 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-6`

```css
@keyframes rs-revealer-6 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-7`

```css
@keyframes rs-revealer-7 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-7`

```css
@keyframes rs-revealer-7 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-8`

```css
@keyframes rs-revealer-8 {
  0% {
    transform: scale(0, 0);
    opacity: 0.5;
  }
  100% {
    transform: scale(1, 1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rs-revealer-8`

```css
@keyframes rs-revealer-8 {
  0% {
    transform: scale(0, 0);
    opacity: 0.5;
  }
  100% {
    transform: scale(1, 1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rs-revealer-9`

```css
@keyframes rs-revealer-9 {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-9`

```css
@keyframes rs-revealer-9 {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-10`

```css
@keyframes rs-revealer-10 {
  0%, 100%, 40% {
    transform: scaleY(0.4);
  }
  20% {
    transform: scaleY(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-10`

```css
@keyframes rs-revealer-10 {
  0%, 100%, 40% {
    transform: scaleY(0.4);
  }
  20% {
    transform: scaleY(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-11`

```css
@keyframes rs-revealer-11 {
  0%, 100%, 70% {
    transform: scale3d(1, 1, 1);
  }
  35% {
    transform: scale3d(0, 0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-11`

```css
@keyframes rs-revealer-11 {
  0%, 100%, 70% {
    transform: scale3d(1, 1, 1);
  }
  35% {
    transform: scale3d(0, 0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-12`

```css
@keyframes rs-revealer-12 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-12`

```css
@keyframes rs-revealer-12 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-13`

```css
@keyframes rs-revealer-13 {
  0%, 100% {
    transform: translate(0px);
  }
  25% {
    transform: translate(160%);
  }
  50% {
    transform: translate(160%, 160%);
  }
  75% {
    transform: translate(0px, 160%);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-13`

```css
@keyframes rs-revealer-13 {
  0%, 100% {
    transform: translate(0px);
  }
  25% {
    transform: translate(160%);
  }
  50% {
    transform: translate(160%, 160%);
  }
  75% {
    transform: translate(0px, 160%);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-1`

```css
@keyframes rs-revealer-14-1 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-2`

```css
@keyframes rs-revealer-14-2 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-3`

```css
@keyframes rs-revealer-14-3 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-4`

```css
@keyframes rs-revealer-14-4 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-1`

```css
@keyframes rs-revealer-14-1 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-2`

```css
@keyframes rs-revealer-14-2 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-3`

```css
@keyframes rs-revealer-14-3 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-4`

```css
@keyframes rs-revealer-14-4 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-15`

```css
@keyframes rs-revealer-15 {
  25% {
    transform: translateX(30px) rotate(-90deg) scale(0.5);
  }
  50% {
    transform: translateX(30px) translateY(30px) rotate(-180deg);
  }
  75% {
    transform: translateX(0px) translateY(30px) rotate(-270deg) scale(0.5);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-15`

```css
@keyframes rs-revealer-15 {
  25% {
    transform: translateX(30px) rotate(-90deg) scale(0.5);
  }
  50% {
    transform: translateX(30px) translateY(30px) rotate(-179deg);
  }
  50.1% {
    transform: translateX(30px) translateY(30px) rotate(-180deg);
  }
  75% {
    transform: translateX(0px) translateY(30px) rotate(-270deg) scale(0.5);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

## Motion Tokens (CSS Variables)

### Duration Tokens

```css
--nfd-wb-anim-transition-duration: 1400ms;
```

### Delay Tokens

```css
--nfd-wb-anim-transition-delay: 50ms;
```

### Other Tokens

```css
--nfd-wb-anim-transition-easing-function: cubic-bezier(0.4,1,0.65,1);
--nfd-wb-anim-transition: all var(--nfd-wb-anim-transition-duration) var(--nfd-wb-anim-transition-easing-function) var(--nfd-wb-anim-transition-delay);
```

## Global Transition Declarations

These `transition` values were extracted from CSS rules across the site:

```css
transition: 0.3s;
transition: background 0.3s, color 0.3s;
transition: width 0.35s cubic-bezier(0.35, 0.7, 0.35, 1);
transition: transform 0.3s;
transition: transform 0.35s, opacity 0.35s;
transition: color 0.3s, opacity 0.3s, left 0.3s;
transition: background-color 0.2s linear;
transition: opacity 80ms, transform linear 81ms;
transition: background-color 0.3s ease-out;
transition: height 0.2s ease-out;
transition: transform 0.6s ease-in-out;
transition: var(--nfd-wb-anim-transition);
```

## How to Recreate This Motion Design

### Step 2 — Scroll-Reveal Pattern

Elements that animate into view follow this pattern:

```css
/* Initial hidden state */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 1400ms cubic-bezier(0.4, 0, 0.2, 1),
              transform 1400ms cubic-bezier(0.4, 0, 0.2, 1);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### Step 3 — Key Motion Principles

- **Duration scale:** `1400ms` · `0.3s` · `0.35s` — use these values, never invent new durations
- **Always add** `@media (prefers-reduced-motion: reduce) { * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }`

### Step 4 — Scroll Journey Reference

Match what happens at each scroll position:

- **0%** (`0px`) → `screens/scroll/scroll-000.png`
- **17%** (`891px`) → `screens/scroll/scroll-017.png`
- **33%** (`1731px`) → `screens/scroll/scroll-033.png`
- **50%** (`2622px`) → `screens/scroll/scroll-050.png`
- **67%** (`3447px`) → `screens/scroll/scroll-067.png`
- **83%** (`3447px`) → `screens/scroll/scroll-083.png`
- **100%** (`3447px`) → `screens/scroll/scroll-100.png`

## Layout & Grid (LAYOUT.md)

# Layout Reference

> Auto-extracted from live DOM. Use this to understand how the site is structured spatially.

## Spacing System

**Base grid:** 5px

**Scale:** `5, 10, 15, 20, 25, 30, 35, 40, 50, 60, 70, 80, 85, 95, 100` px

| Spacing | Semantic Use |
|---------|-------------|
| 5px | Tight — within a component |
| 10px | Medium — between sibling items |
| 20px | Wide — between sections |
| 40px | Vast — major section breaks |

## Flex Layouts

| Element | Direction | Justify | Align | Gap | Children |
|---------|-----------|---------|-------|-----|----------|
| `div.row-inner.clearfix` | row | — | end | — | 1 |
| `div.vc_column-inner` | row | — | end | — | 1 |

## Structural Containers

### `<footer>` (`footer#footer`)

```
display:          block
padding:          114px 0px 50px
children:         1
```

### `<header>` (`header#site-header`)

```
display:          block
children:         1
```

### `<article>` (`article.page-content.post-13588`)

```
display:          block
children:         1
```

### `<nav>` (`nav#main-nav.main-nav`)

```
display:          block
children:         1
```

### `<section>` (`section#sobrenos.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section#solucoes.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

## Layout Rules

- **Container max-width:** `90%` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Every spacing value must be a multiple of **5px**
- Never use arbitrary margin/padding values outside the spacing scale

## Component Patterns (COMPONENTS.md)

# Component Reference

> Repeated DOM patterns detected by structural analysis. Each component appeared 3+ times.

## Detected Components

| Component | Category | Instances | Key Classes |
|-----------|----------|-----------|-------------|
| **Vc Column Inner** | unknown | 9× | `.vc_column-inner` |
| **Clearfix** | unknown | 8× | `.clearfix`, `.heading` |
| **Wpb Wrapper** | unknown | 6× | `.wpb_wrapper` |
| **Agrikole Content Box** | unknown | 6× | `.agrikole-content-box`, `.clearfix` |
| **Agrikole Container** | unknown | 5× | `.agrikole-container` |
| **Entered** | unknown | 4× | `.entered`, `.error`, `.perfmatters-lazy` |
| **Clearfix** | unknown | 4× | `.clearfix`, `.vc-col-spacing-30`, `.vc-custom-col-spacing` |
| **Clearfix** | unknown | 4× | `.clearfix`, `.row-inner` |
| **Clearfix** | unknown | 4× | `.clearfix`, `.vc-col-inner-spacing-30`, `.vc-custom-col-inner-spacing` |
| **Wpb Wrapper** | unknown | 4× | `.wpb_wrapper` |
| **Vc Col Sm 12** | unknown | 3× | `.vc_col-sm-12`, `.vc_column_container`, `.wpb_column` |
| **Clearfix** | unknown | 3× | `.clearfix`, `.pre-heading` |
| **Clearfix** | unknown | 3× | `.clearfix`, `.sep` |
| **Wpb Wrapper** | unknown | 3× | `.wpb_wrapper` |
| **Vc Col Has Fill** | unknown | 3× | `.vc_col-has-fill`, `.vc_col-sm-4`, `.vc_column_container` |
| **Vc Figure** | unknown | 3× | `.vc_figure`, `.wpb_wrapper` |
| **Vc Box Border Grey** | unknown | 3× | `.vc_box_border_grey`, `.vc_single_image-wrapper` |
| **Attachment Full** | unknown | 3× | `.attachment-full`, `.entered`, `.error` |
| **Agrikole Headings** | unknown | 3× | `.agrikole-headings`, `.clearfix`, `.text-center` |
| **Wpb Content Element** | unknown | 3× | `.wpb_content_element`, `.wpb_text_column` |

## Other Components

### Vc Column Inner

**Instances found:** 9

**CSS classes:** `.vc_column-inner`

**HTML structure:**

```html
<div class="vc_column-inner"><div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="60" style=""><div class="pre-heading clearfix" style="font-weight:600;color:#83c75d;font-
```

**Base styles (from design tokens):**

```css
.vc_column-inner {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 8

**CSS classes:** `.clearfix` `.heading`

**HTML structure:**

```html
<h2 class="heading clearfix" style="line-height:70px;font-size:70px;"> QUEM SOMOS </h2>
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Wpb Wrapper

**Instances found:** 6

**CSS classes:** `.wpb_wrapper`

**HTML structure:**

```html
<div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="60" style=""><div class="pre-heading clearfix" style="font-weight:600;color:#83c75d;font-size:14px;letter-spacing:3px;
```

**Base styles (from design tokens):**

```css
.wpb_wrapper {
  background: #f5f0e9;
  padding: 5px;
}```

### Agrikole Content Box

**Instances found:** 6

**CSS classes:** `.agrikole-content-box` `.clearfix`

**HTML structure:**

```html
<div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="60" style=""><div class="pre-heading clearfix" style="font-weight:600;color:#83c75d;font-size:14px;letter-spacing:3px;font-family:Montserrat;"> conheça </div><h2 class="heading clearfix" style="line-height:70px;font-size:70px;"> QUEM SOMO
```

**Base styles (from design tokens):**

```css
.agrikole-content-box {
  background: #f5f0e9;
  padding: 5px;
}```

### Agrikole Container

**Instances found:** 5

**CSS classes:** `.agrikole-container`

**HTML structure:**

```html
<div class="agrikole-container"><div class="row-inner clearfix"><div class="wpb_column vc_column_container vc_col-sm-12"><div class="vc_column-inner"><div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clear
```

**Base styles (from design tokens):**

```css
.agrikole-container {
  background: #f5f0e9;
  padding: 5px;
}```

### Entered

**Instances found:** 4

**CSS classes:** `.entered` `.error` `.perfmatters-lazy`

**HTML structure:**

```html
<img width="510" height="200" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%20510%20200&amp;apos;%3E%3C/svg%3E" alt="Núcleo Rural | Suplementos Nutracêuticos para Gado de Corte e Leite" data-lazy-src="https://nucleorural.com.br/wp-content/webp-express/webp-images/uploads/2024/08/Copia-de-1716833208340-1a36cdb4-7f84-4027-b4a9-82cd88ea46e0_1-removebg-preview-1-e1723642499206.png.webp" class="perfmatters-lazy entered error" data-src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apo
```

**Base styles (from design tokens):**

```css
.entered {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 4

**CSS classes:** `.clearfix` `.vc-col-spacing-30` `.vc-custom-col-spacing`

**HTML structure:**

```html
<div class="vc-custom-col-spacing clearfix vc-col-spacing-30"><section id="sobrenos" class="wpb_row vc_row-fluid row-content-position-Default"><div class="agrikole-container"><div class="row-inner clearfix"><div class="wpb_column vc_column_container vc_col-sm-12"><div class="vc_column-inner"><div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_c
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 4

**CSS classes:** `.clearfix` `.row-inner`

**HTML structure:**

```html
<div class="row-inner clearfix"><div class="wpb_column vc_column_container vc_col-sm-12"><div class="vc_column-inner"><div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 4

**CSS classes:** `.clearfix` `.vc-col-inner-spacing-30` `.vc-custom-col-inner-spacing`

**HTML structure:**

```html
<div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="60" style=""><div class="pre-heading clearfix" style="font-weight:600;color:#83c75d;font-size:14px;letter-spacing:3px;font-family:Montserrat;"> conheça </div><h2 class="heading clearfix" style="line-height:70px;font-size:70px;"> QUEM SOMOS </h2><div class="sub-heading clearfix"> <
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Wpb Wrapper

**Instances found:** 4

**CSS classes:** `.wpb_wrapper`

**HTML structure:**

```html
<div class="wpb_wrapper"> <p>A Núcleo Rural é uma empresa dedicada a …</p> </div>
```

**Base styles (from design tokens):**

```css
.wpb_wrapper {
  background: #f5f0e9;
  padding: 5px;
}```

### Vc Col Sm 12

**Instances found:** 3

**CSS classes:** `.vc_col-sm-12` `.vc_column_container` `.wpb_column`

**HTML structure:**

```html
<div class="wpb_column vc_column_container vc_col-sm-12"><div class="vc_column-inner"><div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="112" data-mobi="60" data-smobi="60"></div><div class="agrikole-content-box clearfix"><div class="vc-custom-col-inner-spacing clearfix vc-col-inner-spacing-30"><div class="wpb_row vc_inner vc_row-fluid"><div class="wpb_column vc_column_container vc_col-sm-6 vc_col-xs-1 vc_hidden-xs"><div class="vc_column-inner"><div class="wpb_wrapper"><div class="agrikole-headings clearfix" data-font="70" data-mfont="60" style=""><div class="pre-hea
```

**Base styles (from design tokens):**

```css
.vc_col-sm-12 {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 3

**CSS classes:** `.clearfix` `.pre-heading`

**HTML structure:**

```html
<div class="pre-heading clearfix" style="font-weight:600;color:#83c75d;font-size:14px;letter-spacing:3px;font-family:Montserrat;"> conheça </div>
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Clearfix

**Instances found:** 3

**CSS classes:** `.clearfix` `.sep`

**HTML structure:**

```html
<div class="sep clearfix" style="margin:5px 0 0;"> <img width="55" height="22" decoding="async" alt="image" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%2055%2022&amp;apos;%3E%3C/svg%3E" data-lazy-src="https://nucleorural.com.br/wp-content/webp-express/webp-images/uploads/2020/01/separator.png.webp" class="perfmatters-lazy entered error" data-src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%2055%2022&amp;apos;%3E%3C/svg%3E" data-ll-status="error"><noscript><img widt
```

**Base styles (from design tokens):**

```css
.clearfix {
  background: #f5f0e9;
  padding: 5px;
}```

### Wpb Wrapper

**Instances found:** 3

**CSS classes:** `.wpb_wrapper`

**HTML structure:**

```html
<div class="wpb_wrapper"> <div class="agrikole-spacer clearfix" data-desktop="30" data-mobi="50" data-smobi="50"></div><div class="agrikole-simple-image reveal wow lr"> <figure style="border-radius:5px;overflow:hidden;"><img width="1280" height="960" decoding="async" alt="image" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%201280%20960&amp;apos;%3E%3C/svg%3E" data-lazy-src="https://nucleorural.com.br/wp-content/webp-express/webp-images/uploads/2024/08/Design-sem-nome-7.png.webp" class="perfmatters-lazy entered error" data-src="
```

**Base styles (from design tokens):**

```css
.wpb_wrapper {
  background: #f5f0e9;
  padding: 5px;
}```

### Vc Col Has Fill

**Instances found:** 3

**CSS classes:** `.vc_col-has-fill` `.vc_col-sm-4` `.vc_column_container` `.wpb_column`

**HTML structure:**

```html
<div class="wpb_column vc_column_container vc_col-sm-4 vc_col-has-fill"><div class="vc_column-inner vc_custom_1728437542923"><div class="wpb_wrapper"> <div class="wpb_single_image wpb_content_element vc_align_left wpb_content_element vc_custom_1728437387823"> <figure class="wpb_wrapper vc_figure"> <a href="https://nucleorural.com.br/project/aumento-na-producao-de-carne/" target="_self" class="vc_single_image-wrapper vc_box_border_grey"><img decoding="async" width="734" height="787" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%2
```

**Base styles (from design tokens):**

```css
.vc_col-has-fill {
  background: #f5f0e9;
  padding: 5px;
}```

### Vc Figure

**Instances found:** 3

**CSS classes:** `.vc_figure` `.wpb_wrapper`

**HTML structure:**

```html
<figure class="wpb_wrapper vc_figure"> <a href="https://nucleorural.com.br/project/aumento-na-producao-de-carne/" target="_self" class="vc_single_image-wrapper vc_box_border_grey"><img decoding="async" width="734" height="787" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%20734%20787&amp;apos;%3E%3C/svg%3E" class="vc_single_image-img attachment-full perfmatters-lazy entered error" alt="Suplemento para gado de corte Master Engorda da Núcleo Rural promovendo ganho de peso eficiente em bovinos." title="Cópia de MASTER ENGORDA" data
```

**Base styles (from design tokens):**

```css
.vc_figure {
  background: #f5f0e9;
  padding: 5px;
}```

### Vc Box Border Grey

**Instances found:** 3

**CSS classes:** `.vc_box_border_grey` `.vc_single_image-wrapper`

**HTML structure:**

```html
<a href="https://nucleorural.com.br/project/aumento-na-producao-de-carne/" target="_self" class="vc_single_image-wrapper vc_box_border_grey"><img decoding="async" width="734" height="787" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%20734%20787&amp;apos;%3E%3C/svg%3E" class="vc_single_image-img attachment-full perfmatters-lazy entered error" alt="Suplemento para gado de corte Master Engorda da Núcleo Rural promovendo ganho de peso eficiente em bovinos." title="Cópia de MASTER ENGORDA" data-lazy-srcset="https://nucleorural.com.b
```

**Base styles (from design tokens):**

```css
.vc_box_border_grey {
  background: #f5f0e9;
  padding: 5px;
}```

### Attachment Full

**Instances found:** 3

**CSS classes:** `.attachment-full` `.entered` `.error` `.perfmatters-lazy` `.vc_single_image-img`

**HTML structure:**

```html
<img decoding="async" width="734" height="787" src="data:image/svg+xml,%3Csvg%20xmlns=&amp;apos;http://www.w3.org/2000/svg&amp;apos;%20viewBox=&amp;apos;0%200%20734%20787&amp;apos;%3E%3C/svg%3E" class="vc_single_image-img attachment-full perfmatters-lazy entered error" alt="Suplemento para gado de corte Master Engorda da Núcleo Rural promovendo ganho de peso eficiente em bovinos." title="Cópia de MASTER ENGORDA" data-lazy-srcset="https://nucleorural.com.br/wp-content/webp-express/webp-images/uploads/2020/02/Copia-de-MASTER-ENGORDA.png.webp 734w, https://nucleorural.com.br/wp-content/webp-expre
```

**Base styles (from design tokens):**

```css
.attachment-full {
  background: #f5f0e9;
  padding: 5px;
}```

### Agrikole Headings

**Instances found:** 3

**CSS classes:** `.agrikole-headings` `.clearfix` `.text-center`

**HTML structure:**

```html
<div class="agrikole-headings clearfix text-center" style=""><h2 class="heading clearfix" style=""> Aumento na Produção de Carne </h2></div>
```

**Base styles (from design tokens):**

```css
.agrikole-headings {
  background: #f5f0e9;
  padding: 5px;
}```

### Wpb Content Element

**Instances found:** 3

**CSS classes:** `.wpb_content_element` `.wpb_text_column`

**HTML structure:**

```html
<div class="wpb_text_column wpb_content_element"> <div class="wpb_wrapper"> <p style="text-align: center;"><span>MASTER ENGORDA é um nutraceutico a base …</span></p> </div> </div>
```

**Base styles (from design tokens):**

```css
.wpb_content_element {
  background: #f5f0e9;
  padding: 5px;
}```

## Component Rules

- Match class names exactly from the patterns above
- Each component instance must be visually identical to others of its type
- Do not add extra wrappers or change the DOM structure
- Use `#404a3d` for all dividers within components
- Use `#00d084` for all interactive/active states

## Interactions & States (INTERACTIONS.md)

# Interaction Reference

> Micro-interactions extracted from live DOM. Recreate these exactly for authentic feel.

## Coverage

| Component Type | Count | States Captured |
|----------------|-------|----------------|
| Link | 3 | default, hover, focus |

## Transition System

These transition declarations were extracted from interactive elements:

```css
transition: 0.3s;
```

Apply these to all interactive elements. Never invent new durations or easings.

## Link Interactions

### Link 1 — `a`

**States:**

- Default: `../screens/states/link-1-default.png`
- Hover: `../screens/states/link-1-hover.png`
- Focus: `../screens/states/link-1-focus.png`

**On hover:**

```css
/* color: rgb(131, 199, 93) → */ color: rgb(64, 74, 61);
/* border-color: rgb(131, 199, 93) → */ border-color: rgb(64, 74, 61);
/* outline: rgb(131, 199, 93) none 0px → */ outline: rgb(64, 74, 61) none 0px;
/* outline-color: rgb(131, 199, 93) → */ outline-color: rgb(64, 74, 61);
```

**On focus:**

```css
/* color: rgb(131, 199, 93) → */ color: rgb(64, 74, 61);
/* border-color: rgb(131, 199, 93) → */ border-color: rgb(64, 74, 61);
/* outline: rgb(131, 199, 93) none 0px → */ outline: rgb(64, 74, 61) none 0px;
/* outline-color: rgb(131, 199, 93) → */ outline-color: rgb(64, 74, 61);
```

**Transition:** `0.3s`

### Link 2 — `home`

**States:**

- Default: `../screens/states/link-2-default.png`
- Hover: `../screens/states/link-2-hover.png`
- Focus: `../screens/states/link-2-focus.png`

**Transition:** `0.3s`

_No visible style changes detected for this element._

### Link 3 — `Últimas Notícias`

**States:**

- Default: `../screens/states/link-3-default.png`
- Hover: `../screens/states/link-3-hover.png`
- Focus: `../screens/states/link-3-focus.png`

**Transition:** `0.3s`

_No visible style changes detected for this element._

## Interaction Rules

- Accent color `#00d084` is used for focus rings, active states, and hover highlights
- Hover effects include **color transitions** — use the extracted values, not approximations
- Focus states use **outline** (not box-shadow) — always match the extracted focus ring
- Transition durations in use: `0.3s`
- Always respect `prefers-reduced-motion` — set all transitions to `0s` when enabled

## Design Tokens — JSON Files

### tokens/colors.json
```json
{
  "$schema": "https://design-tokens.github.io/community-group/format/",
  "core": {
    "text-muted": {
      "value": "#878986",
      "role": "text-muted"
    },
    "text-primary": {
      "value": "#043038",
      "role": "text-primary"
    },
    "background": {
      "value": "#ffffff",
      "role": "background",
      "name": "wp--preset--color--white"
    },
    "border": {
      "value": "#404a3d",
      "role": "border"
    },
    "surface": {
      "value": "#f5f0e9",
      "role": "surface"
    },
    "accent": {
      "value": "#00d084",
      "role": "accent",
      "name": "wp--preset--color--vivid-green-cyan"
    }
  },
  "status": {
    "success": {
      "value": "#83c75d",
      "role": "success"
    },
    "warning": {
      "value": "#eddd5e",
      "role": "warning"
    },
    "danger": {
      "value": "#ff4539",
      "role": "danger"
    }
  },
  "extended": {
    "color-5b8c51": {
      "value": "#5b8c51",
      "role": "unknown"
    },
    "color-c5c9c4": {
      "value": "#c5c9c4",
      "role": "unknown"
    },
    "wp--preset--color--black": {
      "value": "#000000",
      "role": "unknown",
      "name": "wp--preset--color--black"
    },
    "color-313131": {
      "value": "#313131",
      "role": "unknown"
    },
    "wp-editor-canvas-background": {
      "value": "#dddddd",
      "role": "unknown",
      "name": "wp-editor-canvas-background"
    },
    "color-128c7e": {
      "value": "#128c7e",
      "role": "unknown"
    },
    "wp--preset--color--vivid-cyan-blue": {
      "value": "#0693e3",
      "role": "info",
      "name": "wp--preset--color--vivid-cyan-blue"
    },
    "wndb--color--primary": {
      "value": "#0000ff",
      "role": "unknown",
      "name": "wndb--color--primary"
    },
    "color-25d366": {
      "value": "#25d366",
      "role": "unknown"
    },
    "color-4a4a4a": {
      "value": "#4a4a4a",
      "role": "unknown"
    },
    "color-252a24": {
      "value": "#252a24",
      "role": "unknown"
    }
  },
  "meta": {
    "theme": "light",
    "extracted": "2026-08-25"
  }
}
```

### tokens/spacing.json
```json
{
  "base": {
    "value": "5px",
    "description": "Grid unit — all spacing must be multiples of this"
  },
  "unit": "px",
  "scale": {
    "xs": {
      "value": "5px",
      "px": 5
    },
    "sm": {
      "value": "10px",
      "px": 10
    },
    "md": {
      "value": "15px",
      "px": 15
    },
    "lg": {
      "value": "20px",
      "px": 20
    },
    "xl": {
      "value": "25px",
      "px": 25
    },
    "2xl": {
      "value": "30px",
      "px": 30
    },
    "3xl": {
      "value": "35px",
      "px": 35
    },
    "4xl": {
      "value": "40px",
      "px": 40
    },
    "5xl": {
      "value": "50px",
      "px": 50
    },
    "6xl": {
      "value": "60px",
      "px": 60
    }
  },
  "multipliers": {
    "1x": {
      "value": "5px",
      "raw": 5
    },
    "2x": {
      "value": "10px",
      "raw": 10
    },
    "3x": {
      "value": "15px",
      "raw": 15
    },
    "4x": {
      "value": "20px",
      "raw": 20
    },
    "5x": {
      "value": "25px",
      "raw": 25
    },
    "6x": {
      "value": "30px",
      "raw": 30
    },
    "7x": {
      "value": "35px",
      "raw": 35
    },
    "8x": {
      "value": "40px",
      "raw": 40
    },
    "9x": {
      "value": "45px",
      "raw": 45
    },
    "10x": {
      "value": "50px",
      "raw": 50
    },
    "11x": {
      "value": "55px",
      "raw": 55
    },
    "12x": {
      "value": "60px",
      "raw": 60
    },
    "13x": {
      "value": "65px",
      "raw": 65
    },
    "14x": {
      "value": "70px",
      "raw": 70
    },
    "15x": {
      "value": "75px",
      "raw": 75
    },
    "16x": {
      "value": "80px",
      "raw": 80
    }
  },
  "meta": {
    "totalValues": 15,
    "min": 5,
    "max": 100
  }
}
```

### tokens/typography.json
```json
{
  "families": [
    "Pe-icon-7-stroke",
    "AgrikoleIcons"
  ],
  "scale": {
    "heading-1": {
      "fontFamily": "Pe-icon-7-stroke",
      "fontSize": "70px",
      "fontWeight": "700",
      "lineHeight": null,
      "source": "css"
    },
    "heading-2": {
      "fontFamily": "Pe-icon-7-stroke",
      "fontSize": "50px",
      "fontWeight": "700",
      "lineHeight": null,
      "source": "css"
    },
    "heading-3": {
      "fontFamily": "Pe-icon-7-stroke",
      "fontSize": "40px",
      "fontWeight": "700",
      "lineHeight": null,
      "source": "css"
    },
    "body": {
      "fontFamily": "AgrikoleIcons",
      "fontSize": "16px",
      "fontWeight": "400",
      "lineHeight": null,
      "source": "css"
    },
    "caption": {
      "fontFamily": "AgrikoleIcons",
      "fontSize": "18px",
      "fontWeight": "400",
      "lineHeight": null,
      "source": "css"
    }
  },
  "fontFaces": [
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/agrikoleicons/AgrikoleIcons.svg#AgrikoleIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/pe7s/Pe-icon-7-stroke.svg?d7yf1v#Pe-icon-7-stroke",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../plugins/wprt-addons/assets/eleganticons/ElegantIcons.svg#ElegantIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.ttf?onqajd",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.woff?onqajd",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_icons_v3/fonts/vcpb-plugin-icons.svg?onqajd#vcpb-plugin-icons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.eot?-9hbgac",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.eot?#iefix-9hbgac",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.woff?-9hbgac",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.ttf?-9hbgac",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/js_composer/assets/css/../../../../../../../../../../../../plugins/js_composer/assets/fonts/vc_grid/vc_grid_v1.svg?-9hbgac#vc_grid_v1",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/eleganticons/ElegantIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/eleganticons/ElegantIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/eleganticons/ElegantIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/eleganticons/ElegantIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/eleganticons/ElegantIcons.svg#ElegantIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/pe7s/Pe-icon-7-stroke.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/pe7s/Pe-icon-7-stroke.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/pe7s/Pe-icon-7-stroke.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/pe7s/Pe-icon-7-stroke.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/pe7s/Pe-icon-7-stroke.svg?d7yf1v#Pe-icon-7-stroke",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/cache/min/1/wp-content/themes/agrikole/assets/css/../../../../../../../../themes/agrikole/assets/font/coreicon/coreicon.svg?d7yf1v#coreicon",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ytpregular",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../../../../../plugins/wprt-addons/assets/font/ytp-regular.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ytpregular",
      "src": "data:application/x-font-woff;charset=utf-8;base64,d09GRgABAAAAAA5sABEAAAAAFCAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABGRlRNAAABgAAAABwAAAAcZ9iuNUdERUYAAAGcAAAAHQAAACAAdAAET1MvMgAAAbwAAABJAAAAYHUMUrFjbWFwAAACCAAAAKkAAAGKn5XycWN2dCAAAAK0AAAANgAAADYNLQohZnBnbQAAAuwAAAGxAAACZVO0L6dnYXNwAAAEoAAAAAgAAAAIAAAAEGdseWYAAASoAAAGVQAAB4jz86dSaGVhZAAACwAAAAAzAAAANgbKONpoaGVhAAALNAAAACAAAAAkESQLXGhtdHgAAAtUAAAAVAAAARxOmwVwbG9jYQAAC6gAAAAjAAAAkFoEXRRtYXhwAAALzAAAACAAAAAgAWoB625hbWUAAAvsAAAA+wAAAeok3Eb+cG9zdAAADOgAAADAAAABN99tv1lwcmVwAAANqAAAALkAAAFY3I6ikndlYmYAAA5kAAAABgAAAAbHMlGnAAAAAQAAAADMPaLPAAAAAM3Nk7QAAAAAzc13sXjaY2BkYGDgA2IJBhBgYmAEQjcgZgHzGAAHTAB5AAAAeNpjYGbZwDiBgZWBhdWY5SwDA8MsCM10liGNKQ3IB0rBASMDEgj1DvdjcGDgfcDAlvYPqJJVldEZpoZVkuUZkFJgYAQAUUULewAAAHjaY2BgYGaAYBkGRgYQaAHyGMF8FoYMIC3GIAAUYQOyeBkUGKIYqhgWKHAp6CvEP2D4/x+sAyTuyJAIFGeAizP+//r/8f/D//f+n/HA8oHo/WcKblDzsQBGoOkwSUYmIMGErgDiRLyAhZWNnYOTi5uHl49fQFBIWERUTFxCUkpaRhYiLyevoKikrKKqpq6hqaWto6unb2BoZGxiambOQF1gQZYuAIQnH4IAAAAAAAAAAAABegEnAHEAswC9AOAA5QD+ARcBIwBdAHIBtgBcAGAAZgByAI8AogErAbIAUwBEBREAAHjaXVG7TltBEN0NDwOBxNggOdoUs5mQxnuhBQnE1Y1iZDuF5QhpN3KRi3EBH0CBRA3arxmgoaRImwYhF0h8Qj4hEjNriKI0Ozuzc86ZM0vKkap36WvPU+ckkMLdBs02/U5ItbMA96Tr642MtIMHWmxm9Mp1+/4LBpvRlDtqAOU9bykPGU07gVq0p/7R/AqG+/wf8zsYtDTT9NQ6CekhBOabcUuD7xnNussP+oLV4WIwMKSYpuIuP6ZS/rc052rLsLWR0byDMxH5yTRAU2ttBJr+1CHV83EUS5DLprE2mJiy/iQTwYXJdFVTtcz42sFdsrPoYIMqzYEH2MNWeQweDg8mFNK3JMosDRH2YqvECBGTHAo55dzJ/qRA+UgSxrxJSjvjhrUGxpHXwKA2T7P/PJtNbW8dwvhZHMF3vxlLOvjIhtoYEWI7YimACURCRlX5hhrPvSwG5FL7z0CUgOXxj3+dCLTu2EQ8l7V1DjFWCHp+29zyy4q7VrnOi0J3b6pqqNIpzftezr7HA54eC8NBY8Gbz/v+SoH6PCyuNGgOBEN6N3r/orXqiKu8Fz6yJ9O/sVoAAAAAAQAB//8AD3jaTZVrbBxXFcfvufNe72Nmdx77tmfHO2N76117784OTr154YAbR7RQuUQhttoSuXZKFQVKKYqgiFJAgkpIkVClIn8opSomjXY3VHHTFldEIYpay1hR+ID4Bha27FoIEQGpd8Idu4lY7c6eOfee//2f3+zeizAaQwif4iYRgwRUbgGqjLYFNvVxtcVzfxltM5iGqMUEaS5ItwU+vTPahiBPFFMpmoo5hnv8XnjFn+Um7/xmjF1GCLHoPf+fgsUVEYcSKIcGkYbaWYxKLZ3bgGa50qpACQ0NeyYoYILaDTqpurUK2FZBUYlJY8ukEc0egLpbo+kY8O/BQcx2dvwP2Fh6/Q+Gl19fyroubHmer7rpjHllPZ/NKB+tp2/4/TzxSx0zo/74uUY29vJZOEHIfng4lzz7cjyXzn/jJwqCwCOLdj2iPSP3F/hUAHF3v+Cviee5DIqhJDLRACLoPGpHECq1M7Sd5iDZ/W6zQW8mu9Ecql7SI6xYaiOpnxCydwPNWqWJ/tSSjY1mqtqU5ZYNpWal2pJiGy0XSi1bVuKX1Fyh1GuMoJYeUeJvy/GEVbTpfTOjHJRVzUim0tlcwekbKD1QrgR5M97OV8nIyMjQsKPUEKWGNEVFFBwqEs/yHMEVFMM1PIc4FhiWQVxHcxjD0zzXEkgbmHe5G1eA9T955453xd+B9tbpi6vj10+fvj6+evH0Fju7vPDU5szVY8euzmw+tXABv7kEov/v33WOv+v/C8LG9M2xD19/EquzCyuHVuY6R25Obz35+odw4NDKwuzWHAK86q9x21wKYYQkjFeZ3M5f/TUmw6Qo12P+38Wf0zEZpVABlVANfQu1owHXXMD1AdIyQhvNgeou2b1LAuhAkVwyExRps/ppAE230qrTX1MrEVXil5W4qlm9thMAMpR2MtVHAbXMnBJvZ8oVGjdZ5XK6u6cwNExqdNJ9dnm4D+8eIeYeM7hH0b3H9bcQuczdeH75ef+TxTveO/5tuDK2Mrs5d+HmzQtzm7MrbP6ZqxMrrz2+vf34aysTV5+5iN9YhMi51W93Tiz5/wFp+ujy/MntGXx+dfrjqflrO788Ob989MaMP716+Nr8FOpCjbvnw032BUrm82gKfQc10SJaAwwZGINHEUrksaEndI3XCppBavWaU7Nrda/u7QfPsnmBF1ReK4NjCxbkgVRJdW/MdmiyjHkhCgKvGkrNq+uGngPLUDXVioJTcGxONWguENOIYmkq1lQqaDu2q1AqKi6qRh6CN0uqhlkn1WIwt1Z3FTqH6lt2kWLkqZpQ2F1H4D3X1CzFUkCp1R8EVaeKGr3mgXpyd3OKZTcgioMi3qImqA2FaFSYrkHd7BYESnSMdqAx1HNgg/6pG0Bo95RAGehqoNAuaRHR90wGdXyJtkAJ1DxSDVQCfS8ocui+EohqagNjFroniyLAOYbBgvSQxuXxiUSCGQXReJBnjafhbf6xBs8P9ZclLLJdTJfdL3bLRsgd50Nf52P7JIWjInYqFuZhUGErucF0Qj/zNJtPGArDz7EYFi0chvSpw8C/mJRgRVLfgrEf7RvowhyjJ3JPfPlX/h8N/6fZryX7bh/pJsPj4QLX9Ra89NL3QQkljmOqnognU6HcxKkoI/JsaJ8cDcfCqZAMC2cfFeSoHu+WFEmWzIQqx8PVmCThSFqPKqLIsgxJx0QYZt1iocjgfrPbjIoiltkXxzxTlE5FVTL1zb7YmTOSzXGiEBU0ZgHzXexjd9HklDtTc2P7iR4/Wmqk/jGhfZXjZW1bYFVp3y01G+ocrh/K9VST3+05OUsaEnAYGKZRfWIpDQaXT2Ej2/vCl1S5nNe7jHq5eCAlM7rOpFx8PP1Zf/NzCUdkpXjUhHmdfdi/Xv31D6WccPAIDjNMmPnBzC+ErAipZzPf++LkQyGRhTDEpCNkbmLpz8892zmE3+8swq1YODIqf2Z7lO8RdJHn7RS8kpY6r0qhAg7xXIHnhViu+zBDbhcx16UOfGVgaGkoXe6LhwS+h7NgSa+vR7ESZvPyq6VUqN+SC0ZSTPm3oETGoxGIh/p60w3naIyJ/Gywf9CMnnAemR3524hT5DErxOwBhR55COMw3e+u0T0tOEsR0JMx+NBHftD/AJ+D/f7v/TW+9t+P+Bo9e/7vNYz+By6FsKkAAAB42mNgZGBgYGRwbI8IWhzPb/OVQZ6DAQTOni3fCKP/+/x7yrOBNRTI5WBgAokCAG3mDbAAeNpjYGRgYFX9t5eBgeftf5//WTwbGIAiKMAdAJycBph42mN6w+DCwcDAAMIsZ8D0HhBNLIap52D478fBwHQRyvbBpZ7nLYMtKeZjt5OJhxT1TKsYGFhDETTjcSAG0gyPoRgozigIpL0hNEiOBcgFAEBoNC142mNgYNCBwjoccALDBEY9RhsgPIMMmZcRhHtIhkcA9pQspAAAAQAAAEcBVAALAAAAAAACAAEAAgAWAAABAACTAAAAAHjalZCxTgJBFEXPApJoYYgF9VZUSIAFTdDCnmiIgsTKsASQuGiCu0YaCr4OfomKOzsTCHRmMzPn3blz38sCFyzJ4uXOgbKWZY+8KssZLqk7zkp9cJyjSOT4jD9WjvPSt46vKHoFx2txyfGGqnfPO18kyohSGjBjJPqRFmqPmWolWkZ9o0uHZ/EkfTNgTo0KVX017ujRps+TyDqvT7xW9U/UV1Vz9ZryrQn8o8QOL1JsdVA/5IwZpv7f/YsKTW50O1PqpzKNZyw1UnKov2c9dbkD7c1/zdhXFSrNdIz3HbuaJFH1KM9CZyDN3N3SoiFupfP66mbOYAd8k0EGAHjabc05TwJhHITxZ0BBBc/P4IkI7y4sh0dBsosHKiqHeLUiiTE0FH56Xdl/6TS/ZIoZUszzM+ad/3IOSilNmm122GWPfQ4ocEiRI0qUcXj4VKgSUKNOgybHnHDKGSER7Xjjgkuu6HDNDbd0ueOeB3r0GTDkkRFPPPPCK29a0KIyympJy1pRTnmtak3r2tCmtjLjz+/ph5edfU2cc2Fiy/3px4Xpmb5ZMatmYNbMutkwm2Yr0W8nBnOj+OcXVDk0PnjaRc67DoJAEAVQFuT9fqsJCSZ2+w12QkNjrCCx9w+sbSy19DsGK/9Ob3RZujk3k7nzZp8bsbvSkXXoR8Yew9gavN9QNHSUHTFch4oMfuoV0uqGNL4nv25emq3yHzzADwVcwOsFHMCtBWzAWQlYgJ0ImIA1rRmAeRbQAWM6vQD04A9GgXglRBo4Kh+19gJGYDgzBqOnZALGO8kUTLaSGZhWkjmYrSULMA8kS7CYi5ZgKTlQxr/W1F5aAAAAAAFRp8cxAAA=",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "ytpregular",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/wprt-addons/assets/../../../../../../../../../../../plugins/wprt-addons/assets/font/ytp-regular.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "revicons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.eot?5510888",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "revicons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.eot?5510888#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "revicons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.woff?5510888",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "revicons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.ttf?5510888",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "revicons",
      "src": "https://nucleorural.com.br/wp-content/cache/background-css/nucleorural.com.br/wp-content/cache/min/1/wp-content/plugins/revslider/sr6/assets/css/../../../../../../../../../../../../../plugins/revslider/sr6/assets/fonts/revicons/revicons.svg?5510888#revicons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Montserrat",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/JTUSjIg1_i6t8kCHKm459WRhyyTh89ZNpQ.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Montserrat",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/JTUSjIg1_i6t8kCHKm459W1hyyTh89ZNpQ.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Montserrat",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/JTUSjIg1_i6t8kCHKm459WZhyyTh89ZNpQ.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Montserrat",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/JTUSjIg1_i6t8kCHKm459WdhyyTh89ZNpQ.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Montserrat",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/JTUSjIg1_i6t8kCHKm459WlhyyTh89Y.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHrv4kjgoGqM7E3b_s0wH8DnzcjTrA.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHrv4kjgoGqM7E3b_s1wH8DnzcjTrA.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHrv4kjgoGqM7E3b_s7wH8Dnzcj.woff2",
      "format": "woff2",
      "weight": "100"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3w-os6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "200"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3w-os6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "200"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3w-os51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "200"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3p-ks6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "300"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3p-ks6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "300"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3p-ks51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "300"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHpv4kjgoGqM7E_A8s5ynghnQci.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHpv4kjgoGqM7E_Ass5ynghnQci.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHpv4kjgoGqM7E_DMs5ynghnQ.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3_-gs6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "500"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3_-gs6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "500"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3_-gs51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "500"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E30-8s6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "600"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E30-8s6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "600"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E30-8s51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "600"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3t-4s6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "700"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3t-4s6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "700"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3t-4s51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "700"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3q-0s6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "800"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3q-0s6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "800"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3q-0s51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "800"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3j-ws6Fostz0rdom9.woff2",
      "format": "woff2",
      "weight": "900"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3j-ws6Vostz0rdom9.woff2",
      "format": "woff2",
      "weight": "900"
    },
    {
      "family": "Barlow",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/7cHqv4kjgoGqM7E3j-ws51ostz0rdg.woff2",
      "format": "woff2",
      "weight": "900"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmZiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmQiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmYiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmXiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVnoiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVn6iAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmbiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmaiAr0klQmz24O0g.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "Roboto",
      "src": "https://nucleorural.com.br/wp-content/cache/perfmatters/nucleorural.com.br/fonts/KFOMCnqEu92Fr1ME7kSn66aGLdTylUAMQXC89YmC2DPNWubEbVmUiAr0klQmz24.woff2",
      "format": "woff2",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/agrikoleicons/AgrikoleIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/agrikoleicons/AgrikoleIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/agrikoleicons/AgrikoleIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/agrikoleicons/AgrikoleIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "AgrikoleIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/agrikoleicons/AgrikoleIcons.svg#AgrikoleIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/pe7s/Pe-icon-7-stroke.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/pe7s/Pe-icon-7-stroke.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/pe7s/Pe-icon-7-stroke.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/pe7s/Pe-icon-7-stroke.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/pe7s/Pe-icon-7-stroke.svg?d7yf1v#Pe-icon-7-stroke",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/eleganticons/ElegantIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/eleganticons/ElegantIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/eleganticons/ElegantIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/eleganticons/ElegantIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons//assets/eleganticons/ElegantIcons.svg#ElegantIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_icons_v3/fonts/vcpb-plugin-icons.eot?onqajd#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_icons_v3/fonts/vcpb-plugin-icons.ttf?onqajd",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_icons_v3/fonts/vcpb-plugin-icons.woff?onqajd",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "vcpb-plugin-icons",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_icons_v3/fonts/vcpb-plugin-icons.svg?onqajd#vcpb-plugin-icons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_grid/vc_grid_v1.eot?-9hbgac",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_grid/vc_grid_v1.eot?#iefix-9hbgac",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_grid/vc_grid_v1.woff?-9hbgac",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_grid/vc_grid_v1.ttf?-9hbgac",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "vc_grid_v1",
      "src": "https://nucleorural.com.br/wp-content/plugins/js_composer/assets/css/../fonts/vc_grid/vc_grid_v1.svg?-9hbgac#vc_grid_v1",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/eleganticons/ElegantIcons.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/eleganticons/ElegantIcons.eot?#iefix",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/eleganticons/ElegantIcons.woff",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/eleganticons/ElegantIcons.ttf",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "ElegantIcons",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/eleganticons/ElegantIcons.svg#ElegantIcons",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/pe7s/Pe-icon-7-stroke.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/pe7s/Pe-icon-7-stroke.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/pe7s/Pe-icon-7-stroke.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/pe7s/Pe-icon-7-stroke.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Pe-icon-7-stroke",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/pe7s/Pe-icon-7-stroke.svg?d7yf1v#Pe-icon-7-stroke",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/coreicon/coreicon.eot?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/coreicon/coreicon.eot?#iefixd7yf1v",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/coreicon/coreicon.woff?d7yf1v",
      "format": "woff",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/coreicon/coreicon.ttf?d7yf1v",
      "format": "truetype",
      "weight": "400"
    },
    {
      "family": "Core Icon",
      "src": "https://nucleorural.com.br/wp-content/themes/agrikole/assets/css/../font/coreicon/coreicon.svg?d7yf1v#coreicon",
      "format": "svg",
      "weight": "400"
    },
    {
      "family": "ytpregular",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons/assets/font/ytp-regular.eot",
      "format": "embedded-opentype",
      "weight": "400"
    },
    {
      "family": "ytpregular",
      "src": "https://nucleorural.com.br/wp-content/plugins/wprt-addons/assets/font/ytp-regular.ttf",
      "format": "truetype",
      "weight": "400"
    }
  ],
  "rules": {
    "maxSizesPerScreen": 4,
    "headingWeightRange": "600-700",
    "bodyWeight": 400,
    "lineHeightBody": 1.5,
    "lineHeightHeading": 1.2
  }
}
```

## Bundled Fonts (fonts/)

The following font files are bundled in the `fonts/` directory:

- `fonts/Barlow-Black.ttf`
- `fonts/Barlow-Bold.ttf`
- `fonts/Barlow-ExtraBold.ttf`
- `fonts/Barlow-ExtraLight.ttf`
- `fonts/Barlow-Light.ttf`
- `fonts/Barlow-Medium.ttf`
- `fonts/Barlow-Regular.ttf`
- `fonts/Barlow-SemiBold.ttf`
- `fonts/Barlow-Thin.ttf`
- `fonts/Montserrat-Black.ttf`
- `fonts/Montserrat-Bold.ttf`
- `fonts/Montserrat-ExtraBold.ttf`
- `fonts/Montserrat-ExtraLight.ttf`
- `fonts/Montserrat-Light.ttf`
- `fonts/Montserrat-Medium.ttf`
- `fonts/Montserrat-Regular.ttf`
- `fonts/Montserrat-SemiBold.ttf`
- `fonts/Montserrat-Thin.ttf`
- `fonts/Roboto-Black.ttf`
- `fonts/Roboto-Bold.ttf`
- `fonts/Roboto-ExtraBold.ttf`
- `fonts/Roboto-ExtraLight.ttf`
- `fonts/Roboto-Light.ttf`
- `fonts/Roboto-Medium.ttf`
- `fonts/Roboto-Regular.ttf`
- `fonts/Roboto-SemiBold.ttf`
- `fonts/Roboto-Thin.ttf`

Use these local font files in `@font-face` declarations instead of fetching from Google Fonts.

## Screenshots Inventory (screens/)

> Study all screenshots carefully before implementing any UI. Match every visual detail exactly.

### Scroll Journey (screens/scroll/)

*Cinematic scroll states — page visual at each scroll depth*

![scroll-000.png](screens/scroll/scroll-000.png)

![scroll-017.png](screens/scroll/scroll-017.png)

![scroll-033.png](screens/scroll/scroll-033.png)

![scroll-050.png](screens/scroll/scroll-050.png)

![scroll-067.png](screens/scroll/scroll-067.png)

![scroll-083.png](screens/scroll/scroll-083.png)

![scroll-100.png](screens/scroll/scroll-100.png)

### Full Page Screenshots (screens/pages/)

*Full-page screenshots of each crawled URL*

![blog.png](screens/pages/blog.png)

![contato.png](screens/pages/contato.png)

![home.png](screens/pages/home.png)

![project-aumento-na-producao-de-carne.png](screens/pages/project-aumento-na-producao-de-carne.png)

![project-eliminacao-de-parasitas-do-gado.png](screens/pages/project-eliminacao-de-parasitas-do-gado.png)

### Section Clips (screens/sections/)

*Clipped individual sections and components*

![contato-section-1.png](screens/sections/contato-section-1.png)

![contato-section-2.png](screens/sections/contato-section-2.png)

![home-section-1.png](screens/sections/home-section-1.png)

![home-section-2.png](screens/sections/home-section-2.png)

![project-aumento-na-producao-de-carne-section-1.png](screens/sections/project-aumento-na-producao-de-carne-section-1.png)

![project-aumento-na-producao-de-carne-section-2.png](screens/sections/project-aumento-na-producao-de-carne-section-2.png)

### Interaction States (screens/states/)

*Hover, focus, and active state captures*

![link-1-default.png](screens/states/link-1-default.png)

![link-1-focus.png](screens/states/link-1-focus.png)

![link-1-hover.png](screens/states/link-1-hover.png)

![link-2-default.png](screens/states/link-2-default.png)

![link-2-focus.png](screens/states/link-2-focus.png)

![link-2-hover.png](screens/states/link-2-hover.png)

![link-3-default.png](screens/states/link-3-default.png)

![link-3-focus.png](screens/states/link-3-focus.png)

![link-3-hover.png](screens/states/link-3-hover.png)

### Screenshot Index (screens/INDEX.md)

# Screenshot Index

## Scroll Journey

> Shows the cinematic state at each point of the page

| Scroll | Y Position | File |
|--------|-----------|------|
| 0% | 0px | `screens/scroll/scroll-000.png` |
| 17% | 891px | `screens/scroll/scroll-017.png` |
| 33% | 1731px | `screens/scroll/scroll-033.png` |
| 50% | 2622px | `screens/scroll/scroll-050.png` |
| 67% | 3447px | `screens/scroll/scroll-067.png` |
| 83% | 3447px | `screens/scroll/scroll-083.png` |
| 100% | 3447px | `screens/scroll/scroll-100.png` |

## Pages

| Page | URL | File |
|------|-----|------|
| Núcleo Rural: suplementos para gado de corte e leite | `https://nucleorural.com.br/` | `screens/pages/home.png` |
| Blog Núcleo Rural: Dicas Práticas para Pecuária de Alta Performance | `https://nucleorural.com.br/blog/` | `screens/pages/blog.png` |
| Contato - Núcleo Rural | `https://nucleorural.com.br/contato/` | `screens/pages/contato.png` |
| Eliminação de Parasitas do Gado com Master S3 - Núcleo Rural | `https://nucleorural.com.br/project/aumento-na-producao-de-carne/` | `screens/pages/project-aumento-na-producao-de-carne.png` |
| Eliminação de Parasitas do Gado | `https://nucleorural.com.br/project/eliminacao-de-parasitas-do-gado/` | `screens/pages/project-eliminacao-de-parasitas-do-gado.png` |

## Sections

| Page | Section | File |
|------|---------|------|
| home | #1 (section) | `screens/sections/home-section-1.png` |
| home | #2 (section) | `screens/sections/home-section-2.png` |
| contato | #1 (section) | `screens/sections/contato-section-1.png` |
| contato | #2 (article) | `screens/sections/contato-section-2.png` |
| project-aumento-na-producao-de-carne | #1 (section) | `screens/sections/project-aumento-na-producao-de-carne-section-1.png` |
| project-aumento-na-producao-de-carne | #2 (section) | `screens/sections/project-aumento-na-producao-de-carne-section-2.png` |

## Homepage Screenshots (screenshots/)

![homepage.png](screenshots/homepage.png)


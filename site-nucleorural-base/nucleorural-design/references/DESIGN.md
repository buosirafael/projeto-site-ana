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

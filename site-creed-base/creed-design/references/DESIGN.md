# creed-design DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 2 · Components: 11
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![creed-design Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a cool tone. Depth is expressed through layered shadows and subtle surface color variation. Typography uses **Copperplate** throughout — a technical, developer-focused choice that maintains consistency. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 14, 16px. The accent color **#3275b4** anchors interactive elements (buttons, links, focus rings). Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| color-black | `#000000` | background | Page background, darkest surface |
| surface | `#333333` | surface | Card and panel backgrounds |
| tw-ring-offset-color | `#ffffff` | text-primary | Headings and body text |
| text-muted | `#666666` | text-muted | Captions, placeholders, secondary info |
| tw-ring-color | `#4a5158` | border | Dividers, card borders, outlines |
| accent | `#3275b4` | accent | CTAs, links, focus rings, active states |
| color-error | `#c22f3d` | danger | Error states, destructive actions |
| color-success | `#2e8442` | success | Success states, positive indicators |
| warning | `#fff4e8` | warning | Warning states, caution indicators |
| info | `#3860be` | info | Informational highlights |
| color-border | `#e5e5e5` | unknown | Palette color |
| unknown | `#17171a` | unknown | Palette color |
| color-neutral | `#f2f2f2` | unknown | Palette color |
| unknown | `#2c3e50` | unknown | Palette color |
| unknown | `#d4d4d4` | unknown | Palette color |
| unknown | `#6b7280` | unknown | Palette color |
| unknown | `#767676` | unknown | Palette color |
| color-info | `#4e72c6` | unknown | Palette color |
| unknown | `#c8c8c8` | unknown | Palette color |
| unknown | `#bbbbbb` | unknown | Palette color |

### CSS Variable Tokens

```css
--tw-border-style: solid;
--color-primary: oklch(43%.0147 248.17);
--color-secondary: oklch(67%.15 250);
--color-primary-500: oklch(from var(--color-primary) l c h);
--color-primary-dark: var(--color-primary-950);
--color-primary-hover: var(--color-primary-600);
--accordion-border: none;
--alert-border-default: none;
--alert-border-radius: var(--radius-site);
--btn-border-width: 0px;
--btn-bordered-border-width: 3px;
--btn-border-width: var(--btn-bordered-border-width);
--input-border-width: 1px;
--input-border-width-active: 2px;
--input-border-width-invalid: 2px;
--input-error-border-color: var(--color-error);
--dropdown-border-width: 1px;
--dropdown-border-width-active: 2px;
--dropdown-error-border-color: var(--color-error);
--breadcrumb-icon-border-top: 1px;
```


---

## 3. Typography Rules

**Font Stack:**
- **Copperplate** — Heading 1, Heading 2, Heading 3
- **SFMono-Regular** — Body, Caption, Code

**Font Sources:**

```css
@font-face {
  font-family: "Copperplate";
  src: url("fonts/Copperplate-300.woff") format("woff");
  font-weight: 300;
}
@font-face {
  font-family: "BigCaslon";
  src: url("fonts/BigCaslon-Regular.woff") format("woff");
  font-weight: 400;
}
@font-face {
  font-family: "BigCaslon";
  src: url("fonts/BigCaslon-700.woff") format("woff");
  font-weight: 700;
}
@font-face {
  font-family: "Pinyon Script";
  src: url("fonts/PinyonScript-Regular.ttf") format("truetype");
  font-weight: 400;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Copperplate | 300px | 700 |
| Heading 2 | Copperplate | 42px | 700 |
| Heading 3 | Copperplate | var(--text-desktop-xl,32px) | 700 |
| Body | SFMono-Regular | 1rem | 400 |
| Caption | SFMono-Regular | 16px | 400 |
| Code | SFMono-Regular | 14px | 400 |

**Typographic Rules:**
- Use **Copperplate** for all text — do not mix font families
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
- Variants: `light`, `status`

**Badge** — `html`

**List** — `html`

### Data Input (2)

**Button** — `html`
- Animation: 

**Input** — `html`
- State: :focus, :placeholder

### Overlay (1)

**Modal** — `html`

### Media (3)

**Image** — `html`

**Icon** — `html`

**Map/Canvas** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 14, 16, 20, 24, 26, 28
- **Border radius:** .25rem, .3125rem, .375rem, .5rem, 1px, 2px, 4px, 5px, 8px, 12px, 17px, 20px, 50px
- **Max content width:** 80rem

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

- `inset 0 0 0 2px var(--color-border-hover)`
- `0 1px 2px #00000080`

### Raised — cards, buttons, interactive elements

- `var(--modal-box-shadow)`
- `var(--modal-mobile-shadow)`
- `inset 0 0 0 var(--input-border-width) var(--color-border)`

### Floating — dropdowns, popovers, modals

- `0-6px 12px -4px #0000001a`
- `0 2px 10px #0000001a`

### Z-Index Scale

`0, 1, 2, 3, 4, 5, 10, 20, 30, 40, 41, 50, 55, 60, 100, 101, 999, 1000, 9000, 9999, 50000, 99999, 999999`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes skeleton-loading`
- `@keyframes chatbot-sparkle`
- `@keyframes spin`
- `@keyframes pulse`
- `@keyframes slide-up`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#3275b4` for interactive elements (buttons, links, focus rings)
- Use `#000000` as the primary page background
- Use **Copperplate** for all UI text
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: .25rem, .3125rem, .375rem, .5rem, 1px
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't mix font families — use Copperplate consistently
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
| sm | 40rem | css |
| md | 48rem | css |
| lg | 64rem | css |
| xl | 80rem | css |
| 2xl | 96rem | css |
| sm | 599px | css |
| sm | 600px | css |
| sm | 639px | css |
| sm | 640px | css |
| md | 767px | css |
| md | 768px | css |
| lg | 1023px | css |
| lg | 1024px | css |
| xl | 1200px | css |
| xl | 1280px | css |
| 2xl | 1440px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #333333
Border: 1px solid #4a5158
Radius: 4px
Padding: 16px
Font: Copperplate
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg #3275b4, text white
Ghost: bg transparent, border #4a5158
Padding: 8px 16px
Radius: 4px
Hover: opacity 0.9 or lighter shade
Focus: ring with #3275b4
```

### Build a Page Layout

```
Background: #000000
Max-width: 80rem, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #333333
Label: #666666 (muted, 12px, uppercase)
Value: #ffffff (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #000000
Input border: 1px solid #4a5158
Focus: border-color #3275b4
Label: #666666 12px
Spacing: 16px between fields
Radius: 4px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Copperplate, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```

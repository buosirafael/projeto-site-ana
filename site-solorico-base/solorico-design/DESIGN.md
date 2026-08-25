# solorico-design DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 1 · Components: 10
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![solorico-design Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a neutral tone. Depth is expressed through layered shadows and subtle surface color variation. Typography uses **sans-serif** throughout — a clean, modern choice that maintains consistency. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 14, 16px. Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| bs-body-color | `#1e1e1e` | background | Page background, darkest surface |
| text-dark | `#333333` | surface | Card and panel backgrounds |
| text-light | `#f9f9f9` | text-primary | Headings and body text |
| bs-btn-active-border-color | `#bfbfbf` | text-muted | Captions, placeholders, secondary info |
| bs-dark-text | `#555555` | border | Dividers, card borders, outlines |
| bs-danger | `#dc3545` | danger | Error states, destructive actions |
| success | `#28a745` | success | Success states, positive indicators |
| bs-warning | `#ffc107` | warning | Warning states, caution indicators |
| bs-primary | `#0d6efd` | info | Informational highlights |
| bs-emphasis-color | `#000000` | unknown | Palette color |
| bs-table-border-color | `#cccccc` | unknown | Palette color |
| primary-green | `#3b7d1c` | unknown | Palette color |
| bs-secondary | `#777777` | unknown | Palette color |
| unknown | `#666666` | unknown | Palette color |
| bs-success | `#198754` | unknown | Palette color |
| bs-border-color | `#e2e2e2` | unknown | Palette color |
| bs-info | `#0dcaf0` | unknown | Palette color |
| unknown | `#f4a51c` | unknown | Palette color |
| primary-yellow | `#f7d51c` | unknown | Palette color |
| secondary-green | `#6bbf34` | unknown | Palette color |

### CSS Variable Tokens

```css
--primary-green: #3b7d1c;
--secondary-green: #6bbf34;
--primary-yellow: #f7d51c;
--bs-primary: #0d6efd;
--bs-secondary: #6c757d;
--bs-primary-rgb: 13,110,253;
--bs-secondary-rgb: 108,117,125;
--bs-primary-text: #0a58ca;
--bs-secondary-text: #6c757d;
--bs-primary-bg-subtle: #cfe2ff;
--bs-secondary-bg-subtle: #f8f9fa;
--bs-primary-border-subtle: #9ec5fe;
--bs-secondary-border-subtle: #e9ecef;
--bs-success-border-subtle: #a3cfbb;
--bs-info-border-subtle: #9eeaf9;
--bs-warning-border-subtle: #ffe69c;
--bs-danger-border-subtle: #f1aeb5;
--bs-light-border-subtle: #e9ecef;
--bs-dark-border-subtle: #adb5bd;
--bs-secondary-color: rgba(33,37,41,0.75);
```


---

## 3. Typography Rules

**Font Stack:**
- **sans-serif** — Heading 1, Heading 2, Heading 3, Body, Caption

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | sans-serif | 5rem | 700 |
| Heading 2 | sans-serif | 4.5rem | 700 |
| Heading 3 | sans-serif | 4rem | 700 |
| Body | sans-serif | 1rem | 400 |
| Caption | sans-serif | 1.25rem | 400 |

**Typographic Rules:**
- Use **sans-serif** for all text — do not mix font families
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
- Variants: `custom`, `img`, `body`, `icon`, `title`

**Badge** — `html`

**List** — `html`

### Data Input (2)

**Button** — `html`
- Variants: `success`, `sm`, `close`, `close-white`
- Animation: 

**Input** — `html`
- State: :focus, :placeholder

### Overlay (1)

**Modal** — `html`

### Media (2)

**Image** — `html`

**Map/Canvas** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 14, 16, 20, 24, 26, 28
- **Border radius:** .1em, .25rem, .25em, .375rem, .5rem, 1rem, 2em, 2px, 4px, 5px, 6px, 8px, 10px, 12px, 15px, 15px 15px 10px 10px, 20px, 24px, inherit
- **Max content width:** 991.98px

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

- `inset 0-1px 0 rgba(0,0,0,0.15)`
- `0 0 0 1px #fff,0 0 0 .25rem rgba(13,110,253,.25)`

### Raised — cards, buttons, interactive elements

- `0 4px 6px rgba(0,0,0,0.1)`
- `0 4px 8px rgba(0,0,0,0.1)`
- `0 0 0 0.2rem rgba(40,167,69,0.25)`

### Floating — dropdowns, popovers, modals

- `0px 4px 10px rgba(0,0,0,0.2)`
- `0px 6px 15px rgba(0,0,0,0.3)`
- `0 5px 15px rgba(0,0,0,0.1)`

### Overlay — full-screen overlays, top-level dialogs

- `0 8px 25px rgba(0,0,0,0.1)`
- `0 20px 45px rgba(0,0,0,0.35)`
- `inset 0 0 0 9999px var(--bs-table-accent-bg)`

### Z-Index Scale

`0, 1, 2, 3, 4, 5, 10, 20, 1000, 1020, 1030, 1040, 1050, 9999`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes fa-beat`
- `@keyframes fa-bounce`
- `@keyframes fa-fade`
- `@keyframes fa-beat-fade`
- `@keyframes fa-flip`
- `@keyframes fa-shake`
- `@keyframes fa-spin`
- `@keyframes progress-bar-stripes`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#1e1e1e` as the primary page background
- Use **sans-serif** for all UI text
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: .1em, .25rem, .25em, .375rem, .5rem
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't mix font families — use sans-serif consistently
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
| sm | 575.98px | css |
| sm | 576px | css |
| md | 767px | css |
| md | 767.98px | css |
| md | 768px | css |
| lg | 991px | css |
| lg | 991.98px | css |
| lg | 992px | css |
| xl | 1199.98px | css |
| xl | 1200px | css |
| 2xl | 1399.98px | css |
| 2xl | 1400px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #333333
Border: 1px solid #555555
Radius: 5px
Padding: 16px
Font: sans-serif
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg var(--accent), text white
Ghost: bg transparent, border #555555
Padding: 8px 16px
Radius: 5px
Hover: opacity 0.9 or lighter shade
Focus: ring with var(--accent)
```

### Build a Page Layout

```
Background: #1e1e1e
Max-width: 991.98px, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #333333
Label: #bfbfbf (muted, 12px, uppercase)
Value: #f9f9f9 (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #1e1e1e
Input border: 1px solid #555555
Focus: border-color var(--accent)
Label: #bfbfbf 12px
Spacing: 16px between fields
Radius: 5px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: sans-serif, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```

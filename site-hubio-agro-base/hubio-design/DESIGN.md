# hubio-design DESIGN.md

> Auto-generated design system — reverse-engineered via static analysis by skillui.
> Frameworks: None detected
> Colors: 20 · Fonts: 1 · Components: 10
> Icon library: not detected · State: not detected
> Primary theme: dark · Dark mode toggle: no · Motion: expressive

## Visual Reference

**Match this design exactly** — study colors, fonts, spacing, and component shapes before writing any UI code.

![hubio-design Homepage](../screenshots/homepage.png)

---

## 1. Visual Theme & Atmosphere

This is a **dark-themed** interface with a neutral tone. Depth is expressed through layered shadows and subtle surface color variation. Typography uses **Poppins** throughout — a clean, modern choice that maintains consistency. Spacing follows a **4px base grid** (compact density), with scale: 2, 4, 6, 8, 10, 12, 14, 16px. Motion is expressive — spring physics, layout animations, and staggered reveals are part of the visual language.

---

## 2. Color Palette & Roles

| Token | Hex | Role | Use |
|---|---|---|---|
| background | `#1f221c` | background | Page background, darkest surface |
| surface | `#164133` | surface | Card and panel backgrounds |
| text-primary | `#ffffff` | text-primary | Headings and body text |
| text-muted | `#565b50` | text-muted | Captions, placeholders, secondary info |
| border | `#2a3a30` | border | Dividers, card borders, outlines |
| danger | `#b76318` | danger | Error states, destructive actions |
| success | `#1ebb01` | success | Success states, positive indicators |
| info | `#1f5a8a` | info | Informational highlights |
| unknown | `#83c802` | unknown | Palette color |
| unknown | `#f1f5ee` | unknown | Palette color |
| unknown | `#dde1d8` | unknown | Palette color |
| unknown | `#0d2a20` | unknown | Palette color |
| unknown | `#081f14` | unknown | Palette color |
| unknown | `#000000` | unknown | Palette color |
| unknown | `#7a8073` | unknown | Palette color |
| unknown | `#9aa091` | unknown | Palette color |
| unknown | `#1ed760` | unknown | Palette color |
| unknown | `#98e003` | unknown | Palette color |
| unknown | `#e7eedf` | unknown | Palette color |
| unknown | `#9fe26a` | unknown | Palette color |


---

## 3. Typography Rules

**Font Stack:**
- **Poppins** — Heading 1, Heading 2, Heading 3, Body, Caption

**Font Sources:**

```css
@font-face {
  font-family: "Poppins";
  src: url("https://fonts.gstatic.com/s/poppins/v24/pxiGyp8kv8JHgFVrJJLedw.ttf") format("truetype");
  font-weight: 400;
}
@font-face {
  font-family: "Poppins";
  src: url("https://fonts.gstatic.com/s/poppins/v24/pxiByp8kv8JHgFVrLCz7V1s.ttf") format("truetype");
  font-weight: 700;
}
```

| Role | Font | Size | Weight |
|---|---|---|---|
| Heading 1 | Poppins | 14rem | 700 |
| Heading 2 | Poppins | 9rem | 700 |
| Heading 3 | Poppins | clamp(3rem,6vw,4.6rem) | 700 |
| Body | Poppins | .68rem | 400 |
| Caption | Poppins | .8rem | 400 |

**Typographic Rules:**
- Use **Poppins** for all text — do not mix font families
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
- Variants: `top`, `big`, `figure`, `bottom`, `feats`

**Badge** — `html`

**List** — `html`

### Data Input (2)

**Button** — `html`
- Variants: `primary`, `prev`
- Animation: 

**Input** — `html`
- State: :focus, :placeholder

### Media (3)

**Image** — `html`

**Icon** — `html`

**Map/Canvas** — `html`



---

## 5. Layout Principles

- **Base spacing unit:** 4px
- **Spacing scale:** 2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24
- **Border radius:** 1px, 2px, 3px, 4px, 6px, 8px, 10px, 11px, 12px, 13px, 14px, 16px, 18px, 22px, 24px, 24px 24px 0px 0px, 28px, 30px, 32px, 100px, 100px 0px 0px 100px
- **Max content width:** 980px

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

- `0 0 0 2px rgba(30,187,1,.3)`
- `rgba(131, 200, 2, 0.506) 0px 0px 0px 1.08104px`
- `rgba(131, 200, 2, 0.55) 0px 0px 0px 0px`

### Raised — cards, buttons, interactive elements

- `0 0 0 0 rgba(30,187,1,.7)`
- `0 0 8px var(--lm)`
- `0 0 0 0 rgba(131,200,2,.55)`

### Floating — dropdowns, popovers, modals

- `0 0 16px var(--lm)`
- `0 0 14px var(--vr)`
- `0 6px 16px rgba(131,200,2,.32)`

### Overlay — full-screen overlays, top-level dialogs

- `0 10px 30px rgba(131,200,2,.32)`
- `0 14px 36px rgba(131,200,2,.32)`
- `0 6px 22px rgba(30,187,1,.32),inset 0 1px 0 rgba(255,255,255,.18)`

### Z-Index Scale

`0, 1, 2, 3, 20, 100`



---

## 7. Animation & Motion

This project uses **expressive motion**. Animations are an integral part of the experience.

### CSS Animations

- `@keyframes flOrbit`
- `@keyframes flOrbitRev`
- `@keyframes hbmaxBadge`
- `@keyframes ctaPulse`
- `@keyframes fadeUp`
- `@keyframes pulse`
- `@keyframes sbounce`
- `@keyframes rotate`

### Animated Components

- **Button**: 

### Motion Guidelines

- Duration: 150-300ms for micro-interactions, 300-500ms for page transitions
- Easing: `ease-out` for enters, `ease-in` for exits
- Always respect `prefers-reduced-motion`


---

## 8. Do's and Don'ts

### Do's

- Use `#1f221c` as the primary page background
- Use **Poppins** for all UI text
- Follow the **4px** spacing grid for all margins, padding, and gaps
- Use the defined shadow tokens for elevation — see Section 6
- Use border-radius from the scale: 1px, 2px, 3px, 4px, 6px
- Reuse existing components from Section 4 before creating new ones

### Don'ts

- Don't introduce colors outside this palette — extend the design tokens first
- Don't mix font families — use Poppins consistently
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
| xs | 400px | css |
| sm | 560px | css |
| sm | 600px | css |
| sm | 640px | css |
| md | 760px | css |
| lg | 900px | css |
| lg | 980px | css |
| xl | 1100px | css |

**Approach:** Use `@media (min-width: ...)` queries matching the breakpoints above.


---

## 10. Agent Prompt Guide

Use these as starting points when building new UI:

### Build a Card

```
Background: #164133
Border: 1px solid #2a3a30
Radius: 14px
Padding: 16px
Font: Poppins
Use shadow tokens from Section 6.
```

### Build a Button

```
Primary: bg var(--accent), text white
Ghost: bg transparent, border #2a3a30
Padding: 8px 16px
Radius: 14px
Hover: opacity 0.9 or lighter shade
Focus: ring with var(--accent)
```

### Build a Page Layout

```
Background: #1f221c
Max-width: 980px, centered
Grid: 4px base
Responsive: mobile-first, breakpoints from Section 9
```

### Build a Stats Card

```
Surface: #164133
Label: #565b50 (muted, 12px, uppercase)
Value: #ffffff (primary, 24-32px, bold)
Status: use success/warning/danger from Section 2
```

### Build a Form

```
Input bg: #1f221c
Input border: 1px solid #2a3a30
Focus: border-color var(--accent)
Label: #565b50 12px
Spacing: 16px between fields
Radius: 14px
```

### General Component

```
1. Read DESIGN.md Sections 2-6 for tokens
2. Colors: only from palette
3. Font: Poppins, type scale from Section 3
4. Spacing: 4px grid
5. Components: match patterns from Section 4
6. Elevation: shadow tokens
```

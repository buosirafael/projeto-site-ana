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

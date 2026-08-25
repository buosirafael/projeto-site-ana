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


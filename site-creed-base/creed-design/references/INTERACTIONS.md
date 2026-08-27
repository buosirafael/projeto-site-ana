# Interaction Reference

> Micro-interactions extracted from live DOM. Recreate these exactly for authentic feel.

## Coverage

| Component Type | Count | States Captured |
|----------------|-------|----------------|
| Button | 3 | default, hover, focus |
| Link | 3 | default, hover, focus |
| Input | 2 | default, hover, focus |

## Transition System

These transition declarations were extracted from interactive elements:

```css
transition: all;
```

Apply these to all interactive elements. Never invent new durations or easings.

## Button Interactions

### Button 1 — `Submit search`

**States:**

- Default: `../screens/states/button-1-default.png`
- Hover: `../screens/states/button-1-hover.png`
- Focus: `../screens/states/button-1-focus.png`

**On focus:**

```css
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Button 2 — `Account`

**States:**

- Default: `../screens/states/button-2-default.png`
- Hover: `../screens/states/button-2-hover.png`
- Focus: `../screens/states/button-2-focus.png`

**On focus:**

```css
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Button 3 — `Enter Account Menu`

**States:**

- Default: `../screens/states/button-3-default.png`
- Hover: `../screens/states/button-3-hover.png`
- Focus: `../screens/states/button-3-focus.png`

**On focus:**

```css
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

## Link Interactions

### Link 1 — `Country Locator`

**States:**

- Default: `../screens/states/link-1-default.png`
- Hover: `../screens/states/link-1-hover.png`
- Focus: `../screens/states/link-1-focus.png`

**On focus:**

```css
/* color: oklch(0 0 0) → */ color: oklch(0.364544 0 0);
/* border-color: oklch(0 0 0) → */ border-color: oklch(0.364544 0 0);
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
/* text-decoration: none → */ text-decoration: underline;
```

**Transition:** `all`

### Link 2 — `Country Locator`

**States:**

- Default: `../screens/states/link-2-default.png`
- Hover: `../screens/states/link-2-hover.png`
- Focus: `../screens/states/link-2-focus.png`

**On focus:**

```css
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Link 3 — `Store Locator`

**States:**

- Default: `../screens/states/link-3-default.png`
- Hover: `../screens/states/link-3-hover.png`
- Focus: `../screens/states/link-3-focus.png`

**On focus:**

```css
/* background-color: oklch(0.985744 0 0) → */ background-color: oklch(0.991446 0 0);
/* color: oklch(0 0 0) → */ color: oklch(0.5696 0 0);
/* border-color: oklch(0.985744 0 0) → */ border-color: oklch(0.934 0 0);
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

## Input Interactions

### Input 1 — `email`

**States:**

- Default: `../screens/states/input-1-default.png`
- Hover: `../screens/states/input-1-hover.png`
- Focus: `../screens/states/input-1-focus.png`

**On focus:**

```css
/* box-shadow: none → */ box-shadow: rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgba(0, 0, 0, 0) 0px 0px 0px 0px, rgb(255, 255, 255) 0px 0px 0px 2px, oklch(0 0 0) 0px 0px 0px 4px, rgba(0, 0, 0, 0) 0px 0px 0px 0px;
/* outline: oklch(0.364544 0 0) none 3px → */ outline: rgb(16, 16, 16) none 1px;
/* outline-color: oklch(0.364544 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Input 2 — `Search for products`

**States:**

- Default: `../screens/states/input-2-default.png`
- Hover: `../screens/states/input-2-hover.png`
- Focus: `../screens/states/input-2-focus.png`

**On focus:**

```css
/* outline: oklch(0 0 0) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: oklch(0 0 0) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

## Interaction Rules

- Accent color `#3275b4` is used for focus rings, active states, and hover highlights
- Focus states use **outline** (not box-shadow) — always match the extracted focus ring
- Always respect `prefers-reduced-motion` — set all transitions to `0s` when enabled


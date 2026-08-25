# Interaction Reference

> Micro-interactions extracted from live DOM. Recreate these exactly for authentic feel.

## Coverage

| Component Type | Count | States Captured |
|----------------|-------|----------------|
| Button | 2 | default, hover, focus |
| Role Button | 3 | default, hover, focus |
| Link | 3 | default, hover, focus |

## Transition System

These transition declarations were extracted from interactive elements:

```css
transition: opacity 0.15s;
transition: 0.2s ease-in-out;
transition: all;
```

Apply these to all interactive elements. Never invent new durations or easings.

## Button Interactions

### Button 1 — `Anterior`

**States:**

- Default: `../screens/states/button-1-default.png`
- Hover: `../screens/states/button-1-hover.png`
- Focus: `../screens/states/button-1-focus.png`

**On hover:**

```css
/* opacity: 0.5 → */ opacity: 0.9;
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(255, 255, 255) none 0px;
```

**On focus:**

```css
/* opacity: 0.5 → */ opacity: 0.9;
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(255, 255, 255) none 0px;
```

**Transition:** `opacity 0.15s`

### Button 2 — `Próximo`

**States:**

- Default: `../screens/states/button-2-default.png`
- Hover: `../screens/states/button-2-hover.png`
- Focus: `../screens/states/button-2-focus.png`

**On hover:**

```css
/* opacity: 0.5 → */ opacity: 0.9;
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(255, 255, 255) none 0px;
```

**On focus:**

```css
/* opacity: 0.5 → */ opacity: 0.9;
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(255, 255, 255) none 0px;
```

**Transition:** `opacity 0.15s`

## Role Button Interactions

### Role Button 1 — `ATENDIMENTO`

**States:**

- Default: `../screens/states/role-button-1-default.png`
- Hover: `../screens/states/role-button-1-hover.png`
- Focus: `../screens/states/role-button-1-focus.png`

**On focus:**

```css
/* color: rgb(255, 255, 255) → */ color: rgba(255, 255, 255, 0.75);
/* border-color: rgb(255, 255, 255) → */ border-color: rgba(255, 255, 255, 0.75);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `0.2s ease-in-out`

### Role Button 2 — `a`

**States:**

- Default: `../screens/states/role-button-2-default.png`
- Hover: `../screens/states/role-button-2-hover.png`
- Focus: `../screens/states/role-button-2-focus.png`

**On focus:**

```css
/* color: rgb(255, 255, 255) → */ color: rgba(255, 255, 255, 0.75);
/* border-color: rgb(255, 255, 255) → */ border-color: rgba(255, 255, 255, 0.75);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `0.2s ease-in-out`

### Role Button 3 — `Buscar`

**States:**

- Default: `../screens/states/role-button-3-default.png`
- Hover: `../screens/states/role-button-3-hover.png`
- Focus: `../screens/states/role-button-3-focus.png`

**On hover:**

```css
/* color: rgb(255, 255, 255) → */ color: rgb(247, 213, 28);
/* border-color: rgb(255, 255, 255) → */ border-color: rgb(247, 213, 28);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(247, 213, 28) none 3px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(247, 213, 28);
```

**On focus:**

```css
/* color: rgb(255, 255, 255) → */ color: rgba(255, 255, 255, 0.75);
/* border-color: rgb(255, 255, 255) → */ border-color: rgba(255, 255, 255, 0.75);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `0.2s ease-in-out`

## Link Interactions

### Link 1 — `a`

**States:**

- Default: `../screens/states/link-1-default.png`
- Hover: `../screens/states/link-1-hover.png`
- Focus: `../screens/states/link-1-focus.png`

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Link 2 — `HOME`

**States:**

- Default: `../screens/states/link-2-default.png`
- Hover: `../screens/states/link-2-hover.png`
- Focus: `../screens/states/link-2-focus.png`

**On hover:**

```css
/* color: rgb(255, 255, 255) → */ color: rgb(247, 213, 28);
/* border-color: rgb(255, 255, 255) → */ border-color: rgb(247, 213, 28);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(247, 213, 28) none 3px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(247, 213, 28);
```

**On focus:**

```css
/* color: rgb(255, 255, 255) → */ color: rgba(255, 255, 255, 0.75);
/* border-color: rgb(255, 255, 255) → */ border-color: rgba(255, 255, 255, 0.75);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `0.2s ease-in-out`

### Link 3 — `A EMPRESA`

**States:**

- Default: `../screens/states/link-3-default.png`
- Hover: `../screens/states/link-3-hover.png`
- Focus: `../screens/states/link-3-focus.png`

**On hover:**

```css
/* color: rgb(255, 255, 255) → */ color: rgb(247, 213, 28);
/* border-color: rgb(255, 255, 255) → */ border-color: rgb(247, 213, 28);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(247, 213, 28) none 3px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(247, 213, 28);
```

**On focus:**

```css
/* color: rgb(255, 255, 255) → */ color: rgba(255, 255, 255, 0.75);
/* border-color: rgb(255, 255, 255) → */ border-color: rgba(255, 255, 255, 0.75);
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `0.2s ease-in-out`

## Interaction Rules

- Hover effects use **opacity** changes, not color shifts
- Hover effects include **color transitions** — use the extracted values, not approximations
- Focus states use **outline** (not box-shadow) — always match the extracted focus ring
- Transition durations in use: `0.15s`, `0.2s`
- Always respect `prefers-reduced-motion` — set all transitions to `0s` when enabled


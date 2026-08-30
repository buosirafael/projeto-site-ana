# Interaction Reference

> Micro-interactions extracted from live DOM. Recreate these exactly for authentic feel.

## Coverage

| Component Type | Count | States Captured |
|----------------|-------|----------------|
| Button | 3 | default, hover, focus |
| Link | 3 | default, hover, focus |
| Input | 3 | default, hover, focus |

## Transition System

These transition declarations were extracted from interactive elements:

```css
transition: color 0.4s;
transition: background 0.25s;
transition: all;
transition: color 0.3s;
transition: border-color 0.2s, box-shadow 0.2s, background 0.2s;
```

Apply these to all interactive elements. Never invent new durations or easings.

## Button Interactions

### Button 1 — `On Farm`

**States:**

- Default: `../screens/states/button-1-default.png`
- Hover: `../screens/states/button-1-hover.png`
- Focus: `../screens/states/button-1-focus.png`

**On focus:**

```css
/* outline: rgb(12, 36, 24) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(12, 36, 24) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `color 0.4s`

### Button 2 — `Comerciais`

**States:**

- Default: `../screens/states/button-2-default.png`
- Hover: `../screens/states/button-2-hover.png`
- Focus: `../screens/states/button-2-focus.png`

**On focus:**

```css
/* outline: rgba(255, 255, 255, 0.55) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgba(255, 255, 255, 0.55) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `color 0.4s`

### Button 3 — `Fechar`

**States:**

- Default: `../screens/states/button-3-default.png`
- Hover: `../screens/states/button-3-hover.png`
- Focus: `../screens/states/button-3-focus.png`

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `background 0.25s`

## Link Interactions

### Link 1 — `Hubio Agro — página inicial`

**States:**

- Default: `../screens/states/link-1-default.png`
- Hover: `../screens/states/link-1-hover.png`
- Focus: `../screens/states/link-1-focus.png`

**On focus:**

```css
/* outline: rgb(31, 34, 28) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(31, 34, 28) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `all`

### Link 2 — `Início`

**States:**

- Default: `../screens/states/link-2-default.png`
- Hover: `../screens/states/link-2-hover.png`
- Focus: `../screens/states/link-2-focus.png`

**On focus:**

```css
/* outline: rgb(255, 255, 255) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgb(255, 255, 255) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `color 0.3s`

### Link 3 — `On Farm`

**States:**

- Default: `../screens/states/link-3-default.png`
- Hover: `../screens/states/link-3-hover.png`
- Focus: `../screens/states/link-3-focus.png`

**On hover:**

```css
/* color: rgba(255, 255, 255, 0.62) → */ color: rgb(255, 255, 255);
/* border-color: rgba(255, 255, 255, 0.62) → */ border-color: rgb(255, 255, 255);
/* outline: rgba(255, 255, 255, 0.62) none 3px → */ outline: rgb(255, 255, 255) none 3px;
/* outline-color: rgba(255, 255, 255, 0.62) → */ outline-color: rgb(255, 255, 255);
```

**On focus:**

```css
/* outline: rgba(255, 255, 255, 0.62) none 3px → */ outline: rgb(16, 16, 16) auto 1px;
/* outline-color: rgba(255, 255, 255, 0.62) → */ outline-color: rgb(16, 16, 16);
```

**Transition:** `color 0.3s`

## Input Interactions

### Input 1 — `Seu nome completo`

**States:**

- Default: `../screens/states/input-1-default.png`
- Hover: `../screens/states/input-1-hover.png`
- Focus: `../screens/states/input-1-focus.png`

**On focus:**

```css
/* background-color: rgb(248, 250, 247) → */ background-color: rgb(255, 255, 255);
/* border-color: rgb(221, 225, 216) → */ border-color: rgb(30, 187, 1);
/* box-shadow: none → */ box-shadow: rgba(30, 187, 1, 0.12) 0px 0px 0px 3px;
```

**Transition:** `border-color 0.2s, box-shadow 0.2s, background 0.2s`

### Input 2 — `(00) 00000-0000`

**States:**

- Default: `../screens/states/input-2-default.png`
- Hover: `../screens/states/input-2-hover.png`
- Focus: `../screens/states/input-2-focus.png`

**On focus:**

```css
/* background-color: rgb(248, 250, 247) → */ background-color: rgb(254, 254, 253);
/* border-color: rgb(221, 225, 216) → */ border-color: rgb(68, 195, 44);
/* box-shadow: none → */ box-shadow: rgba(30, 187, 1, 0.098) 0px 0px 0px 2.40585px;
```

**Transition:** `border-color 0.2s, box-shadow 0.2s, background 0.2s`

### Input 3 — `seunome@email.com`

**States:**

- Default: `../screens/states/input-3-default.png`
- Hover: `../screens/states/input-3-hover.png`
- Focus: `../screens/states/input-3-focus.png`

**On focus:**

```css
/* background-color: rgb(248, 250, 247) → */ background-color: rgb(255, 255, 255);
/* border-color: rgb(221, 225, 216) → */ border-color: rgb(30, 187, 1);
/* box-shadow: none → */ box-shadow: rgba(30, 187, 1, 0.12) 0px 0px 0px 3px;
```

**Transition:** `border-color 0.2s, box-shadow 0.2s, background 0.2s`

## Interaction Rules

- Hover effects include **color transitions** — use the extracted values, not approximations
- Focus states use **outline** (not box-shadow) — always match the extracted focus ring
- Transition durations in use: `0.4s`, `0.25s`, `0.3s`, `0.2s`
- Always respect `prefers-reduced-motion` — set all transitions to `0s` when enabled


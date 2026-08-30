# Animation Reference

> Cinematic motion design extracted from live DOM. Follow these specs exactly to recreate the experience.

## Motion Technology Stack

| Library | Type | Notes |
|---------|------|-------|
| **Web Animations API (10 active)** | animation |  |
| Canvas (1 elements) | 2D Canvas | 2D canvas rendering |

## Scroll Journey

The page is **5.677px** tall. Each frame below shows what the user sees at that scroll depth.

> **Use these screenshots to understand WHAT animates, WHEN it animates, and HOW it moves.**

### 0% — Top / Hero
Scroll position: 0px

![Scroll 0%](../screens/scroll/scroll-000.png)

### 17% — Opening Section
Scroll position: 812px

![Scroll 17%](../screens/scroll/scroll-017.png)

### 33% — First Feature Section
Scroll position: 1.576px

![Scroll 33%](../screens/scroll/scroll-033.png)

### 50% — Mid-Page
Scroll position: 2.389px

![Scroll 50%](../screens/scroll/scroll-050.png)

### 67% — Lower Content
Scroll position: 3.201px

![Scroll 67%](../screens/scroll/scroll-067.png)

### 83% — Near Footer
Scroll position: 3.965px

![Scroll 83%](../screens/scroll/scroll-083.png)

### 100% — Bottom / Footer
Scroll position: 4.777px

![Scroll 100%](../screens/scroll/scroll-100.png)

## CSS Keyframes (13 extracted)

### `@keyframes hbmaxBadge`

Duration: `2.4s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.of-card.hbmax-highlight::before`

```css
@keyframes hbmaxBadge {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.06);
  }
}
```

> Transform/motion animation

### `@keyframes ctaPulse`

Duration: `2.4s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.hero-actions .btn-primary`

```css
@keyframes ctaPulse {
  0%, 100% {
    box-shadow: rgba(131, 200, 2, 0.55) 0px 0px 0px 0px;
  }
  50% {
    box-shadow: rgba(131, 200, 2, 0) 0px 0px 0px 14px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes pulse`

Duration: `2s` · Easing: `ease` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.hero-eyebrow .pulse`

```css
@keyframes pulse {
  0%, 100% {
    box-shadow: rgba(30, 187, 1, 0.5) 0px 0px 0px 0px;
  }
  50% {
    box-shadow: rgba(30, 187, 1, 0) 0px 0px 0px 8px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes sbounce`

Duration: `2s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.scroll-mouse::after`

```css
@keyframes sbounce {
  0%, 100% {
    transform: translateX(-50%) translateY(0px);
    opacity: 1;
  }
  50% {
    transform: translateX(-50%) translateY(8px);
    opacity: 0.3;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate`

Duration: `60s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.hero-visual .ring`

```css
@keyframes rotate {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes gentle`

Duration: `8s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.hero-visual::before`

```css
@keyframes gentle {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.04);
  }
}
```

> Transform/motion animation

### `@keyframes typing`

Duration: `1.4s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.rb-typing span`

```css
@keyframes typing {
  0%, 60%, 100% {
    transform: translateY(0px);
    opacity: 0.5;
  }
  30% {
    transform: translateY(-6px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes lfIn`

Duration: `0.35s` · Easing: `ease` · Delay: `0s` · Iteration: `1` · Fill: `none`

Used by: `.lf-cond`

```css
@keyframes lfIn {
  0% {
    opacity: 0;
    transform: translateY(-6px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes lfSpin`

Duration: `0.7s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.lf-spin`

```css
@keyframes lfSpin {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes lfFabPulse`

Duration: `2.4s` · Easing: `ease-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.lf-fab-avatar::before`

```css
@keyframes lfFabPulse {
  0% {
    opacity: 0.7;
    transform: scale(1);
  }
  100% {
    opacity: 0;
    transform: scale(1.45);
  }
}
```

> Fade + motion enter animation

### `@keyframes flOrbit`

```css
@keyframes flOrbit {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes flOrbitRev`

```css
@keyframes flOrbitRev {
  0% {
    transform: translate(-50%, -50%) translateY(calc(-1 * var(--r))) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -50%) translateY(calc(-1 * var(--r))) rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes fadeUp`

```css
@keyframes fadeUp {
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

## Global Transition Declarations

These `transition` values were extracted from CSS rules across the site:

```css
transition: padding .4s var(--t1), background .4s var(--t1), backdrop-filter .4s;
transition: transform .3s var(--t1);
transition: color 0.3s;
transition: transform .3s var(--t1), box-shadow .3s, background .3s;
transition: transform 0.3s, opacity 0.3s;
transition: transform .3s var(--t1), box-shadow .3s, background .3s, color .3s, border-color .3s;
transition: gap .3s var(--t1);
transition: opacity .8s var(--t1), transform .8s var(--t1);
transition: 0.3s;
transition: all 1.5s var(--t1);
transition: color 0.4s;
transition: opacity .7s var(--t1), transform .7s var(--t1);
```

## How to Recreate This Motion Design

### Step 1 — Install Dependencies

```bash
```

### Step 2 — Scroll-Reveal Pattern

Elements that animate into view follow this pattern:

```css
/* Initial hidden state */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 4s cubic-bezier(0.4, 0, 0.2, 1),
              transform 4s cubic-bezier(0.4, 0, 0.2, 1);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### Step 3 — Key Motion Principles

- **Canvas elements (1)** — animated via requestAnimationFrame loop. Use canvas for particle effects, gradient animations, and WebGL scenes
- **Duration scale:** `4s` · `3s` · `0.3s` — use these values, never invent new durations
- **Always add** `@media (prefers-reduced-motion: reduce) { * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }`

### Step 4 — Scroll Journey Reference

Match what happens at each scroll position:

- **0%** (`0px`) → `screens/scroll/scroll-000.png`
- **17%** (`812px`) → `screens/scroll/scroll-017.png`
- **33%** (`1576px`) → `screens/scroll/scroll-033.png`
- **50%** (`2389px`) → `screens/scroll/scroll-050.png`
- **67%** (`3201px`) → `screens/scroll/scroll-067.png`
- **83%** (`3965px`) → `screens/scroll/scroll-083.png`
- **100%** (`4777px`) → `screens/scroll/scroll-100.png`


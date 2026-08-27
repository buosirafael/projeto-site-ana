# Animation Reference

> Cinematic motion design extracted from live DOM. Follow these specs exactly to recreate the experience.

## Motion Technology Stack

| Library | Type | Notes |
|---------|------|-------|
| **Web Animations API (1 active)** | animation |  |

## Scroll Journey

The page is **4.851px** tall. Each frame below shows what the user sees at that scroll depth.

> **Use these screenshots to understand WHAT animates, WHEN it animates, and HOW it moves.**

### 0% — Top / Hero
Scroll position: 0px

![Scroll 0%](../screens/scroll/scroll-000.png)

### 17% — Opening Section
Scroll position: 672px

![Scroll 17%](../screens/scroll/scroll-017.png)

### 33% — First Feature Section
Scroll position: 1.304px

![Scroll 33%](../screens/scroll/scroll-033.png)

### 50% — Mid-Page
Scroll position: 1.976px

![Scroll 50%](../screens/scroll/scroll-050.png)

### 67% — Lower Content
Scroll position: 2.647px

![Scroll 67%](../screens/scroll/scroll-067.png)

### 83% — Near Footer
Scroll position: 3.279px

![Scroll 83%](../screens/scroll/scroll-083.png)

### 100% — Bottom / Footer
Scroll position: 3.951px

![Scroll 100%](../screens/scroll/scroll-100.png)

## Video Elements

| # | Role | Autoplay | Loop | Muted | Size | First Frame |
|---|------|----------|------|-------|------|-------------|
| 1 | background | ✓ | — | ✓ | 1440×720 | [view](../screens/scroll/video-1-frame.png) |

**Video 1 first frame:**

![Video 1 Frame](../screens/scroll/video-1-frame.png)

- **Source:** `https://s1.thcdn.com/video/original/2026/05/2ca7f7cc-f0ab-491f-bb4d-8197416a90bd-Creed_Aventus_Hero_Movie_30s_16-9_VA-02`

## Scroll Animation Patterns

| Pattern | Library | Element Count | Duration | Delay | Easing |
|---------|---------|---------------|----------|-------|--------|
| parallax / sticky scroll | CSS | 2 | — | — | — |

### CSS Implementation

## CSS Keyframes (5 extracted)

### `@keyframes skeleton-loading`

Duration: `1.5s` · Easing: `ease` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.skeleton`

```css
@keyframes skeleton-loading {
  0% {
    background-position-x: 200%;
    background-position-y: 0px;
  }
  100% {
    background-position-x: -200%;
    background-position-y: 0px;
  }
}
```

> Background color/gradient shift · Background position (shimmer/scroll)

### `@keyframes chatbot-sparkle`

Duration: `2.5s` · Easing: `ease-in-out` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.chatbot-animated-border svg`

```css
@keyframes chatbot-sparkle {
  0%, 100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.6;
    transform: scale(0.9);
  }
}
```

> Fade + motion enter animation

### `@keyframes slide-up`

Duration: `1s` · Easing: `ease` · Delay: `0s` · Iteration: `1` · Fill: `forwards`

Used by: `.slide-up[data-astro-cid-yjgbfhnf]`

```css
@keyframes slide-up {
  0% {
    transform: translateY(110vh);
  }
  100% {
    transform: translateY(0px);
  }
}
```

> Transform/motion animation

### `@keyframes spin`

```css
@keyframes spin {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes pulse`

```css
@keyframes pulse {
  50% {
    opacity: 0.5;
  }
}
```

> Opacity fade

## Motion Tokens (CSS Variables)

### Duration Tokens

```css
--modal-animation-duration: .3s;
--duration-speed-default: .2s;
--carousel-animation-speed: .3s;
--default-transition-duration: .15s;
--duration-speed-quick: .1s;
--duration-speed-slow: .3s;
--drawer-animation-speed: .3s;
```

### Easing Tokens

```css
--ease-in: cubic-bezier(.4,0,1,1);
--default-transition-timing-function: cubic-bezier(.4,0,.2,1);
--ease-out: cubic-bezier(0,0,.2,1);
--ease-in-out: cubic-bezier(.4,0,.2,1);
```

### Other Tokens

```css
--accordion-icon-transition: all .1s/**/ease-in;
--color-promotion-200: oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h);
--control-pip-swap-transition: .3s;
--control-pip-transition: .2s;
--color-promotion-100: oklch(from oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h);
--color-promotion-950: oklch(from oklch(from oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h);
--color-promotion-800: oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h);
--color-promotion-700: oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h);
--color-promotion-500: oklch(from oklch(63% .2577 29.23)l c h);
--color-promotion-400: oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(1 - ((1 - l)*.6)) calc(c*.8) h);
--color-promotion-600: oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(l*.8) calc(c*1.1) h);
--color-promotion-300: oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h);
--color-promotion-50: oklch(from oklch(from oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h) calc(1 - ((1 - l)*.6)) calc(c*.8) h);
--color-promotion-900: oklch(from oklch(from oklch(from oklch(from oklch(from oklch(63% .2577 29.23)l c h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h) calc(l*.8) calc(c*1.1) h);
--color-promotion: oklch(63% .2577 29.23);
```

## Global Transition Declarations

These `transition` values were extracted from CSS rules across the site:

```css
transition: max-height 0.3s ease-in-out, padding 0.3s ease-in-out;
transition: top 0.3s ease-in-out;
transition: transform var(--transition-duration)var(--transition-easing);
transition: left 0.3s, right 0.3s;
transition: background-color 0.3s;
transition: transform 0.3s ease-in-out;
transition: opacity;
transition: all var(--duration-speed-slow) ease;
transition: background-color;
transition: transform var(--duration-speed-quick) ease;
transition: transform 0.3s;
transition: color 0.2s;
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
  transition: opacity .3s cubic-bezier(.4,0,1,1),
              transform .3s cubic-bezier(.4,0,1,1);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### Step 3 — Key Motion Principles

- **Video backgrounds** — use `<video autoplay loop muted playsinline>` for background videos. Always include a poster image fallback
- **Duration scale:** `.3s` · `.2s` · `.15s` · `.1s` · `0.3s` — use these values, never invent new durations
- **Always add** `@media (prefers-reduced-motion: reduce) { * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }`

### Step 4 — Scroll Journey Reference

Match what happens at each scroll position:

- **0%** (`0px`) → `screens/scroll/scroll-000.png`
- **17%** (`672px`) → `screens/scroll/scroll-017.png`
- **33%** (`1304px`) → `screens/scroll/scroll-033.png`
- **50%** (`1976px`) → `screens/scroll/scroll-050.png`
- **67%** (`2647px`) → `screens/scroll/scroll-067.png`
- **83%** (`3279px`) → `screens/scroll/scroll-083.png`
- **100%** (`3951px`) → `screens/scroll/scroll-100.png`


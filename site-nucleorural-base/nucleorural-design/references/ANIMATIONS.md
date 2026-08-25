# Animation Reference

> Cinematic motion design extracted from live DOM. Follow these specs exactly to recreate the experience.

## Motion Technology Stack

Pure CSS animations — no external animation libraries detected.

## Scroll Journey

The page is **6.144px** tall. Each frame below shows what the user sees at that scroll depth.

> **Use these screenshots to understand WHAT animates, WHEN it animates, and HOW it moves.**

### 0% — Top / Hero
Scroll position: 0px

![Scroll 0%](../screens/scroll/scroll-000.png)

### 17% — Opening Section
Scroll position: 891px

![Scroll 17%](../screens/scroll/scroll-017.png)

### 33% — First Feature Section
Scroll position: 1.731px

![Scroll 33%](../screens/scroll/scroll-033.png)

### 50% — Mid-Page
Scroll position: 2.622px

![Scroll 50%](../screens/scroll/scroll-050.png)

### 67% — Lower Content
Scroll position: 3.447px

![Scroll 67%](../screens/scroll/scroll-067.png)

### 83% — Near Footer
Scroll position: 3.447px

![Scroll 83%](../screens/scroll/scroll-083.png)

### 100% — Bottom / Footer
Scroll position: 3.447px

![Scroll 100%](../screens/scroll/scroll-100.png)

## Scroll Animation Patterns

| Pattern | Library | Element Count | Duration | Delay | Easing |
|---------|---------|---------------|----------|-------|--------|
| scroll-trigger | GSAP | 2 | — | — | — |
| parallax / sticky scroll | CSS | 7 | — | — | — |

### GSAP Implementation

```javascript
// GSAP ScrollTrigger
gsap.registerPlugin(ScrollTrigger);

gsap.from('.element', {
  opacity: 0,
  y: 60,
  duration: 0.8,
  ease: 'power2.out',
  scrollTrigger: {
    trigger: '.element',
    start: 'top 80%',
    end: 'bottom 20%',
  }
});
```

### CSS Implementation

## CSS Keyframes (362 extracted)

### `@keyframes joinchat_show`

Duration: `0.5s` · Easing: `cubic-bezier(0.18, 0.89, 0.32, 1.28)` · Delay: `10ms` · Iteration: `1` · Fill: `both`

Used by: `.joinchat`, `.joinchat__bubble`

```css
@keyframes joinchat_show {
  0% {
    transform: scale3d(0, 0, 0);
  }
  100% {
    transform: scaleX(1);
  }
}
```

> Transform/motion animation

### `@keyframes progress-bar-stripes`

Duration: `2s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.vc_progress_bar .vc_single_bar .vc_bar.animated`

```css
@keyframes progress-bar-stripes {
  0% {
    background-position-x: 40px;
    background-position-y: 0px;
  }
  100% {
    background-position-x: 0px;
    background-position-y: 0px;
  }
}
```

> Background color/gradient shift · Background position (shimmer/scroll)

### `@keyframes reveal-from-left`

Used by: `.agrikole-simple-image.reveal.lr.animated::after`

```css
@keyframes reveal-from-left {
  0% {
    transform-origin: left top;
    transform: scale(0, 1);
  }
  66.6% {
    transform-origin: left center;
    transform: scale(1, 1);
  }
  66.7% {
    transform-origin: right center;
    transform: scale(1, 1);
  }
  100% {
    transform-origin: right center;
    transform: scale(0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes reveal-from-right`

Used by: `.agrikole-simple-image.reveal.rl.animated::after`

```css
@keyframes reveal-from-right {
  0% {
    transform-origin: right top;
    transform: scale(0, 1);
  }
  66.6% {
    transform-origin: right center;
    transform: scale(1, 1);
  }
  66.7% {
    transform-origin: left center;
    transform: scale(1, 1);
  }
  100% {
    transform-origin: left center;
    transform: scale(0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes flip`

Used by: `.animated.flip`

```css
@keyframes flip {
  0% {
    transform: perspective(400px) rotate3d(0, 1, 0, -360deg);
    animation-timing-function: ease-out;
  }
  40% {
    transform: perspective(400px) translate3d(0px, 0px, 150px) rotate3d(0, 1, 0, -190deg);
    animation-timing-function: ease-out;
  }
  50% {
    transform: perspective(400px) translate3d(0px, 0px, 150px) rotate3d(0, 1, 0, -170deg);
    animation-timing-function: ease-in;
  }
  80% {
    transform: perspective(400px) scale3d(0.95, 0.95, 0.95);
    animation-timing-function: ease-in;
  }
  100% {
    transform: perspective(400px);
    animation-timing-function: ease-in;
  }
}
```

> Transform/motion animation

### `@keyframes cbp-rotation`

Duration: `0.8s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.cbp::after, .cbp-lazyload::after, .cbp-popup-loadingBox::after, .cbp-popup-sing`

```css
@keyframes cbp-rotation {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes cbp-rotation`

Duration: `0.8s` · Easing: `linear` · Delay: `0s` · Iteration: `infinite` · Fill: `none`

Used by: `.cbp::after, .cbp-lazyload::after, .cbp-popup-loadingBox::after, .cbp-popup-sing`

```css
@keyframes cbp-rotation {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes scroll-slider-slide`

Duration: `1s` · Easing: `ease` · Delay: `1s` · Iteration: `1` · Fill: `forwards`

Used by: `.nfd-scroll-slider-horizontal.nfd-scroll-slider-animate > .wp-block-cover:first-`

```css
@keyframes scroll-slider-slide {
  0% {
    margin-left: 0px;
  }
  100% {
    margin-left: -100vw;
  }
}
```

### `@keyframes pmFadeIn`

Duration: `500ms` · Easing: `ease` · Delay: `0s` · Iteration: `1` · Fill: `none`

Used by: `.perfmatters-lazy.pmloaded, .perfmatters-lazy.pmloaded > img, .perfmatters-lazy `

```css
@keyframes pmFadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes load7`

```css
@keyframes load7 {
  0%, 100%, 80% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px -1.3em;
  }
  40% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px 0px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes wpb_ttb`

```css
@keyframes wpb_ttb {
  0% {
    transform: translate(0px, -10%);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_btt`

```css
@keyframes wpb_btt {
  0% {
    transform: translate(0px, 10%);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_ltr`

```css
@keyframes wpb_ltr {
  0% {
    transform: translate(-10%, 0px);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_rtl`

```css
@keyframes wpb_rtl {
  0% {
    transform: translate(10%, 0px);
    opacity: 0;
  }
  100% {
    transform: translate(0px, 0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes wpb_appear`

```css
@keyframes wpb_appear {
  0% {
    transform: scale(0.5);
    opacity: 0.1;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes vc_woo-add-cart-load`

```css
@keyframes vc_woo-add-cart-load {
  0%, 100%, 80% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px -1.3em;
  }
  40% {
    box-shadow: rgba(235, 235, 235, 0.75) 0px 2.5em 0px 0px;
  }
}
```

> Shadow pulse/glow effect

### `@keyframes hide-show`

```css
@keyframes hide-show {
  0%, 66.6% {
    opacity: 0;
    visibility: hidden;
  }
  100%, 66.7% {
    opacity: 1;
    visibility: visible;
  }
}
```

> Opacity fade

### `@keyframes bounce`

```css
@keyframes bounce {
  0%, 20%, 53%, 80%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
    transform: translate3d(0px, 0px, 0px);
  }
  40%, 43% {
    animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
    transform: translate3d(0px, -30px, 0px);
  }
  70% {
    animation-timing-function: cubic-bezier(0.755, 0.05, 0.855, 0.06);
    transform: translate3d(0px, -15px, 0px);
  }
  90% {
    transform: translate3d(0px, -4px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes flash`

```css
@keyframes flash {
  0%, 50%, 100% {
    opacity: 1;
  }
  25%, 75% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes pulse`

```css
@keyframes pulse {
  0% {
    transform: scale3d(1, 1, 1);
  }
  50% {
    transform: scale3d(1.05, 1.05, 1.05);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rubberBand`

```css
@keyframes rubberBand {
  0% {
    transform: scale3d(1, 1, 1);
  }
  30% {
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes shake`

```css
@keyframes shake {
  0%, 100% {
    transform: translate3d(0px, 0px, 0px);
  }
  10%, 30%, 50%, 70%, 90% {
    transform: translate3d(-10px, 0px, 0px);
  }
  20%, 40%, 60%, 80% {
    transform: translate3d(10px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes headShake`

```css
@keyframes headShake {
  0% {
    transform: translateX(0px);
  }
  6.5% {
    transform: translateX(-6px) rotateY(-9deg);
  }
  18.5% {
    transform: translateX(5px) rotateY(7deg);
  }
  31.5% {
    transform: translateX(-3px) rotateY(-5deg);
  }
  43.5% {
    transform: translateX(2px) rotateY(3deg);
  }
  50% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes swing`

```css
@keyframes swing {
  20% {
    transform: rotate3d(0, 0, 1, 15deg);
  }
  40% {
    transform: rotate3d(0, 0, 1, -10deg);
  }
  60% {
    transform: rotate3d(0, 0, 1, 5deg);
  }
  80% {
    transform: rotate3d(0, 0, 1, -5deg);
  }
  100% {
    transform: rotate3d(0, 0, 1, 0deg);
  }
}
```

> Transform/motion animation

### `@keyframes tada`

```css
@keyframes tada {
  0% {
    transform: scale3d(1, 1, 1);
  }
  10%, 20% {
    transform: scale3d(0.9, 0.9, 0.9) rotate3d(0, 0, 1, -3deg);
  }
  30%, 50%, 70%, 90% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, 3deg);
  }
  40%, 60%, 80% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, -3deg);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}
```

> Transform/motion animation

### `@keyframes wobble`

```css
@keyframes wobble {
  0% {
    transform: none;
  }
  15% {
    transform: translate3d(-25%, 0px, 0px) rotate3d(0, 0, 1, -5deg);
  }
  30% {
    transform: translate3d(20%, 0px, 0px) rotate3d(0, 0, 1, 3deg);
  }
  45% {
    transform: translate3d(-15%, 0px, 0px) rotate3d(0, 0, 1, -3deg);
  }
  60% {
    transform: translate3d(10%, 0px, 0px) rotate3d(0, 0, 1, 2deg);
  }
  75% {
    transform: translate3d(-5%, 0px, 0px) rotate3d(0, 0, 1, -1deg);
  }
  100% {
    transform: none;
  }
}
```

> Transform/motion animation

### `@keyframes jello`

```css
@keyframes jello {
  0%, 11.1%, 100% {
    transform: none;
  }
  22.2% {
    transform: skewX(-12.5deg) skewY(-12.5deg);
  }
  33.3% {
    transform: skewX(6.25deg) skewY(6.25deg);
  }
  44.4% {
    transform: skewX(-3.125deg) skewY(-3.125deg);
  }
  55.5% {
    transform: skewX(1.5625deg) skewY(1.5625deg);
  }
  66.6% {
    transform: skewX(-0.78125deg) skewY(-0.78125deg);
  }
  77.7% {
    transform: skewX(0.390625deg) skewY(0.390625deg);
  }
  88.8% {
    transform: skewX(-0.195312deg) skewY(-0.195312deg);
  }
}
```

> Transform/motion animation

### `@keyframes bounceIn`

```css
@keyframes bounceIn {
  0%, 20%, 40%, 60%, 80%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  20% {
    transform: scale3d(1.1, 1.1, 1.1);
  }
  40% {
    transform: scale3d(0.9, 0.9, 0.9);
  }
  60% {
    opacity: 1;
    transform: scale3d(1.03, 1.03, 1.03);
  }
  80% {
    transform: scale3d(0.97, 0.97, 0.97);
  }
  100% {
    opacity: 1;
    transform: scale3d(1, 1, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInDown`

```css
@keyframes bounceInDown {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(0px, -3000px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(0px, 25px, 0px);
  }
  75% {
    transform: translate3d(0px, -10px, 0px);
  }
  90% {
    transform: translate3d(0px, 5px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInLeft`

```css
@keyframes bounceInLeft {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(-3000px, 0px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(25px, 0px, 0px);
  }
  75% {
    transform: translate3d(-10px, 0px, 0px);
  }
  90% {
    transform: translate3d(5px, 0px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInRight`

```css
@keyframes bounceInRight {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(3000px, 0px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(-25px, 0px, 0px);
  }
  75% {
    transform: translate3d(10px, 0px, 0px);
  }
  90% {
    transform: translate3d(-5px, 0px, 0px);
  }
  100% {
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceInUp`

```css
@keyframes bounceInUp {
  0%, 60%, 75%, 90%, 100% {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  0% {
    opacity: 0;
    transform: translate3d(0px, 3000px, 0px);
  }
  60% {
    opacity: 1;
    transform: translate3d(0px, -20px, 0px);
  }
  75% {
    transform: translate3d(0px, 10px, 0px);
  }
  90% {
    transform: translate3d(0px, -5px, 0px);
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOut`

```css
@keyframes bounceOut {
  20% {
    transform: scale3d(0.9, 0.9, 0.9);
  }
  50%, 55% {
    opacity: 1;
    transform: scale3d(1.1, 1.1, 1.1);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutDown`

```css
@keyframes bounceOutDown {
  20% {
    transform: translate3d(0px, 10px, 0px);
  }
  40%, 45% {
    opacity: 1;
    transform: translate3d(0px, -20px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutLeft`

```css
@keyframes bounceOutLeft {
  20% {
    opacity: 1;
    transform: translate3d(20px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(-2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutRight`

```css
@keyframes bounceOutRight {
  20% {
    opacity: 1;
    transform: translate3d(-20px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceOutUp`

```css
@keyframes bounceOutUp {
  20% {
    transform: translate3d(0px, -10px, 0px);
  }
  40%, 45% {
    opacity: 1;
    transform: translate3d(0px, 20px, 0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeInDown`

```css
@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translate3d(0px, -20px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInDownBig`

```css
@keyframes fadeInDownBig {
  0% {
    opacity: 0;
    transform: translate3d(0px, -1000px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInLeft`

```css
@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translate3d(-20px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInLeftBig`

```css
@keyframes fadeInLeftBig {
  0% {
    opacity: 0;
    transform: translate3d(-1000px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInRight`

```css
@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translate3d(20px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInRightBig`

```css
@keyframes fadeInRightBig {
  0% {
    opacity: 0;
    transform: translate3d(1000px, 0px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInUp`

```css
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translate3d(0px, 20px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInUpBig`

```css
@keyframes fadeInUpBig {
  0% {
    opacity: 0;
    transform: translate3d(0px, 1000px, 0px);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut`

```css
@keyframes fadeOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOutDown`

```css
@keyframes fadeOutDown {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 100%, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutDownBig`

```css
@keyframes fadeOutDownBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, 2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutLeft`

```css
@keyframes fadeOutLeft {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(-100%, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutLeftBig`

```css
@keyframes fadeOutLeftBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(-2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutRight`

```css
@keyframes fadeOutRight {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(100%, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutRightBig`

```css
@keyframes fadeOutRightBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(2000px, 0px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutUp`

```css
@keyframes fadeOutUp {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -100%, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutUpBig`

```css
@keyframes fadeOutUpBig {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -2000px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipInX`

```css
@keyframes flipInX {
  0% {
    transform: perspective(400px) rotate3d(1, 0, 0, 90deg);
    animation-timing-function: ease-in;
    opacity: 0;
  }
  40% {
    transform: perspective(400px) rotate3d(1, 0, 0, -20deg);
    animation-timing-function: ease-in;
  }
  60% {
    transform: perspective(400px) rotate3d(1, 0, 0, 10deg);
    opacity: 1;
  }
  80% {
    transform: perspective(400px) rotate3d(1, 0, 0, -5deg);
  }
  100% {
    transform: perspective(400px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipInY`

```css
@keyframes flipInY {
  0% {
    transform: perspective(400px) rotate3d(0, 1, 0, 90deg);
    animation-timing-function: ease-in;
    opacity: 0;
  }
  40% {
    transform: perspective(400px) rotate3d(0, 1, 0, -20deg);
    animation-timing-function: ease-in;
  }
  60% {
    transform: perspective(400px) rotate3d(0, 1, 0, 10deg);
    opacity: 1;
  }
  80% {
    transform: perspective(400px) rotate3d(0, 1, 0, -5deg);
  }
  100% {
    transform: perspective(400px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOutX`

```css
@keyframes flipOutX {
  0% {
    transform: perspective(400px);
  }
  30% {
    transform: perspective(400px) rotate3d(1, 0, 0, -20deg);
    opacity: 1;
  }
  100% {
    transform: perspective(400px) rotate3d(1, 0, 0, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOutY`

```css
@keyframes flipOutY {
  0% {
    transform: perspective(400px);
  }
  30% {
    transform: perspective(400px) rotate3d(0, 1, 0, -15deg);
    opacity: 1;
  }
  100% {
    transform: perspective(400px) rotate3d(0, 1, 0, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes lightSpeedIn`

```css
@keyframes lightSpeedIn {
  0% {
    transform: translate3d(100%, 0px, 0px) skewX(-30deg);
    opacity: 0;
  }
  60% {
    transform: skewX(20deg);
    opacity: 1;
  }
  80% {
    transform: skewX(-5deg);
    opacity: 1;
  }
  100% {
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes lightSpeedOut`

```css
@keyframes lightSpeedOut {
  0% {
    opacity: 1;
  }
  100% {
    transform: translate3d(100%, 0px, 0px) skewX(30deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateIn`

```css
@keyframes rotateIn {
  0% {
    transform-origin: center center;
    transform: rotate3d(0, 0, 1, -200deg);
    opacity: 0;
  }
  100% {
    transform-origin: center center;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInDownLeft`

```css
@keyframes rotateInDownLeft {
  0% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
  100% {
    transform-origin: left bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInDownRight`

```css
@keyframes rotateInDownRight {
  0% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
  100% {
    transform-origin: right bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInUpLeft`

```css
@keyframes rotateInUpLeft {
  0% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
  100% {
    transform-origin: left bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateInUpRight`

```css
@keyframes rotateInUpRight {
  0% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, -90deg);
    opacity: 0;
  }
  100% {
    transform-origin: right bottom;
    transform: none;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOut`

```css
@keyframes rotateOut {
  0% {
    transform-origin: center center;
    opacity: 1;
  }
  100% {
    transform-origin: center center;
    transform: rotate3d(0, 0, 1, 200deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutDownLeft`

```css
@keyframes rotateOutDownLeft {
  0% {
    transform-origin: left bottom;
    opacity: 1;
  }
  100% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, 45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutDownRight`

```css
@keyframes rotateOutDownRight {
  0% {
    transform-origin: right bottom;
    opacity: 1;
  }
  100% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutUpLeft`

```css
@keyframes rotateOutUpLeft {
  0% {
    transform-origin: left bottom;
    opacity: 1;
  }
  100% {
    transform-origin: left bottom;
    transform: rotate3d(0, 0, 1, -45deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateOutUpRight`

```css
@keyframes rotateOutUpRight {
  0% {
    transform-origin: right bottom;
    opacity: 1;
  }
  100% {
    transform-origin: right bottom;
    transform: rotate3d(0, 0, 1, 90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes hinge`

```css
@keyframes hinge {
  0% {
    transform-origin: left top;
    animation-timing-function: ease-in-out;
  }
  20%, 60% {
    transform: rotate3d(0, 0, 1, 80deg);
    transform-origin: left top;
    animation-timing-function: ease-in-out;
  }
  40%, 80% {
    transform: rotate3d(0, 0, 1, 60deg);
    transform-origin: left top;
    animation-timing-function: ease-in-out;
    opacity: 1;
  }
  100% {
    transform: translate3d(0px, 700px, 0px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes jackInTheBox`

```css
@keyframes jackInTheBox {
  0% {
    opacity: 0;
    transform: scale(0.1) rotate(30deg);
    transform-origin: center bottom;
  }
  50% {
    transform: rotate(-10deg);
  }
  70% {
    transform: rotate(3deg);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes rollIn`

```css
@keyframes rollIn {
  0% {
    opacity: 0;
    transform: translate3d(-100%, 0px, 0px) rotate3d(0, 0, 1, -120deg);
  }
  100% {
    opacity: 1;
    transform: none;
  }
}
```

> Fade + motion enter animation

### `@keyframes rollOut`

```css
@keyframes rollOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate3d(100%, 0px, 0px) rotate3d(0, 0, 1, 120deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomIn`

```css
@keyframes zoomIn {
  0% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInDown`

```css
@keyframes zoomInDown {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, -1000px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, 60px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInLeft`

```css
@keyframes zoomInLeft {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(-1000px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(10px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInRight`

```css
@keyframes zoomInRight {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(1000px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(-10px, 0px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomInUp`

```css
@keyframes zoomInUp {
  0% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, 1000px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  60% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, -60px, 0px);
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOut`

```css
@keyframes zoomOut {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
    transform: scale3d(0.3, 0.3, 0.3);
  }
  100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutDown`

```css
@keyframes zoomOutDown {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, -60px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, 2000px, 0px);
    transform-origin: center bottom;
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutLeft`

```css
@keyframes zoomOutLeft {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(42px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: scale(0.1) translate3d(-2000px, 0px, 0px);
    transform-origin: left center;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutRight`

```css
@keyframes zoomOutRight {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(-42px, 0px, 0px);
  }
  100% {
    opacity: 0;
    transform: scale(0.1) translate3d(2000px, 0px, 0px);
    transform-origin: right center;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoomOutUp`

```css
@keyframes zoomOutUp {
  40% {
    opacity: 1;
    transform: scale3d(0.475, 0.475, 0.475) translate3d(0px, 60px, 0px);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  100% {
    opacity: 0;
    transform: scale3d(0.1, 0.1, 0.1) translate3d(0px, -2000px, 0px);
    transform-origin: center bottom;
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideInDown`

```css
@keyframes slideInDown {
  0% {
    transform: translate3d(0px, -100%, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInLeft`

```css
@keyframes slideInLeft {
  0% {
    transform: translate3d(-100%, 0px, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInRight`

```css
@keyframes slideInRight {
  0% {
    transform: translate3d(100%, 0px, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideInUp`

```css
@keyframes slideInUp {
  0% {
    transform: translate3d(0px, 100%, 0px);
    visibility: visible;
  }
  100% {
    transform: translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutDown`

```css
@keyframes slideOutDown {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(0px, 100%, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutLeft`

```css
@keyframes slideOutLeft {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(-100%, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutRight`

```css
@keyframes slideOutRight {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(100%, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideOutUp`

```css
@keyframes slideOutUp {
  0% {
    transform: translate3d(0px, 0px, 0px);
  }
  100% {
    visibility: hidden;
    transform: translate3d(0px, -100%, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading`

```css
@keyframes animsition-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading`

```css
@keyframes animsition-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading-reverse`

```css
@keyframes animsition-loading-reverse {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes animsition-loading-reverse`

```css
@keyframes animsition-loading-reverse {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes fade-in`

```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade-in`

```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade-out`

```css
@keyframes fade-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fade-out`

```css
@keyframes fade-out {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fade-in-up`

```css
@keyframes fade-in-up {
  0% {
    transform: translateY(500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up`

```css
@keyframes fade-in-up {
  0% {
    transform: translateY(500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up`

```css
@keyframes fade-out-up {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up`

```css
@keyframes fade-out-up {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-sm`

```css
@keyframes fade-in-up-sm {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-sm`

```css
@keyframes fade-in-up-sm {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-sm`

```css
@keyframes fade-out-up-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-sm`

```css
@keyframes fade-out-up-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-lg`

```css
@keyframes fade-in-up-lg {
  0% {
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-up-lg`

```css
@keyframes fade-in-up-lg {
  0% {
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-lg`

```css
@keyframes fade-out-up-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-up-lg`

```css
@keyframes fade-out-up-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(-1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down`

```css
@keyframes fade-in-down {
  0% {
    transform: translateY(-500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down`

```css
@keyframes fade-in-down {
  0% {
    transform: translateY(-500px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down`

```css
@keyframes fade-out-down {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down`

```css
@keyframes fade-out-down {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down-sm`

```css
@keyframes fade-in-down-sm {
  0% {
    transform: translateY(-100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-down-sm`

```css
@keyframes fade-in-down-sm {
  0% {
    transform: translateY(-100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-sm`

```css
@keyframes fade-out-down-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-sm`

```css
@keyframes fade-out-down-sm {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-lg`

```css
@keyframes fade-out-down-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-down-lg`

```css
@keyframes fade-out-down-lg {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  100% {
    transform: translateY(1000px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left`

```css
@keyframes fade-in-left {
  0% {
    transform: translateX(-500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left`

```css
@keyframes fade-in-left {
  0% {
    transform: translateX(-500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left`

```css
@keyframes fade-out-left {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left`

```css
@keyframes fade-out-left {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-sm`

```css
@keyframes fade-in-left-sm {
  0% {
    transform: translateX(-100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-sm`

```css
@keyframes fade-in-left-sm {
  0% {
    transform: translateX(-100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-sm`

```css
@keyframes fade-out-left-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-sm`

```css
@keyframes fade-out-left-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-lg`

```css
@keyframes fade-in-left-lg {
  0% {
    transform: translateX(-1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-left-lg`

```css
@keyframes fade-in-left-lg {
  0% {
    transform: translateX(-1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-lg`

```css
@keyframes fade-out-left-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-left-lg`

```css
@keyframes fade-out-left-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(-1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right`

```css
@keyframes fade-in-right {
  0% {
    transform: translateX(500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right`

```css
@keyframes fade-in-right {
  0% {
    transform: translateX(500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right`

```css
@keyframes fade-out-right {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right`

```css
@keyframes fade-out-right {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-sm`

```css
@keyframes fade-in-right-sm {
  0% {
    transform: translateX(100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-sm`

```css
@keyframes fade-in-right-sm {
  0% {
    transform: translateX(100px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-sm`

```css
@keyframes fade-out-right-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-sm`

```css
@keyframes fade-out-right-sm {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(100px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-lg`

```css
@keyframes fade-in-right-lg {
  0% {
    transform: translateX(1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-in-right-lg`

```css
@keyframes fade-in-right-lg {
  0% {
    transform: translateX(1500px);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-lg`

```css
@keyframes fade-out-right-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fade-out-right-lg`

```css
@keyframes fade-out-right-lg {
  0% {
    transform: translateX(0px);
    opacity: 1;
  }
  100% {
    transform: translateX(1500px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in`

```css
@keyframes rotate-in {
  0% {
    transform: rotate(-90deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in`

```css
@keyframes rotate-in {
  0% {
    transform: rotate(-90deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out`

```css
@keyframes rotate-out {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(90deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out`

```css
@keyframes rotate-out {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(90deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-sm`

```css
@keyframes rotate-in-sm {
  0% {
    transform: rotate(-45deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-sm`

```css
@keyframes rotate-in-sm {
  0% {
    transform: rotate(-45deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-sm`

```css
@keyframes rotate-out-sm {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(45deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-sm`

```css
@keyframes rotate-out-sm {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(45deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-lg`

```css
@keyframes rotate-in-lg {
  0% {
    transform: rotate(-180deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-in-lg`

```css
@keyframes rotate-in-lg {
  0% {
    transform: rotate(-180deg);
    transform-origin: center center;
    opacity: 0;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-lg`

```css
@keyframes rotate-out-lg {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(180deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rotate-out-lg`

```css
@keyframes rotate-out-lg {
  0% {
    transform: rotate(0deg);
    transform-origin: center center;
    opacity: 1;
  }
  0%, 100% {
    transform-origin: center center;
  }
  100% {
    transform: rotate(180deg);
    transform-origin: center center;
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x`

```css
@keyframes flip-in-x {
  0% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x`

```css
@keyframes flip-in-x {
  0% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x`

```css
@keyframes flip-out-x {
  0% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x`

```css
@keyframes flip-out-x {
  0% {
    transform: perspective(550px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-nr`

```css
@keyframes flip-in-x-nr {
  0% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-nr`

```css
@keyframes flip-in-x-nr {
  0% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-nr`

```css
@keyframes flip-out-x-nr {
  0% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-nr`

```css
@keyframes flip-out-x-nr {
  0% {
    transform: perspective(100px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-fr`

```css
@keyframes flip-in-x-fr {
  0% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-x-fr`

```css
@keyframes flip-in-x-fr {
  0% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-fr`

```css
@keyframes flip-out-x-fr {
  0% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-x-fr`

```css
@keyframes flip-out-x-fr {
  0% {
    transform: perspective(1000px) rotateX(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateX(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y`

```css
@keyframes flip-in-y {
  0% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y`

```css
@keyframes flip-in-y {
  0% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y`

```css
@keyframes flip-out-y {
  0% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y`

```css
@keyframes flip-out-y {
  0% {
    transform: perspective(550px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(550px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-nr`

```css
@keyframes flip-in-y-nr {
  0% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-nr`

```css
@keyframes flip-in-y-nr {
  0% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-nr`

```css
@keyframes flip-out-y-nr {
  0% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-nr`

```css
@keyframes flip-out-y-nr {
  0% {
    transform: perspective(100px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(100px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-fr`

```css
@keyframes flip-in-y-fr {
  0% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in-y-fr`

```css
@keyframes flip-in-y-fr {
  0% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
  100% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-fr`

```css
@keyframes flip-out-y-fr {
  0% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out-y-fr`

```css
@keyframes flip-out-y-fr {
  0% {
    transform: perspective(1000px) rotateY(0deg);
    opacity: 1;
  }
  100% {
    transform: perspective(1000px) rotateY(90deg);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in`

```css
@keyframes zoom-in {
  0% {
    transform: scale(0.7);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in`

```css
@keyframes zoom-in {
  0% {
    transform: scale(0.7);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out`

```css
@keyframes zoom-out {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.7);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out`

```css
@keyframes zoom-out {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.7);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-sm`

```css
@keyframes zoom-in-sm {
  0% {
    transform: scale(0.95);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-sm`

```css
@keyframes zoom-in-sm {
  0% {
    transform: scale(0.95);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-sm`

```css
@keyframes zoom-out-sm {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.95);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-sm`

```css
@keyframes zoom-out-sm {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.95);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-lg`

```css
@keyframes zoom-in-lg {
  0% {
    transform: scale(0.4);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-in-lg`

```css
@keyframes zoom-in-lg {
  0% {
    transform: scale(0.4);
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-lg`

```css
@keyframes zoom-out-lg {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.4);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes zoom-out-lg`

```css
@keyframes zoom-out-lg {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(0.4);
  }
  50%, 100% {
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes overlay-slide-in-top`

```css
@keyframes overlay-slide-in-top {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-top`

```css
@keyframes overlay-slide-in-top {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-top`

```css
@keyframes overlay-slide-out-top {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-top`

```css
@keyframes overlay-slide-out-top {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-bottom`

```css
@keyframes overlay-slide-in-bottom {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-bottom`

```css
@keyframes overlay-slide-in-bottom {
  0% {
    height: 100%;
  }
  100% {
    height: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-bottom`

```css
@keyframes overlay-slide-out-bottom {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-bottom`

```css
@keyframes overlay-slide-out-bottom {
  0% {
    height: 0px;
  }
  100% {
    height: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-left`

```css
@keyframes overlay-slide-in-left {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-left`

```css
@keyframes overlay-slide-in-left {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-left`

```css
@keyframes overlay-slide-out-left {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-left`

```css
@keyframes overlay-slide-out-left {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-right`

```css
@keyframes overlay-slide-in-right {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-in-right`

```css
@keyframes overlay-slide-in-right {
  0% {
    width: 100%;
  }
  100% {
    width: 0px;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-right`

```css
@keyframes overlay-slide-out-right {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes overlay-slide-out-right`

```css
@keyframes overlay-slide-out-right {
  0% {
    width: 0px;
  }
  100% {
    width: 100%;
  }
}
```

> Dimension expand/collapse

### `@keyframes fa-spin`

```css
@keyframes fa-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(359deg);
  }
}
```

> Transform/motion animation

### `@keyframes fa-spin`

```css
@keyframes fa-spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(359deg);
  }
}
```

> Transform/motion animation

### `@keyframes blink`

```css
@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes blink`

```css
@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes rev-ani-mouse`

```css
@keyframes rev-ani-mouse {
  0% {
    opacity: 1;
    top: 0%;
  }
  30% {
    opacity: 1;
    top: 30%;
  }
  70% {
    opacity: 0;
    top: 30%;
  }
  100% {
    opacity: 0;
    top: 0%;
  }
}
```

> Opacity fade

### `@keyframes circle-fade-inf`

```css
@keyframes circle-fade-inf {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(1.08);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_open_text`

```css
@keyframes joinchat_open_text {
  0% {
    max-width: 0px;
    opacity: 0;
  }
  60% {
    max-width: var(--mw);
    opacity: 0;
  }
  100% {
    max-width: var(--mw);
    opacity: 1;
  }
}
```

> Opacity fade · Dimension expand/collapse

### `@keyframes joinchat_badge_in`

```css
@keyframes joinchat_badge_in {
  0% {
    opacity: 0;
    transform: translate3d(0px, 50px, 0px);
  }
  100% {
    opacity: 1;
    transform: translateZ(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_badge_out`

```css
@keyframes joinchat_badge_out {
  0% {
    opacity: 1;
    transform: translateZ(0px);
  }
  100% {
    opacity: 0;
    transform: translate3d(0px, -20px, 0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes joinchat_send_svg`

```css
@keyframes joinchat_send_svg {
  0%, 50%, 100% {
    stroke-dashoffset: var(--stroke);
  }
  5%, 45% {
    stroke-dashoffset: 0;
  }
}
```

> SVG stroke animation

### `@keyframes joinchat_image_loop`

```css
@keyframes joinchat_image_loop {
  0% {
    opacity: 0;
  }
  3%, 20% {
    opacity: 1;
  }
  25%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes joinchat_tootlip`

```css
@keyframes joinchat_tootlip {
  0% {
    opacity: 0;
    transform: scaleY(0);
  }
  1%, 20% {
    opacity: 1;
    transform: scaleX(1);
  }
  25%, 100% {
    opacity: 0;
    transform: scaleX(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut`

```css
@keyframes fadeOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes quicksand-off`

```css
@keyframes quicksand-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-off`

```css
@keyframes quicksand-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-on`

```css
@keyframes quicksand-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes quicksand-on`

```css
@keyframes quicksand-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOut-off`

```css
@keyframes fadeOut-off {
  0% {
    opacity: 1;
  }
  80%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-off`

```css
@keyframes fadeOut-off {
  0% {
    opacity: 1;
  }
  80%, 100% {
    opacity: 0;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-on`

```css
@keyframes fadeOut-on {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeOut-on`

```css
@keyframes fadeOut-on {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes flipOut-out`

```css
@keyframes flipOut-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateY(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-out`

```css
@keyframes flipOut-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateY(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-in`

```css
@keyframes flipOut-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateY(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipOut-in`

```css
@keyframes flipOut-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateY(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-out`

```css
@keyframes flipBottom-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateX(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-out`

```css
@keyframes flipBottom-out {
  50%, 100% {
    transform: translateZ(-1000px) rotateX(-90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-in`

```css
@keyframes flipBottom-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateX(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes flipBottom-in`

```css
@keyframes flipBottom-in {
  0%, 50% {
    transform: translateZ(-1000px) rotateX(90deg);
    opacity: 0.2;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-out`

```css
@keyframes scaleSides-out {
  50%, 100% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-out`

```css
@keyframes scaleSides-out {
  50%, 100% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-in`

```css
@keyframes scaleSides-in {
  0%, 50% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleSides-in`

```css
@keyframes scaleSides-in {
  0%, 50% {
    transform: scale(0.6);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-off`

```css
@keyframes skew-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(20deg, 0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-off`

```css
@keyframes skew-off {
  100% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(20deg, 0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-on`

```css
@keyframes skew-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(0deg, 20deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes skew-on`

```css
@keyframes skew-on {
  0% {
    opacity: 0;
    transform: scale3d(0, 0, 0) skew(0deg, 20deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-out`

```css
@keyframes fadeOutTop-out {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  50%, 100% {
    transform: translateY(-30px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-out`

```css
@keyframes fadeOutTop-out {
  0% {
    transform: translateY(0px);
    opacity: 1;
  }
  50%, 100% {
    transform: translateY(-30px);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-in`

```css
@keyframes fadeOutTop-in {
  0%, 50% {
    transform: translateY(-30px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeOutTop-in`

```css
@keyframes fadeOutTop-in {
  0%, 50% {
    transform: translateY(-30px);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-out`

```css
@keyframes slideLeft-out {
  0% {
    opacity: 1;
    transform: scale(1);
  }
  25% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
  100% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-out`

```css
@keyframes slideLeft-out {
  0% {
    opacity: 1;
    transform: scale(1);
  }
  25% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
  100% {
    opacity: 0.75;
    transform: scale(0.8) translateX(-200%);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-in`

```css
@keyframes slideLeft-in {
  0%, 25% {
    opacity: 0.75;
    transform: scale(0.8) translateX(200%);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateX(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideLeft-in`

```css
@keyframes slideLeft-in {
  0%, 25% {
    opacity: 0.75;
    transform: scale(0.8) translateX(200%);
  }
  75% {
    opacity: 0.75;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateX(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out`

```css
@keyframes flip-out {
  100% {
    opacity: 0;
    transform: rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-out`

```css
@keyframes flip-out {
  100% {
    opacity: 0;
    transform: rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in`

```css
@keyframes flip-in {
  0% {
    opacity: 0;
    transform: rotateY(-90deg);
  }
  100% {
    opacity: 1;
    transform: rotateY(0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes flip-in`

```css
@keyframes flip-in {
  0% {
    opacity: 0;
    transform: rotateY(-90deg);
  }
  100% {
    opacity: 1;
    transform: rotateY(0deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes slideDelay-out`

```css
@keyframes slideDelay-out {
  100% {
    transform: translateX(-100%);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-out`

```css
@keyframes slideDelay-out {
  100% {
    transform: translateX(-100%);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-in`

```css
@keyframes slideDelay-in {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes slideDelay-in`

```css
@keyframes slideDelay-in {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0px);
  }
}
```

> Transform/motion animation

### `@keyframes rotateSides-out`

```css
@keyframes rotateSides-out {
  100% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-out`

```css
@keyframes rotateSides-out {
  100% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-in`

```css
@keyframes rotateSides-in {
  0% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
  40% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateSides-in`

```css
@keyframes rotateSides-in {
  0% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
  40% {
    opacity: 0;
    transform: translateZ(-500px) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-out`

```css
@keyframes foldLeft-out {
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-out`

```css
@keyframes foldLeft-out {
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-in`

```css
@keyframes foldLeft-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes foldLeft-in`

```css
@keyframes foldLeft-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-out`

```css
@keyframes unfold-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-out`

```css
@keyframes unfold-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-in`

```css
@keyframes unfold-in {
  0% {
    opacity: 0;
    transform: translateX(100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes unfold-in`

```css
@keyframes unfold-in {
  0% {
    opacity: 0;
    transform: translateX(100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-out`

```css
@keyframes scaleDown-out {
  100% {
    opacity: 0;
    transform: scale(0.8);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-out`

```css
@keyframes scaleDown-out {
  100% {
    opacity: 0;
    transform: scale(0.8);
  }
}
```

> Fade + motion enter animation

### `@keyframes scaleDown-in`

```css
@keyframes scaleDown-in {
  0% {
    transform: translateX(100%);
  }
}
```

> Transform/motion animation

### `@keyframes scaleDown-in`

```css
@keyframes scaleDown-in {
  0% {
    transform: translateX(100%);
  }
}
```

> Transform/motion animation

### `@keyframes frontRow-out`

```css
@keyframes frontRow-out {
  100% {
    transform: translateX(-60%) scale(0.8);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-out`

```css
@keyframes frontRow-out {
  100% {
    transform: translateX(-60%) scale(0.8);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-in`

```css
@keyframes frontRow-in {
  0% {
    transform: translateX(100%) scale(0.8);
  }
  100% {
    opacity: 1;
    transform: translateX(0%) scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes frontRow-in`

```css
@keyframes frontRow-in {
  0% {
    transform: translateX(100%) scale(0.8);
  }
  100% {
    opacity: 1;
    transform: translateX(0%) scale(1);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-out`

```css
@keyframes rotateRoom-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-out`

```css
@keyframes rotateRoom-out {
  90% {
    opacity: 0.3;
  }
  100% {
    opacity: 0;
    transform: translateX(-100%) rotateY(90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-in`

```css
@keyframes rotateRoom-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes rotateRoom-in`

```css
@keyframes rotateRoom-in {
  0% {
    opacity: 0.3;
    transform: translateX(100%) rotateY(-90deg);
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-out`

```css
@keyframes bounceBottom-out {
  100% {
    transform: translateY(100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-out`

```css
@keyframes bounceBottom-out {
  100% {
    transform: translateY(100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-in`

```css
@keyframes bounceBottom-in {
  0% {
    transform: translateY(100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceBottom-in`

```css
@keyframes bounceBottom-in {
  0% {
    transform: translateY(100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-out`

```css
@keyframes bounceLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-out`

```css
@keyframes bounceLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-in`

```css
@keyframes bounceLeft-in {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceLeft-in`

```css
@keyframes bounceLeft-in {
  0% {
    transform: translateX(-100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-out`

```css
@keyframes bounceTop-out {
  100% {
    transform: translateY(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-out`

```css
@keyframes bounceTop-out {
  100% {
    transform: translateY(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-in`

```css
@keyframes bounceTop-in {
  0% {
    transform: translateY(-100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes bounceTop-in`

```css
@keyframes bounceTop-in {
  0% {
    transform: translateY(-100%);
    opacity: 0;
  }
  100% {
    transform: translateY(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-out`

```css
@keyframes moveLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-out`

```css
@keyframes moveLeft-out {
  100% {
    transform: translateX(-100%);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-in`

```css
@keyframes moveLeft-in {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes moveLeft-in`

```css
@keyframes moveLeft-in {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0px);
    opacity: 1;
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInBottomToTop`

```css
@keyframes fadeInBottomToTop {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInBottomToTop`

```css
@keyframes fadeInBottomToTop {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeIn`

```css
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fadeInToTop`

```css
@keyframes fadeInToTop {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes fadeInToTop`

```css
@keyframes fadeInToTop {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
```

> Fade + motion enter animation

### `@keyframes kenburns`

```css
@keyframes kenburns {
  0% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes kenburns`

```css
@keyframes kenburns {
  0% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownLeft`

```css
@keyframes kenburnsDownLeft {
  0% {
    transform: scale(1.5) translate(10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownLeft`

```css
@keyframes kenburnsDownLeft {
  0% {
    transform: scale(1.5) translate(10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownRight`

```css
@keyframes kenburnsDownRight {
  0% {
    transform: scale(1.5) translate(-10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDownRight`

```css
@keyframes kenburnsDownRight {
  0% {
    transform: scale(1.5) translate(-10%, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDown`

```css
@keyframes kenburnsDown {
  0% {
    transform: scale(1.5) translate(0px, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsDown`

```css
@keyframes kenburnsDown {
  0% {
    transform: scale(1.5) translate(0px, -10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsLeft`

```css
@keyframes kenburnsLeft {
  0% {
    transform: scale(1.5) translate(10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsLeft`

```css
@keyframes kenburnsLeft {
  0% {
    transform: scale(1.5) translate(10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsRight`

```css
@keyframes kenburnsRight {
  0% {
    transform: scale(1.5) translate(-10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsRight`

```css
@keyframes kenburnsRight {
  0% {
    transform: scale(1.5) translate(-10%, 0px);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpLeft`

```css
@keyframes kenburnsUpLeft {
  0% {
    transform: scale(1.5) translate(10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpLeft`

```css
@keyframes kenburnsUpLeft {
  0% {
    transform: scale(1.5) translate(10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpRight`

```css
@keyframes kenburnsUpRight {
  0% {
    transform: scale(1.5) translate(-10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUpRight`

```css
@keyframes kenburnsUpRight {
  0% {
    transform: scale(1.5) translate(-10%, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUp`

```css
@keyframes kenburnsUp {
  0% {
    transform: scale(1.5) translate(0px, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes kenburnsUp`

```css
@keyframes kenburnsUp {
  0% {
    transform: scale(1.5) translate(0px, 10%);
  }
  100% {
    transform: scale(1) translate(0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes fade`

```css
@keyframes fade {
  0% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes fade`

```css
@keyframes fade {
  0% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}
```

> Opacity fade

### `@keyframes rev-ani-mouse`

```css
@keyframes rev-ani-mouse {
  0% {
    opacity: 1;
    top: 29%;
  }
  15% {
    opacity: 1;
    top: 70%;
  }
  50% {
    opacity: 0;
    top: 70%;
  }
  100% {
    opacity: 0;
    top: 29%;
  }
}
```

> Opacity fade

### `@keyframes tp-rotateplane`

```css
@keyframes tp-rotateplane {
  0% {
    transform: perspective(120px) rotateX(0deg) rotateY(0deg);
  }
  50% {
    transform: perspective(120px) rotateX(-180.1deg) rotateY(0deg);
  }
  100% {
    transform: perspective(120px) rotateX(-180deg) rotateY(-179.9deg);
  }
}
```

> Transform/motion animation

### `@keyframes tp-scaleout`

```css
@keyframes tp-scaleout {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes tp-bouncedelay`

```css
@keyframes tp-bouncedelay {
  0%, 80%, 100% {
    transform: scale(0);
  }
  40% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes tp-rotate`

```css
@keyframes tp-rotate {
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes tp-bounce`

```css
@keyframes tp-bounce {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-6`

```css
@keyframes rs-revealer-6 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-6`

```css
@keyframes rs-revealer-6 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-7`

```css
@keyframes rs-revealer-7 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-7`

```css
@keyframes rs-revealer-7 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-8`

```css
@keyframes rs-revealer-8 {
  0% {
    transform: scale(0, 0);
    opacity: 0.5;
  }
  100% {
    transform: scale(1, 1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rs-revealer-8`

```css
@keyframes rs-revealer-8 {
  0% {
    transform: scale(0, 0);
    opacity: 0.5;
  }
  100% {
    transform: scale(1, 1);
    opacity: 0;
  }
}
```

> Fade + motion enter animation

### `@keyframes rs-revealer-9`

```css
@keyframes rs-revealer-9 {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-9`

```css
@keyframes rs-revealer-9 {
  0%, 100% {
    transform: scale(0);
  }
  50% {
    transform: scale(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-10`

```css
@keyframes rs-revealer-10 {
  0%, 100%, 40% {
    transform: scaleY(0.4);
  }
  20% {
    transform: scaleY(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-10`

```css
@keyframes rs-revealer-10 {
  0%, 100%, 40% {
    transform: scaleY(0.4);
  }
  20% {
    transform: scaleY(1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-11`

```css
@keyframes rs-revealer-11 {
  0%, 100%, 70% {
    transform: scale3d(1, 1, 1);
  }
  35% {
    transform: scale3d(0, 0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-11`

```css
@keyframes rs-revealer-11 {
  0%, 100%, 70% {
    transform: scale3d(1, 1, 1);
  }
  35% {
    transform: scale3d(0, 0, 1);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-12`

```css
@keyframes rs-revealer-12 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-12`

```css
@keyframes rs-revealer-12 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-13`

```css
@keyframes rs-revealer-13 {
  0%, 100% {
    transform: translate(0px);
  }
  25% {
    transform: translate(160%);
  }
  50% {
    transform: translate(160%, 160%);
  }
  75% {
    transform: translate(0px, 160%);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-13`

```css
@keyframes rs-revealer-13 {
  0%, 100% {
    transform: translate(0px);
  }
  25% {
    transform: translate(160%);
  }
  50% {
    transform: translate(160%, 160%);
  }
  75% {
    transform: translate(0px, 160%);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-1`

```css
@keyframes rs-revealer-14-1 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-2`

```css
@keyframes rs-revealer-14-2 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-3`

```css
@keyframes rs-revealer-14-3 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-4`

```css
@keyframes rs-revealer-14-4 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-1`

```css
@keyframes rs-revealer-14-1 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-2`

```css
@keyframes rs-revealer-14-2 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-3`

```css
@keyframes rs-revealer-14-3 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, -80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, -80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-14-4`

```css
@keyframes rs-revealer-14-4 {
  0% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(0px, 0px, 0px);
  }
  20% {
    transform: rotate3d(0, 0, 1, 0deg) translate3d(-80%, 80%, 0px);
  }
  80% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(-80%, 80%, 0px);
  }
  100% {
    transform: rotate3d(0, 0, 1, 360deg) translate3d(0px, 0px, 0px);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-15`

```css
@keyframes rs-revealer-15 {
  25% {
    transform: translateX(30px) rotate(-90deg) scale(0.5);
  }
  50% {
    transform: translateX(30px) translateY(30px) rotate(-180deg);
  }
  75% {
    transform: translateX(0px) translateY(30px) rotate(-270deg) scale(0.5);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

### `@keyframes rs-revealer-15`

```css
@keyframes rs-revealer-15 {
  25% {
    transform: translateX(30px) rotate(-90deg) scale(0.5);
  }
  50% {
    transform: translateX(30px) translateY(30px) rotate(-179deg);
  }
  50.1% {
    transform: translateX(30px) translateY(30px) rotate(-180deg);
  }
  75% {
    transform: translateX(0px) translateY(30px) rotate(-270deg) scale(0.5);
  }
  100% {
    transform: rotate(-360deg);
  }
}
```

> Transform/motion animation

## Motion Tokens (CSS Variables)

### Duration Tokens

```css
--nfd-wb-anim-transition-duration: 1400ms;
```

### Delay Tokens

```css
--nfd-wb-anim-transition-delay: 50ms;
```

### Other Tokens

```css
--nfd-wb-anim-transition-easing-function: cubic-bezier(0.4,1,0.65,1);
--nfd-wb-anim-transition: all var(--nfd-wb-anim-transition-duration) var(--nfd-wb-anim-transition-easing-function) var(--nfd-wb-anim-transition-delay);
```

## Global Transition Declarations

These `transition` values were extracted from CSS rules across the site:

```css
transition: 0.3s;
transition: background 0.3s, color 0.3s;
transition: width 0.35s cubic-bezier(0.35, 0.7, 0.35, 1);
transition: transform 0.3s;
transition: transform 0.35s, opacity 0.35s;
transition: color 0.3s, opacity 0.3s, left 0.3s;
transition: background-color 0.2s linear;
transition: opacity 80ms, transform linear 81ms;
transition: background-color 0.3s ease-out;
transition: height 0.2s ease-out;
transition: transform 0.6s ease-in-out;
transition: var(--nfd-wb-anim-transition);
```

## How to Recreate This Motion Design

### Step 2 — Scroll-Reveal Pattern

Elements that animate into view follow this pattern:

```css
/* Initial hidden state */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 1400ms cubic-bezier(0.4, 0, 0.2, 1),
              transform 1400ms cubic-bezier(0.4, 0, 0.2, 1);
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### Step 3 — Key Motion Principles

- **Duration scale:** `1400ms` · `0.3s` · `0.35s` — use these values, never invent new durations
- **Always add** `@media (prefers-reduced-motion: reduce) { * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; } }`

### Step 4 — Scroll Journey Reference

Match what happens at each scroll position:

- **0%** (`0px`) → `screens/scroll/scroll-000.png`
- **17%** (`891px`) → `screens/scroll/scroll-017.png`
- **33%** (`1731px`) → `screens/scroll/scroll-033.png`
- **50%** (`2622px`) → `screens/scroll/scroll-050.png`
- **67%** (`3447px`) → `screens/scroll/scroll-067.png`
- **83%** (`3447px`) → `screens/scroll/scroll-083.png`
- **100%** (`3447px`) → `screens/scroll/scroll-100.png`


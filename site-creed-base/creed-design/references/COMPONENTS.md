# Component Reference

> Repeated DOM patterns detected by structural analysis. Each component appeared 3+ times.

## Detected Components

| Component | Category | Instances | Key Classes |
|-----------|----------|-----------|-------------|
| **Flex** | card | 33× | `.flex`, `.interactive`, `.items-center` |
| **Flex** | card | 19× | `.flex`, `.font-bold`, `.interactive` |
| **Cursor Pointer** | card | 7× | `.cursor-pointer`, `.flex`, `.items-center` |
| **Desktop Nav Text** | unknown | 7× | `.desktop-nav-text`, `.truncate` |
| **Cursor Pointer** | list-item | 6× | `.cursor-pointer`, `.flex`, `.flex-grow` |
| **Cursor Pointer** | unknown | 6× | `.cursor-pointer`, `.flex`, `.focus-within:outline-2` |
| **Absolute** | unknown | 6× | `.absolute`, `.cursor-default`, `.group/megamenu` |
| **Outline Offset 8** | unknown | 6× | `.-outline-offset-8`, `.group-focus-visible/megamenu:not-focus-visible:outline-2`, `.outline-radius-8` |
| **Flex** | unknown | 6× | `.flex`, `.max-w-[1304px]`, `.mx-auto` |
| **Flex 1** | unknown | 6× | `.flex-1`, `.min-w-0`, `.my-6` |
| **Absolute** | unknown | 6× | `.absolute`, `.bg-black`, `.bottom-[-100vh]` |
| **Overflow Hidden** | unknown | 6× | `.overflow-hidden` |
| **Gutter** | unknown | 4× | `.gutter` |
| **2xl:[  Carousel Item Width:Calc(25% (24px*3/4))]** | card | 4× | `.2xl:[--carousel-item-width:calc(25%-(24px*3/4))]`, `.[--carousel-item-width:100%]`, `.carousel-item` |
| **H Full** | card | 4× | `.h-full`, `.product-card` |
| **Flex** | unknown | 4× | `.flex`, `.flex-col`, `.h-full` |
| **Block** | unknown | 4× | `.block`, `.relative` |
| **Gap 4** | unknown | 3× | `.gap-4`, `.grid` |
| **Widgets** | unknown | 3× | `.widgets` |
| **Break Words** | card | 3× | `.break-words`, `.flex`, `.flex-col` |

## Cards

### Flex

**Instances found:** 33

**CSS classes:** `.flex` `.interactive` `.items-center` `.justify-between` `.navigation-mega-menu-text-item` `.px-2`

**HTML structure:**

```html
<a class="skin-navigation-text-item flex w-full items-center justify-between px-2 py-1 navigation-mega-menu-text-item interactive rounded-site" data-astro-prefetch="false" data-mega-menu-link="true" href="/p/absolu-aventus/16281794?variation=16281796">Absolu Aventus</a>
```

**Base styles (from design tokens):**

```css
.flex {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

### Flex

**Instances found:** 19

**CSS classes:** `.flex` `.font-bold` `.interactive` `.items-center` `.justify-between` `.mb-2`

**HTML structure:**

```html
<a class="skin-navigation-text-item flex w-full items-center justify-between px-2 mb-2 font-bold py-2 navigation-mega-menu-text-item-heading interactive rounded-site" data-astro-prefetch="false" data-mega-menu-link="true" href="/c/fragrances/mens/">All Men's Fragrances</a>
```

**Base styles (from design tokens):**

```css
.flex {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

### Cursor Pointer

**Instances found:** 7

**CSS classes:** `.cursor-pointer` `.flex` `.items-center` `.nav-link` `.py-1` `.relative`

**HTML structure:**

```html
<a id="nav-link-0" class="nav-link relative flex w-full cursor-pointer items-center py-1 focus:outline-none" target="_self" rel="" aria-label="New" data-nav-link="nav-link-0" data-astro-prefetch="hover" data-astro-cid-zafnspx5="true" href="/c/new/"> <span class="desktop-nav-text truncate" data-astro-cid-zafnspx5="">New</span> </a>
```

**Base styles (from design tokens):**

```css
.cursor-pointer {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

### 2xl:[  Carousel Item Width:Calc(25% (24px*3/4))]

**Instances found:** 4

**CSS classes:** `.2xl:[--carousel-item-width:calc(25%-(24px*3/4))]` `.[--carousel-item-width:100%]` `.carousel-item` `.duration-300` `.flex` `.flex-col`

**HTML structure:**

```html
<li class="carousel-item flex-none snap-start p-2 [--carousel-item-width:100%] sm:[--carousel-item-width:calc(50%-(24px*1/2))] lg:[--carousel-item-width:calc(1/3*100%-(24px*2/3))] 2xl:[--carousel-item-width:calc(25%-(24px*3/4))] flex min-h-full flex-col gap-4 overflow-visible transition-all duration-300 responsive-product-block-carousel-item"><div class="product-card h-full " data-testid="product-item"><div class="flex h-full w-full flex-col justify-start"><div class="product-item-image group relative flex aspect-square w-full flex-col "><a href="/p/aventus/12870029/" class="relative block" ar
```

**Base styles (from design tokens):**

```css
.2xl:[--carousel-item-width:calc(25%-(24px*3/4))] {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

### H Full

**Instances found:** 4

**CSS classes:** `.h-full` `.product-card`

**HTML structure:**

```html
<div class="product-card h-full " data-testid="product-item"><div class="flex h-full w-full flex-col justify-start"><div class="product-item-image group relative flex aspect-square w-full flex-col "><a href="/p/aventus/12870029/" class="relative block" aria-hidden="true" tabindex="-1"><div class="overflow-hidden"><picture><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=500&amp;height=500&amp;fit=cover&amp;v=2" media="(max-width: 640px)"><source srcset="/images?url=https://static.thcdn.com/productimg/
```

**Base styles (from design tokens):**

```css
.h-full {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

### Break Words

**Instances found:** 3

**CSS classes:** `.break-words` `.flex` `.flex-col` `.gap-3` `.items-center` `.mb-5`

**HTML structure:**

```html
<div class="text-center mb-5 md:mb-10 flex flex-col gap-3 items-center px-4 sm:px-6 md:px-0 break-words overflow-wrap-break-word simple-widgets-container" data-astro-cid-vkoinrso=""> <div class="simple-widgets-header" data-astro-cid-vkoinrso=""> </div> <div class="simple-text-widget-content simple-widgets-content break-words" data-astro-cid-vkoinrso=""> <h2><em>The House of Creed</em> is an authentic perfume house dedicated to the creation of highly original, artisan fragrances, made from the finest ingredients the world has to offer. <br></h2> <p></p> </div> </div>
```

**Base styles (from design tokens):**

```css
.break-words {
  background: #333333;
  border: 1px solid #4a5158;
  border-radius: 4px;
  padding: 8px;
}```

## List Items

### Cursor Pointer

**Instances found:** 6

**CSS classes:** `.cursor-pointer` `.flex` `.flex-grow` `.flex-shrink` `.focus-within:bg-[var(--color-background-hover)]` `.focus-within:text-[var(--color-foreground-hover)]`

**HTML structure:**

```html
<li id="nav-item-1" class="interactive group/heading static flex h-full min-w-0 flex-shrink flex-grow items-center focus-within:bg-[var(--color-background-hover)] focus-within:text-[var(--color-foreground-hover)] cursor-pointer" data-nav-item="nav-item-1" data-astro-cid-zafnspx5=""> <div id="nav-container-1" class="group/container nav-container relative flex h-12 w-full min-w-0 items-center py-2 focus-within:outline-2 focus-within:outline-offset-[-4px] cursor-pointer" data-nav-container="nav-container-1" data-astro-cid-zafnspx5=""> <a id="nav-link-1" class="nav-link relative flex w-full cursor
```

**Base styles (from design tokens):**

```css
.cursor-pointer {
  padding: 4px 0;
  border-bottom: 1px solid #4a5158;
}```

## Other Components

### Desktop Nav Text

**Instances found:** 7

**CSS classes:** `.desktop-nav-text` `.truncate`

**HTML structure:**

```html
<span class="desktop-nav-text truncate" data-astro-cid-zafnspx5="">New</span>
```

**Base styles (from design tokens):**

```css
.desktop-nav-text {
  background: #333333;
  padding: 4px;
}```

### Cursor Pointer

**Instances found:** 6

**CSS classes:** `.cursor-pointer` `.flex` `.focus-within:outline-2` `.focus-within:outline-offset-[-4px]` `.group/container` `.h-12`

**HTML structure:**

```html
<div id="nav-container-1" class="group/container nav-container relative flex h-12 w-full min-w-0 items-center py-2 focus-within:outline-2 focus-within:outline-offset-[-4px] cursor-pointer" data-nav-container="nav-container-1" data-astro-cid-zafnspx5=""> <a id="nav-link-1" class="nav-link relative flex w-full cursor-pointer items-center py-1 focus:outline-none" target="_self" rel="" aria-label="Fragrances" data-nav-link="nav-link-1" data-astro-prefetch="hover" data-astro-cid-zafnspx5="true" href="/c/all-fragrances/"> <span class="desktop-nav-text truncate" data-astro-cid-zafnspx5="">Fragrances<
```

**Base styles (from design tokens):**

```css
.cursor-pointer {
  background: #333333;
  padding: 4px;
}```

### Absolute

**Instances found:** 6

**CSS classes:** `.absolute` `.cursor-default` `.group/megamenu` `.left-0` `.max-w-[1356px]` `.mega-menu-container`

**HTML structure:**

```html
<div id="mega-menu-1-container" class="mega-menu-container group/megamenu pointer-events-auto absolute top-[100%] right-0 left-0 w-[100%] max-w-[1356px] origin-top cursor-default focus:outline-none" data-mega-menu-container="mega-menu-1-container" data-state="closed" tabindex="-1" data-mega-menu="mega-menu-1" data-parent-nav="nav-item-1" aria-label="Fragrances menu. Press the escape key to close the menu" data-astro-cid-zafnspx5=""> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-inner-container" class="w-full skin-mega-menu-light overflow-x-hidden px-6 rounded-b-site shadow-site group
```

**Base styles (from design tokens):**

```css
.absolute {
  background: #333333;
  padding: 4px;
}```

### Outline Offset 8

**Instances found:** 6

**CSS classes:** `.-outline-offset-8` `.group-focus-visible/megamenu:not-focus-visible:outline-2` `.outline-radius-8` `.overflow-x-hidden` `.px-6` `.rounded-b-site`

**HTML structure:**

```html
<div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-inner-container" class="w-full skin-mega-menu-light overflow-x-hidden px-6 rounded-b-site shadow-site group-focus-visible/megamenu:not-focus-visible:outline-2 -outline-offset-8 outline-radius-8" data-menu-type="TEXT"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-content" class="space-6 mx-auto flex max-w-[1304px]"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main" role="group" class="my-6 min-w-0 flex-1"> <ul> <div class="grid gap-4" style="grid-template-columns: repeat(6, minmax(0, 1fr))"> <li id="mega-menu-1a2fb2d
```

**Base styles (from design tokens):**

```css
.-outline-offset-8 {
  background: #333333;
  padding: 4px;
}```

### Flex

**Instances found:** 6

**CSS classes:** `.flex` `.max-w-[1304px]` `.mx-auto` `.space-6`

**HTML structure:**

```html
<div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-content" class="space-6 mx-auto flex max-w-[1304px]"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main" role="group" class="my-6 min-w-0 flex-1"> <ul> <div class="grid gap-4" style="grid-template-columns: repeat(6, minmax(0, 1fr))"> <li id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-item-0"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-section-0"> <div> <a class="skin-navigation-text-item flex w-full items-center justify-between px-2 mb-2 font-bold py-2 navigation-mega-menu-text-item-heading interactiv
```

**Base styles (from design tokens):**

```css
.flex {
  background: #333333;
  padding: 4px;
}```

### Flex 1

**Instances found:** 6

**CSS classes:** `.flex-1` `.min-w-0` `.my-6`

**HTML structure:**

```html
<div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main" role="group" class="my-6 min-w-0 flex-1"> <ul> <div class="grid gap-4" style="grid-template-columns: repeat(6, minmax(0, 1fr))"> <li id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-item-0"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-section-0"> <div> <a class="skin-navigation-text-item flex w-full items-center justify-between px-2 mb-2 font-bold py-2 navigation-mega-menu-text-item-heading interactive rounded-site" data-astro-prefetch="false" data-mega-menu-link="true" href="/c/fragrances/mens/">All Men's Fr
```

**Base styles (from design tokens):**

```css
.flex-1 {
  background: #333333;
  padding: 4px;
}```

### Absolute

**Instances found:** 6

**CSS classes:** `.absolute` `.bg-black` `.bottom-[-100vh]` `.left-[50%]` `.opacity-20` `.pointer-events-none`

**HTML structure:**

```html
<div class="pointer-events-none absolute top-0 bottom-[-100vh] left-[50%] z-[-1] w-[calc(var(--vw,1vw)*100)] translate-x-[-50%] bg-black opacity-20" data-astro-cid-zafnspx5=""></div>
```

**Base styles (from design tokens):**

```css
.absolute {
  background: #333333;
  padding: 4px;
}```

### Overflow Hidden

**Instances found:** 6

**CSS classes:** `.overflow-hidden`

**HTML structure:**

```html
<div class="overflow-hidden"><picture><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=500&amp;height=500&amp;fit=cover&amp;v=2" media="(max-width: 640px)"><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=450&amp;height=450&amp;fit=cover&amp;v=2" media="(max-width: 1024px)"><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;
```

**Base styles (from design tokens):**

```css
.overflow-hidden {
  background: #333333;
  padding: 4px;
}```

### Gutter

**Instances found:** 4

**CSS classes:** `.gutter`

**HTML structure:**

```html
<div class="gutter" data-astro-cid-vnpofkb5=""> <div class="container mx-auto flex items-center justify-end gap-6 py-1 text-sm" data-astro-cid-vnpofkb5=""> <div class="interactive mr-4" data-feature="hasSessionSettingsTrigger" data-astro-cid-vnpofkb5=""> <a class="flex h-auto cursor-pointer items-center justify-center" aria-label="Your settings, EUR currency selected" tab-index="0" data-astro-cid-vnpofkb5="true" href="/c/country-locator/"> <span class="session-settings-navigation-options-text" data-astro-cid-vnpofkb5=""> Country Locator </span> </a> </div> <a href="/store-locator" class="store
```

**Base styles (from design tokens):**

```css
.gutter {
  background: #333333;
  padding: 4px;
}```

### Flex

**Instances found:** 4

**CSS classes:** `.flex` `.flex-col` `.h-full` `.justify-start` `.w-full`

**HTML structure:**

```html
<div class="flex h-full w-full flex-col justify-start"><div class="product-item-image group relative flex aspect-square w-full flex-col "><a href="/p/aventus/12870029/" class="relative block" aria-hidden="true" tabindex="-1"><div class="overflow-hidden"><picture><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=500&amp;height=500&amp;fit=cover&amp;v=2" media="(max-width: 640px)"><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;au
```

**Base styles (from design tokens):**

```css
.flex {
  background: #333333;
  padding: 4px;
}```

### Block

**Instances found:** 4

**CSS classes:** `.block` `.relative`

**HTML structure:**

```html
<a href="/p/aventus/12870029/" class="relative block" aria-hidden="true" tabindex="-1"><div class="overflow-hidden"><picture><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=500&amp;height=500&amp;fit=cover&amp;v=2" media="(max-width: 640px)"><source srcset="/images?url=https://static.thcdn.com/productimg/original/12870029-1145337306138828.jpg&amp;format=webp&amp;auto=avif&amp;width=450&amp;height=450&amp;fit=cover&amp;v=2" media="(max-width: 1024px)"><source srcset="/images?url=https://static.thcdn.c
```

**Base styles (from design tokens):**

```css
.block {
  background: #333333;
  padding: 4px;
}```

### Gap 4

**Instances found:** 3

**CSS classes:** `.gap-4` `.grid`

**HTML structure:**

```html
<div class="grid gap-4" style="grid-template-columns: repeat(6, minmax(0, 1fr))"> <li id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-item-0"> <div id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-section-0"> <div> <a class="skin-navigation-text-item flex w-full items-center justify-between px-2 mb-2 font-bold py-2 navigation-mega-menu-text-item-heading interactive rounded-site" data-astro-prefetch="false" data-mega-menu-link="true" href="/c/fragrances/mens/">All Men's Fragrances</a> </div> <ul> <li id="mega-menu-1a2fb2d9-487d-4a14-8194-c45b27b0c7b8-main-item-0-child-0"> <div> <
```

**Base styles (from design tokens):**

```css
.gap-4 {
  background: #333333;
  padding: 4px;
}```

### Widgets

**Instances found:** 3

**CSS classes:** `.widgets`

**HTML structure:**

```html
<section class="widgets " data-id="4591095" data-widget="simpletextwidgetwithh1" data-track-type="click" data-track="widgetClick" data-component="simpletextwidgetwithh1" data-description="Homepage Slot 2 Text" style="contain: layout style;"><div data-track="widgetTrack" data-track-type="impression" data-component="simpletextwidgetwithh1"></div><div class="text-center mb-5 md:mb-10 flex flex-col gap-3 items-center px-4 sm:px-6 md:px-0 break-words overflow-wrap-break-word simple-widgets-container" data-astro-cid-vkoinrso=""> <div class="simple-widgets-header" data-astro-cid-vkoinrso=""> </div> <
```

**Base styles (from design tokens):**

```css
.widgets {
  background: #333333;
  padding: 4px;
}```

## Component Rules

- Match class names exactly from the patterns above
- Each component instance must be visually identical to others of its type
- Do not add extra wrappers or change the DOM structure
- Use `#4a5158` for all dividers within components
- Use `#3275b4` for all interactive/active states


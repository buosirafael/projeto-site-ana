# Layout Reference

> Auto-extracted from live DOM. Use this to understand how the site is structured spatially.

## Spacing System

**Base grid:** 4px

**Scale:** `2, 4, 6, 8, 10, 12, 14, 16, 20, 24, 26, 28, 30, 32, 36` px

| Spacing | Semantic Use |
|---------|-------------|
| 4px | Tight — within a component |
| 8px | Medium — between sibling items |
| 16px | Wide — between sections |
| 32px | Vast — major section breaks |

## Flex Layouts

| Element | Direction | Justify | Align | Gap | Children |
|---------|-----------|---------|-------|-----|----------|
| `body.skin.flex` | column | — | — | — | 15 |
| `footer#site-footer.skin-footer.skin-footer-wrapper` | column | — | — | — | 4 |
| `div.container.mx-auto` | row | — | center | 48px | 2 |
| `div.skin-footer.link-sections` | row | — | start | — | 3 |
| `div.skin-footer.skin-footer-payment-icons` | column | — | — | 32px | 2 |
| `div.header-order.relative` | row | space-between | center | — | 4 |
| `div.responsiveUsp_slider.scrollbar-hide` | row | center | center | 24px | 2 |
| `div.email-signup.flex` | row | — | — | 16px | 2 |
| `div.footer-logo.flex` | column | — | start | — | 2 |
| `div.flex.flex-col-reverse` | row | space-between | — | 32px | 2 |
| `div.header-logo.hidden` | row | center | center | — | 1 |
| `div.header-search.flex` | row | start | center | 32px | 3 |
| `ul.navigation-items-list.flex` | row | center | center | — | 7 |
| `a.responsiveUsp_link.usp-item` | row | center | center | 12px | 2 |
| `div.payment-options.flex` | row | — | center | 32px | 1 |

## Grid Layouts

| Element | Template Columns | Gap | Children |
|---------|-----------------|-----|----------|
| `div.desktop-footer-wrapper.hidden` | `275px 275px 275px 275px` | — | 4 |

## Structural Containers

### `<main>` (`main#main-content.flex-grow`)

```
display:          block
padding:          173px 0px 0px
children:         3
```

### `<footer>` (`footer#site-footer.skin-footer.skin-footer-wrapper`)

```
display:          flex
flex-direction:   column
justify-content:  —
align-items:      —
padding:          16px 0px 0px
children:         4
```

### `<header>` (`header#site-header.skin-header`)

```
display:          block
children:         1
```

### `<section>` (`section.skip-link.text-center`)

```
display:          block
padding:          16px
children:         1
```

### `<nav>` (`nav#main-nav.skin-navigation.text-body`)

```
display:          block
children:         1
```

### `<section>` (`section.widgets.mb-10`)

```
display:          block
children:         3
```

### `<section>` (`section.widgets`)

```
display:          block
children:         3
```

### `<section>` (`section.widgets`)

```
display:          block
children:         3
```

### `<section>` (`section.widgets.mb-10`)

```
display:          block
children:         5
```

### `<section>` (`section.widgets.mb-10`)

```
display:          block
children:         2
```

### `<section>` (`section.widgets.mb-10`)

```
display:          block
children:         2
```

### `<section>` (`section.widgets`)

```
display:          block
children:         3
```

## Layout Rules

- **Container max-width:** `1400px` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Secondary layout system: **CSS Grid** (used for card grids and multi-column layouts)
- Every spacing value must be a multiple of **4px**
- Never use arbitrary margin/padding values outside the spacing scale


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
| `nav.navbar.navbar-expand-lg` | row | start | center | — | 1 |
| `div.container` | row | space-between | center | — | 3 |
| `div.row.g-4` | row | — | — | — | 4 |
| `div.row.text-center` | row | — | — | — | 1 |
| `div.row` | row | — | — | — | 4 |
| `div.row.align-items-center` | row | — | center | — | 2 |
| `div.row.justify-content-center` | row | center | — | — | 1 |
| `div.row.mt-5` | row | center | — | — | 5 |
| `div.row.mt-4` | row | — | — | — | 3 |
| `div.row` | row | — | — | — | 3 |
| `div#navbarNav.collapse.navbar-collapse` | row | — | center | — | 1 |

## Structural Containers

### `<header>` (`header.navbar-section.fixed-top`)

```
display:          block
children:         1
```

### `<main>` 

```
display:          block
children:         6
```

### `<footer>` (`footer.footer-section.py-5`)

```
display:          block
padding:          48px 0px
children:         1
```

### `<nav>` (`nav.navbar.navbar-expand-lg`)

```
display:          flex
flex-direction:   row
justify-content:  start
align-items:      center
padding:          24px 0px
children:         1
```

### `<section>` (`section.agriculture-section.py-5`)

```
display:          block
padding:          80px 0px
children:         1
```

### `<section>` (`section.development-section.py-5`)

```
display:          block
padding:          80px 0px
children:         1
```

### `<section>` (`section.product-lines-section.py-5`)

```
display:          block
padding:          80px 0px
children:         1
```

### `<section>` (`section.news-blogs-section.py-5`)

```
display:          block
padding:          48px 0px
children:         1
```

## Layout Rules

- **Container max-width:** `1320px` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Every spacing value must be a multiple of **4px**
- Never use arbitrary margin/padding values outside the spacing scale


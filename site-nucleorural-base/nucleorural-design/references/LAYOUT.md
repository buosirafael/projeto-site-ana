# Layout Reference

> Auto-extracted from live DOM. Use this to understand how the site is structured spatially.

## Spacing System

**Base grid:** 5px

**Scale:** `5, 10, 15, 20, 25, 30, 35, 40, 50, 60, 70, 80, 85, 95, 100` px

| Spacing | Semantic Use |
|---------|-------------|
| 5px | Tight — within a component |
| 10px | Medium — between sibling items |
| 20px | Wide — between sections |
| 40px | Vast — major section breaks |

## Flex Layouts

| Element | Direction | Justify | Align | Gap | Children |
|---------|-----------|---------|-------|-----|----------|
| `div.row-inner.clearfix` | row | — | end | — | 1 |
| `div.vc_column-inner` | row | — | end | — | 1 |

## Structural Containers

### `<footer>` (`footer#footer`)

```
display:          block
padding:          114px 0px 50px
children:         1
```

### `<header>` (`header#site-header`)

```
display:          block
children:         1
```

### `<article>` (`article.page-content.post-13588`)

```
display:          block
children:         1
```

### `<nav>` (`nav#main-nav.main-nav`)

```
display:          block
children:         1
```

### `<section>` (`section#sobrenos.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section#solucoes.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

### `<section>` (`section.wpb_row.vc_row-fluid`)

```
display:          block
children:         1
```

## Layout Rules

- **Container max-width:** `90%` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Every spacing value must be a multiple of **5px**
- Never use arbitrary margin/padding values outside the spacing scale


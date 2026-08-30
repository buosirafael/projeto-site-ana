# Layout Reference

> Auto-extracted from live DOM. Use this to understand how the site is structured spatially.

## Spacing System

**Base grid:** 4px

**Scale:** `2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30` px

| Spacing | Semantic Use |
|---------|-------------|
| 4px | Tight — within a component |
| 8px | Medium — between sibling items |
| 16px | Wide — between sections |
| 32px | Vast — major section breaks |

## Flex Layouts

| Element | Direction | Justify | Align | Gap | Children |
|---------|-----------|---------|-------|-----|----------|
| `nav#nav.nav` | row | space-between | center | — | 3 |
| `section#hero.hero.mode-of` | column | center | — | — | 4 |
| `div.lf-head-row` | row | — | center | 14px | 2 |
| `div.of-card.reveal` | column | — | — | — | 2 |
| `div.of-card.reveal` | column | — | — | — | 2 |
| `div.of-card.reveal` | column | — | — | — | 2 |
| `a.cm-card.reveal` | column | — | — | — | 2 |
| `a.cm-card.reveal` | column | — | — | — | 2 |
| `a.cm-card.reveal` | column | — | — | — | 2 |
| `a.cm-card.reveal` | column | — | — | — | 2 |
| `a.cm-card.reveal` | column | — | — | — | 2 |
| `div.card-bottom` | column | — | — | 18px | 2 |
| `div.card-bottom` | column | — | — | 18px | 2 |

## Grid Layouts

| Element | Template Columns | Gap | Children |
|---------|-----------------|-----|----------|
| `div.hero-inner` | `617.391px 558.594px` | 64px | 2 |
| `div.bridge-grid` | `608px 608px` | 24px | 2 |
| `div.of-grid` | `398.656px 398.672px 398.656px` | 22px | 3 |
| `div.cm-grid` | `233.594px 233.594px 233.609px 233.594px 233.609px` | 18px | 5 |
| `div.hero-visual` | `540px` | — | 6 |
| `a.bridge-card.onfarm` | `536px` | 24px | 3 |
| `a.bridge-card.com` | `534px` | 24px | 3 |
| `div.card-figure` | `534px` | — | 1 |
| `div.card-figure` | `532px` | — | 1 |
| `div.of-card-img` | `396.656px` | — | 1 |

## Structural Containers

### `<nav>` (`nav#nav.nav`)

```
display:          flex
flex-direction:   row
justify-content:  space-between
align-items:      center
padding:          18px 72px
children:         3
```

### `<footer>` (`footer.footer`)

```
display:          block
padding:          72px 72px 28px
children:         3
```

### `<section>` (`section#hero.hero.mode-of`)

```
display:          flex
flex-direction:   column
justify-content:  center
align-items:      —
padding:          80px 72px 60px
children:         4
```

### `<section>` (`section#on-farm-talk.oftalk`)

```
display:          block
padding:          110px 72px
children:         1
```

### `<section>` (`section#bridge.bridge`)

```
display:          block
padding:          110px 72px
children:         1
```

### `<section>` (`section#on-farm.section.light`)

```
display:          block
padding:          129.6px 72px
children:         1
```

### `<section>` (`section#comerciais.section.tint`)

```
display:          block
padding:          129.6px 72px
children:         1
```

### `<section>` (`section.section-cta`)

```
display:          block
padding:          100px 72px
children:         1
```

### `<nav>` (`nav.ft-col`)

```
display:          block
children:         5
```

### `<nav>` (`nav.ft-col`)

```
display:          block
children:         6
```

### `<nav>` (`nav.ft-col`)

```
display:          block
children:         6
```

## Layout Rules

- **Container max-width:** `1240px` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Secondary layout system: **CSS Grid** (used for card grids and multi-column layouts)
- Every spacing value must be a multiple of **4px**
- Never use arbitrary margin/padding values outside the spacing scale


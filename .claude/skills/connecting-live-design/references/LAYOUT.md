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
| `nav.site-nav` | row | space-between | center | 24px | 3 |
| `div.hero-search` | row | — | center | 10px | 2 |

## Grid Layouts

| Element | Template Columns | Gap | Children |
|---------|-----------------|-----|----------|
| `section#top.hero-grid` | `625.797px 566.203px` | 48px | 2 |
| `div.benefits-grid` | `293.5px 293.5px 293.5px 293.5px` | 22px | 4 |
| `div.plans-grid` | `397.328px 397.328px 397.344px` | 24px | 3 |
| `div.ahorro-grid` | `592px 592px` | 56px | 2 |
| `div.footer-grid` | `274px 195.703px 195.719px 195.719px 234.844px` | 36px | 5 |
| `div.hero-visual` | `566.203px` | — | 4 |
| `div.steps-grid` | `348px 348px 348px` | 28px | 4 |

## Structural Containers

### `<header>` 

```
display:          block
children:         1
```

### `<footer>` 

```
display:          block
padding:          0px 0px 100px
children:         2
```

### `<section>` (`section#top.hero-grid`)

```
display:          grid
grid-template-columns: 625.797px 566.203px
gap:              48px
padding:          78px 28px 40px
max-width:        1240px
children:         2
```

### `<section>` (`section#proveedores`)

```
display:          block
padding:          22px 28px 70px
max-width:        1240px
children:         1
```

### `<section>` (`section#beneficios`)

```
display:          block
padding:          20px 28px 90px
max-width:        1240px
children:         2
```

### `<section>` (`section#planes`)

```
display:          block
padding:          0px 28px 96px
max-width:        1240px
children:         3
```

### `<section>` (`section#pasos`)

```
display:          block
padding:          90px 0px
children:         1
```

### `<section>` (`section#ahorro`)

```
display:          block
padding:          90px 28px
max-width:        1240px
children:         3
```

### `<section>` 

```
display:          block
padding:          0px 28px 90px
max-width:        1240px
children:         1
```

### `<nav>` (`nav.site-nav`)

```
display:          flex
flex-direction:   row
justify-content:  space-between
align-items:      center
gap:              24px
padding:          16px 28px
max-width:        1240px
children:         3
```

## Layout Rules

- **Container max-width:** `1240px` — always center with `margin: auto`
- Primary layout system: **Flexbox**
- Secondary layout system: **CSS Grid** (used for card grids and multi-column layouts)
- Every spacing value must be a multiple of **4px**
- Never use arbitrary margin/padding values outside the spacing scale


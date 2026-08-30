# Component Reference

> Repeated DOM patterns detected by structural analysis. Each component appeared 3+ times.

## Detected Components

| Component | Category | Instances | Key Classes |
|-----------|----------|-----------|-------------|
| **Cm Card** | card | 5× | `.cm-card`, `.reveal` |
| **Cm Card Img** | card | 5× | `.cm-card-img` |
| **Cm Card Type** | card | 5× | `.cm-card-type` |
| **Cm Card Body** | card | 5× | `.cm-card-body` |
| **Stat** | unknown | 4× | `.stat` |
| **Tag** | badge | 4× | `.tag`, `.tag-vr` |
| **Btn** | button | 3× | `.btn`, `.btn-primary` |
| **Fl Orbit** | unknown | 3× | `.fl-orbit` |
| **Stat Num** | unknown | 3× | `.stat-num` |
| **Tx Vr** | unknown | 3× | `.tx-vr` |
| **Of Card Img** | card | 3× | `.of-card-img` |
| **Of Card Body** | card | 3× | `.of-card-body` |
| **Ft Col** | unknown | 3× | `.ft-col` |

## Cards

### Cm Card

**Instances found:** 5

**CSS classes:** `.cm-card` `.reveal`

**HTML structure:**

```html
<a class="cm-card reveal" href="comerciais.html#rethax" aria-label="Rethax — ver detalhes nos produtos comerciais"> <div class="cm-card-img"> <span class="cm-card-type">Fungicida</span> <img src="assets/produtos/rethax.png" alt="Rethax"> </div> <div class="cm-card-body"> <h3>Rethax</h3><p>Trichoderma harzianum + T. viride</p> </div> </a>
```

**Base styles (from design tokens):**

```css
.cm-card {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

### Cm Card Img

**Instances found:** 5

**CSS classes:** `.cm-card-img`

**HTML structure:**

```html
<div class="cm-card-img"> <span class="cm-card-type">Fungicida</span> <img src="assets/produtos/rethax.png" alt="Rethax"> </div>
```

**Base styles (from design tokens):**

```css
.cm-card-img {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

### Cm Card Type

**Instances found:** 5

**CSS classes:** `.cm-card-type`

**HTML structure:**

```html
<span class="cm-card-type">Fungicida</span>
```

**Base styles (from design tokens):**

```css
.cm-card-type {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

### Cm Card Body

**Instances found:** 5

**CSS classes:** `.cm-card-body`

**HTML structure:**

```html
<div class="cm-card-body"> <h3>Rethax</h3><p>Trichoderma harzianum + T. viride</p> </div>
```

**Base styles (from design tokens):**

```css
.cm-card-body {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

### Of Card Img

**Instances found:** 3

**CSS classes:** `.of-card-img`

**HTML structure:**

```html
<div class="of-card-img"><img src="assets/equipamentos/hbfas.png" alt="HBFAS"></div>
```

**Base styles (from design tokens):**

```css
.of-card-img {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

### Of Card Body

**Instances found:** 3

**CSS classes:** `.of-card-body`

**HTML structure:**

```html
<div class="of-card-body"> <div class="tag tag-vr">Biofábrica</div> <h3>HBFAS Gold &amp; Silver</h3> <p>Unidade de Produção de Bioinsumos para u…</p> </div>
```

**Base styles (from design tokens):**

```css
.of-card-body {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 8px;
}```

## Buttons

### Btn

**Instances found:** 3

**CSS classes:** `.btn` `.btn-primary`

**HTML structure:**

```html
<a href="on-farm.html" class="btn btn-primary">Conhecer a plataforma <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14M12 5l7 7-7 7"></path></svg> </a>
```

**Base styles (from design tokens):**

```css
.btn {
  color: #ffffff;
  border-radius: 14px;
  padding: 4px 8px;
  cursor: pointer;
}```

## Badges & Chips

### Tag

**Instances found:** 4

**CSS classes:** `.tag` `.tag-vr`

**HTML structure:**

```html
<div class="tag tag-vr">Soluções Comerciais</div>
```

**Base styles (from design tokens):**

```css
.tag {
  background: #164133;
  border: 1px solid #2a3a30;
  border-radius: 14px;
  padding: 2px 4px;
  font-size: 12px;
}```

## Other Components

### Stat

**Instances found:** 4

**CSS classes:** `.stat`

**HTML structure:**

```html
<div class="stat" data-of=""> <div class="stat-num"><span data-t="27">27</span><span class="sx">+</span></div> <div class="stat-label">CEPAS ENTRE FUNGOS E BACTÉRIAS</div> </div>
```

**Base styles (from design tokens):**

```css
.stat {
  background: #164133;
  padding: 4px;
}```

### Fl Orbit

**Instances found:** 3

**CSS classes:** `.fl-orbit`

**HTML structure:**

```html
<div class="fl-orbit" style="--angle:0deg; --delay:0s"><div class="floating-label fl-1"><span class="dot"></span><span class="of-only">Método FAS · Fermentação Assistida</span><span class="cm-only" hidden="">Pronto para uso</span></div></div>
```

**Base styles (from design tokens):**

```css
.fl-orbit {
  background: #164133;
  padding: 4px;
}```

### Stat Num

**Instances found:** 3

**CSS classes:** `.stat-num`

**HTML structure:**

```html
<div class="stat-num sm">Método FAS</div>
```

**Base styles (from design tokens):**

```css
.stat-num {
  background: #164133;
  padding: 4px;
}```

### Tx Vr

**Instances found:** 3

**CSS classes:** `.tx-vr`

**HTML structure:**

```html
<span class="tx-vr">você escolhe.</span>
```

**Base styles (from design tokens):**

```css
.tx-vr {
  background: #164133;
  padding: 4px;
}```

### Ft Col

**Instances found:** 3

**CSS classes:** `.ft-col`

**HTML structure:**

```html
<nav class="ft-col" aria-label="Soluções On Farm"> <h4>On Farm</h4> <a href="on-farm.html#maquinarios">HBFAS Gold e Silver</a> <a href="on-farm.html#biobag">BioBag</a> <a href="on-farm.html#hbmax">Linha HBMax</a> <a href="on-farm.html#calculadora">Calculadora</a> </nav>
```

**Base styles (from design tokens):**

```css
.ft-col {
  background: #164133;
  padding: 4px;
}```

## Component Rules

- Match class names exactly from the patterns above
- Each component instance must be visually identical to others of its type
- Do not add extra wrappers or change the DOM structure
- Use `#2a3a30` for all dividers within components


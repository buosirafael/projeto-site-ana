# Component Reference

> Repeated DOM patterns detected by structural analysis. Each component appeared 3+ times.

## Detected Components

| Component | Category | Instances | Key Classes |
|-----------|----------|-----------|-------------|
| **Nav Item** | card | 8× | `.nav-item` |
| **Nav Link** | unknown | 8× | `.nav-link` |
| **Col 6** | unknown | 5× | `.col-6`, `.col-md`, `.custom-col-5` |
| **Product Card** | card | 5× | `.product-card` |
| **Image Wrapper** | unknown | 5× | `.image-wrapper` |
| **Product Image** | card | 5× | `.product-image` |
| **Product Title Overlay** | card | 5× | `.product-title-overlay` |
| **Col Md 3** | unknown | 4× | `.col-md-3` |
| **Text Decoration None** | unknown | 4× | `.text-decoration-none` |
| **Card Custom** | card | 4× | `.card-custom` |
| **Card Img** | card | 4× | `.card-img` |
| **Icon Top** | unknown | 4× | `.icon-top` |
| **Text Overlay** | unknown | 4× | `.text-overlay` |
| **Fw Bold** | unknown | 4× | `.fw-bold` |
| **Icon Bottom** | unknown | 4× | `.icon-bottom` |
| **Col 12** | unknown | 3× | `.col-12`, `.col-md-4`, `.mb-4` |
| **Blog Card** | card | 3× | `.blog-card`, `.border`, `.h-100` |
| **D Block** | unknown | 3× | `.d-block`, `.h-100`, `.text-dark` |
| **Blog Image** | unknown | 3× | `.blog-image`, `.img-fluid`, `.w-100` |
| **Blog Body** | unknown | 3× | `.blog-body` |

## Cards

### Nav Item

**Instances found:** 8

**CSS classes:** `.nav-item`

**HTML structure:**

```html
<li class="nav-item"><a class="nav-link" href="./">HOME</a></li>
```

**Base styles (from design tokens):**

```css
.nav-item {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Product Card

**Instances found:** 5

**CSS classes:** `.product-card`

**HTML structure:**

```html
<a href="linha/titanium-foliar" class="product-card"> <div class="image-wrapper"> <img src="assets/img/linhas-de-produtos-titaniun-folicular-solo-rico.jpg" alt="Produto 1" class="product-image"> <div class="product-title-overlay">TITANIUM FOLIAR</div> </div> </a>
```

**Base styles (from design tokens):**

```css
.product-card {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Product Image

**Instances found:** 5

**CSS classes:** `.product-image`

**HTML structure:**

```html
<img src="assets/img/linhas-de-produtos-titaniun-folicular-solo-rico.jpg" alt="Produto 1" class="product-image">
```

**Base styles (from design tokens):**

```css
.product-image {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Product Title Overlay

**Instances found:** 5

**CSS classes:** `.product-title-overlay`

**HTML structure:**

```html
<div class="product-title-overlay">TITANIUM FOLIAR</div>
```

**Base styles (from design tokens):**

```css
.product-title-overlay {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Card Custom

**Instances found:** 4

**CSS classes:** `.card-custom`

**HTML structure:**

```html
<div class="card-custom"> <img src="assets/img/top-lime-pro-solo-rico.jpg" class="card-img" alt="Maçãs"> <div class="icon-top"><img src="assets/img/icones/icone1-solorico.png" width="60" alt="Ícone"></div> <div class="text-overlay"> <h5 class="fw-bold">TOP LIME PRO</h5> </div> <div class="icon-bottom">LINHA DE ADJUVANTES</div> </div>
```

**Base styles (from design tokens):**

```css
.card-custom {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Card Img

**Instances found:** 4

**CSS classes:** `.card-img`

**HTML structure:**

```html
<img src="assets/img/top-lime-pro-solo-rico.jpg" class="card-img" alt="Maçãs">
```

**Base styles (from design tokens):**

```css
.card-img {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

### Blog Card

**Instances found:** 3

**CSS classes:** `.blog-card` `.border` `.h-100` `.rounded`

**HTML structure:**

```html
<div class="blog-card border rounded h-100"> <a href="blog/agricultura-regenerativa-como-cuidar-do-solo-e-aumentar-a-produtividade?lang=pt-br" class="text-decoration-none text-dark d-block h-100"> <img src="assets/img/blog/post-2026-08-18-16-56-17-6a84b8e1d947d.jpeg" alt="Agricultura Regenerativa: Como Cuidar do Solo e Aumentar a Produtividade" class="img-fluid w-100 blog-image"> <div class="blog-body"> <span class="blog-badge">Sustentabilidade</span> <h5 class="blog-title">Agricultura Regenerativa: Como Cuidar do…</h5> <p class="blog-description">Entenda o que é agricultura regenerativa…</p> 
```

**Base styles (from design tokens):**

```css
.blog-card {
  background: #333333;
  border: 1px solid #555555;
  border-radius: 5px;
  padding: 8px;
}```

## Other Components

### Nav Link

**Instances found:** 8

**CSS classes:** `.nav-link`

**HTML structure:**

```html
<a class="nav-link" href="./">HOME</a>
```

**Base styles (from design tokens):**

```css
.nav-link {
  background: #333333;
  padding: 4px;
}```

### Col 6

**Instances found:** 5

**CSS classes:** `.col-6` `.col-md` `.custom-col-5`

**HTML structure:**

```html
<div class="col-6 col-md custom-col-5"> <a href="linha/titanium-foliar" class="product-card"> <div class="image-wrapper"> <img src="assets/img/linhas-de-produtos-titaniun-folicular-solo-rico.jpg" alt="Produto 1" class="product-image"> <div class="product-title-overlay">TITANIUM FOLIAR</div> </div> </a> </div>
```

**Base styles (from design tokens):**

```css
.col-6 {
  background: #333333;
  padding: 4px;
}```

### Image Wrapper

**Instances found:** 5

**CSS classes:** `.image-wrapper`

**HTML structure:**

```html
<div class="image-wrapper"> <img src="assets/img/linhas-de-produtos-titaniun-folicular-solo-rico.jpg" alt="Produto 1" class="product-image"> <div class="product-title-overlay">TITANIUM FOLIAR</div> </div>
```

**Base styles (from design tokens):**

```css
.image-wrapper {
  background: #333333;
  padding: 4px;
}```

### Col Md 3

**Instances found:** 4

**CSS classes:** `.col-md-3`

**HTML structure:**

```html
<div class="col-md-3"> <a href="produto/top-lime-pro" class="text-decoration-none"> <div class="card-custom"> <img src="assets/img/top-lime-pro-solo-rico.jpg" class="card-img" alt="Maçãs"> <div class="icon-top"><img src="assets/img/icones/icone1-solorico.png" width="60" alt="Ícone"></div> <div class="text-overlay"> <h5 class="fw-bold">TOP LIME PRO</h5> </div> <div class="icon-bottom">LINHA DE ADJUVANTES</div> </div> </a> </div>
```

**Base styles (from design tokens):**

```css
.col-md-3 {
  background: #333333;
  padding: 4px;
}```

### Text Decoration None

**Instances found:** 4

**CSS classes:** `.text-decoration-none`

**HTML structure:**

```html
<a href="produto/top-lime-pro" class="text-decoration-none"> <div class="card-custom"> <img src="assets/img/top-lime-pro-solo-rico.jpg" class="card-img" alt="Maçãs"> <div class="icon-top"><img src="assets/img/icones/icone1-solorico.png" width="60" alt="Ícone"></div> <div class="text-overlay"> <h5 class="fw-bold">TOP LIME PRO</h5> </div> <div class="icon-bottom">LINHA DE ADJUVANTES</div> </div> </a>
```

**Base styles (from design tokens):**

```css
.text-decoration-none {
  background: #333333;
  padding: 4px;
}```

### Icon Top

**Instances found:** 4

**CSS classes:** `.icon-top`

**HTML structure:**

```html
<div class="icon-top"><img src="assets/img/icones/icone1-solorico.png" width="60" alt="Ícone"></div>
```

**Base styles (from design tokens):**

```css
.icon-top {
  background: #333333;
  padding: 4px;
}```

### Text Overlay

**Instances found:** 4

**CSS classes:** `.text-overlay`

**HTML structure:**

```html
<div class="text-overlay"> <h5 class="fw-bold">TOP LIME PRO</h5> </div>
```

**Base styles (from design tokens):**

```css
.text-overlay {
  background: #333333;
  padding: 4px;
}```

### Fw Bold

**Instances found:** 4

**CSS classes:** `.fw-bold`

**HTML structure:**

```html
<h5 class="fw-bold">TOP LIME PRO</h5>
```

**Base styles (from design tokens):**

```css
.fw-bold {
  background: #333333;
  padding: 4px;
}```

### Icon Bottom

**Instances found:** 4

**CSS classes:** `.icon-bottom`

**HTML structure:**

```html
<div class="icon-bottom">LINHA DE ADJUVANTES</div>
```

**Base styles (from design tokens):**

```css
.icon-bottom {
  background: #333333;
  padding: 4px;
}```

### Col 12

**Instances found:** 3

**CSS classes:** `.col-12` `.col-md-4` `.mb-4`

**HTML structure:**

```html
<div class="col-12 col-md-4 mb-4"> <div class="blog-card border rounded h-100"> <a href="blog/agricultura-regenerativa-como-cuidar-do-solo-e-aumentar-a-produtividade?lang=pt-br" class="text-decoration-none text-dark d-block h-100"> <img src="assets/img/blog/post-2026-08-18-16-56-17-6a84b8e1d947d.jpeg" alt="Agricultura Regenerativa: Como Cuidar do Solo e Aumentar a Produtividade" class="img-fluid w-100 blog-image"> <div class="blog-body"> <span class="blog-badge">Sustentabilidade</span> <h5 class="blog-title">Agricultura Regenerativa: Como Cuidar do…</h5> <p class="blog-description">Entenda o q
```

**Base styles (from design tokens):**

```css
.col-12 {
  background: #333333;
  padding: 4px;
}```

### D Block

**Instances found:** 3

**CSS classes:** `.d-block` `.h-100` `.text-dark` `.text-decoration-none`

**HTML structure:**

```html
<a href="blog/agricultura-regenerativa-como-cuidar-do-solo-e-aumentar-a-produtividade?lang=pt-br" class="text-decoration-none text-dark d-block h-100"> <img src="assets/img/blog/post-2026-08-18-16-56-17-6a84b8e1d947d.jpeg" alt="Agricultura Regenerativa: Como Cuidar do Solo e Aumentar a Produtividade" class="img-fluid w-100 blog-image"> <div class="blog-body"> <span class="blog-badge">Sustentabilidade</span> <h5 class="blog-title">Agricultura Regenerativa: Como Cuidar do…</h5> <p class="blog-description">Entenda o que é agricultura regenerativa…</p> <small class="text-muted">18 Aug 2026</small>
```

**Base styles (from design tokens):**

```css
.d-block {
  background: #333333;
  padding: 4px;
}```

### Blog Image

**Instances found:** 3

**CSS classes:** `.blog-image` `.img-fluid` `.w-100`

**HTML structure:**

```html
<img src="assets/img/blog/post-2026-08-18-16-56-17-6a84b8e1d947d.jpeg" alt="Agricultura Regenerativa: Como Cuidar do Solo e Aumentar a Produtividade" class="img-fluid w-100 blog-image">
```

**Base styles (from design tokens):**

```css
.blog-image {
  background: #333333;
  padding: 4px;
}```

### Blog Body

**Instances found:** 3

**CSS classes:** `.blog-body`

**HTML structure:**

```html
<div class="blog-body"> <span class="blog-badge">Sustentabilidade</span> <h5 class="blog-title">Agricultura Regenerativa: Como Cuidar do…</h5> <p class="blog-description">Entenda o que é agricultura regenerativa…</p> <small class="text-muted">18 Aug 2026</small> </div>
```

**Base styles (from design tokens):**

```css
.blog-body {
  background: #333333;
  padding: 4px;
}```

## Component Rules

- Match class names exactly from the patterns above
- Each component instance must be visually identical to others of its type
- Do not add extra wrappers or change the DOM structure
- Use `#555555` for all dividers within components


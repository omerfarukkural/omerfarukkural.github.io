---
name: frontend-patterns
description: Jekyll + GitHub Pages portfolyo geliştirme iş akışı. HTML/CSS bileşenleri, Jekyll layout ve include yapısı, responsive tasarım kalıpları.
---

# Frontend Patterns – Portfolyo

## Jekyll Layout Yapısı

```
_layouts/
  default.html    # Ana şablon (head, nav, footer)
  page.html       # Statik sayfalar için
_includes/
  head.html       # Meta, CSS linkleri
  nav.html        # Navigasyon
  footer.html     # Alt bilgi
  project-card.html  # Proje kartı bileşeni
```

## Proje Kartı Bileşeni

```html
<!-- _includes/project-card.html -->
<article class="project-card">
  <img src="{{ include.image }}" alt="{{ include.title }}" loading="lazy" width="400" height="250">
  <div class="project-card__content">
    <h3>{{ include.title }}</h3>
    <p>{{ include.description }}</p>
    <div class="project-card__links">
      {% if include.github %}<a href="{{ include.github }}">GitHub</a>{% endif %}
      {% if include.demo %}<a href="{{ include.demo }}">Demo</a>{% endif %}
    </div>
  </div>
</article>
```

Kullanım: `{% include project-card.html title="Proje Adı" image="/assets/images/proje.webp" %}`

## CSS Değişkenleri (Başlangıç)

```css
:root {
  --color-primary: #2563eb;
  --color-bg: #ffffff;
  --color-text: #1e293b;
  --color-muted: #64748b;
  --font-sans: system-ui, -apple-system, sans-serif;
  --spacing-sm: 0.5rem;
  --spacing-md: 1rem;
  --spacing-lg: 2rem;
  --spacing-xl: 4rem;
  --radius: 0.5rem;
  --max-width: 1100px;
}
```

## Responsive Grid

```css
.projects-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--spacing-lg);
}

@media (min-width: 640px) {
  .projects-grid { grid-template-columns: repeat(2, 1fr); }
}

@media (min-width: 1024px) {
  .projects-grid { grid-template-columns: repeat(3, 1fr); }
}
```

## _config.yml Şablonu

```yaml
title: Ömer Faruk Kural
description: Portfolyo sitesi
baseurl: ""
url: "https://bitir.me"
author:
  name: Ömer Faruk Kural
  email: your@email.com
  github: omerfarukkural

plugins:
  - jekyll-feed
  - jekyll-seo-tag
```

## Yaygın Kalıplar

**Smooth scroll:**
```css
html { scroll-behavior: smooth; }
```

**Focus görünürlüğü (erişilebilirlik):**
```css
:focus-visible { outline: 2px solid var(--color-primary); outline-offset: 2px; }
```

**Kart hover efekti:**
```css
.project-card { transition: transform 0.2s ease, box-shadow 0.2s ease; }
.project-card:hover { transform: translateY(-4px); box-shadow: 0 8px 24px rgba(0,0,0,0.12); }
```

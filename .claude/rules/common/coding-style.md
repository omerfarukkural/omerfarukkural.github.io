# Kodlama Stili

## HTML
- Semantic elementler kullan: `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`
- Her img için `alt` attribute zorunlu
- İndentation: 2 boşluk
- Attribute sırası: id → class → data-* → diğerleri

## CSS
- CSS custom properties (variables) kullan: `--color-primary`, `--spacing-md`
- Mobile-first medya sorguları: `min-width` kullan
- BEM naming: `.block__element--modifier`
- `!important` kullanma

## JavaScript
- Vanilla JS tercih et, gereksiz kütüphane ekleme
- `const` ve `let` kullan, `var` kullanma
- DOM hazır olunca çalıştır: `DOMContentLoaded`

## Jekyll
- Frontmatter her sayfada zorunlu: `layout`, `title`
- Liquid tag'leri düzgün kapat: `{% %}` ve `{{ }}`
- `_config.yml` değişikliği için server restart gerekir

## Git
- Commit mesajı: `feat:`, `fix:`, `style:`, `content:` prefix kullan
- Her anlamlı değişiklik için ayrı commit
- `main` branch'e direkt push yerine branch kullan

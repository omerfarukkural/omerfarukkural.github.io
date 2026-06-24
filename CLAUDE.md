# Portfolio – omerfarukkural.github.io

Ömer Faruk Kural'ın kişisel portfolyo sitesi. GitHub Pages + Jekyll ile barındırılıyor, özel domain: **bitir.me**

## Proje Yapısı

```
omerfarukkural.github.io/
├── _config.yml          # Jekyll yapılandırması
├── _layouts/            # Sayfa şablonları
├── _includes/           # Tekrar kullanılabilir bileşenler
├── _posts/              # Blog yazıları (opsiyonel)
├── assets/
│   ├── css/             # Stiller
│   ├── js/              # JavaScript
│   └── images/          # Görseller
├── index.html           # Ana sayfa
├── CNAME                # Özel domain (bitir.me)
└── .github/workflows/   # CI/CD pipeline
```

## Teknoloji Yığını

- **Platform:** GitHub Pages (otomatik deploy)
- **SSG:** Jekyll
- **Domain:** bitir.me
- **CI/CD:** GitHub Actions (jekyll-gh-pages.yml)

## Geliştirme Kuralları

- Saf HTML/CSS/JS tercih et — gereksiz framework ekleme
- Mobil öncelikli (mobile-first) tasarım
- Erişilebilirlik: semantic HTML, alt text, kontrast
- Performans: görsel boyutları optimize et, gereksiz JS yükleme
- Jekyll liquid template sözdizimini kullan
- Commit mesajları Türkçe veya İngilizce olabilir

## İçerik Bölümleri

Portfolyo şu bölümleri içermeli:
- **Hero / Hakkımda:** Kısa tanıtım
- **Projeler:** Öne çıkan çalışmalar
- **Yetenekler:** Teknik beceriler
- **İletişim:** Bağlantı bilgileri

## Deployment

`main` branch'e push → GitHub Actions otomatik build → bitir.me'de yayın

## Geliştirirken

- `bundle exec jekyll serve --livereload` ile yerel preview
- Deploy öncesi mobil görünümü kontrol et
- Görselleri `assets/images/` altına koy
- Yeni sayfa eklerken `layout: default` frontmatter kullan

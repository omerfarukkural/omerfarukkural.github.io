# Performans Kuralları

## Görseller
- WebP formatı kullan (PNG/JPG yerine)
- `loading="lazy"` attribute ekle (hero dışındakilere)
- `width` ve `height` attribute belirt (CLS önlemek için)
- Hero görselleri < 200KB, diğerleri < 100KB

## CSS/JS Yükleme
- CSS `<head>` içinde yükle
- JS `<body>` sonuna koy veya `defer` kullan
- Google Fonts kullanıyorsan `preconnect` ekle:
  ```html
  <link rel="preconnect" href="https://fonts.googleapis.com">
  ```

## Model Seçimi (AI ile çalışırken)
- Rutin HTML/CSS değişiklikler → Sonnet yeterli
- Karmaşık mimari kararlar → Opus kullan
- `/compact` komutunu uzun oturumlarda kullan

## GitHub Pages Limitleri
- Site boyutu < 1GB
- Bandwidth < 100GB/ay
- Build süresi < 10 dakika

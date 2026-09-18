# Eyüb Cemallıoğlu — Kişisel Web Sitesi

Tek sayfalık, premium koyu temalı kişisel portföy sitesi. Framework yok — sadece **HTML + CSS + JS**.

## Çalıştırma

Herhangi bir statik sunucu yeterli:

```bash
npx serve .        # veya
python -m http.server 8000
```

Sonra tarayıcıda `http://localhost:8000` (veya sunucunun verdiği port) aç.

## Dosyalar

| Dosya | İçerik |
|---|---|
| `index.html` | Tüm bölümler (hero, hakkımda, alanlar, projeler, süreç, stack, yolculuk, vizyon, iletişim...) |
| `style.css` | Tema: neredeyse siyah zemin, elektrik mavisi + hafif mor, glassmorphism |
| `main.js` | Parçacık arka planı, scroll animasyonları, kart tilt/spotlight, timeline ilerlemesi |
| `preview.html` | Otomatik oluşturulan tek dosyalık önizleme kopyası (düzenleme için kullanma) |
| `build_preview.py` | `preview.html` üreticisi: CSS/JS'i gömer, galeri görsellerini base64 olarak ekler |
| `assets/gallery/` | Galeri görselleri (uygulama ekran görüntüleri, İHA fotoğrafları) |

## Düzenlenecek Yerler

- **Sosyal linkler** → `index.html` içinde `id="contact"` bölümündeki `href` değerleri (GitHub / Instagram / E-Mail).
- **Proje linkleri** → her `.project-card__link` altındaki `href` (şimdilik `#contact`).
- **Galeri** → yeni görseli `assets/gallery/` klasörüne at, `index.html` içindeki `gallery__grid` bölümüne yeni bir `gallery__item` ekle, sonra aşağıdaki komutu çalıştır.
- **preview.html yenileme** → `index.html`, `style.css`, `main.js` veya görseller değiştikten sonra:

```bash
python build_preview.py
```

# Aybala Ören Diş Kliniği – Web Sitesi

Kozan / Adana'daki Aybala Ören Diş Kliniği için geliştirdiğim, tek sayfalık (single-page), responsive bir tanıtım sitesi.

Projede herhangi bir framework, build aracı ya da harici kütüphane kullanmadım. Site saf HTML5, CSS3 ve vanilla JavaScript ile yazıldı ve statik dosya olarak sunuluyor.

## Özellikler

- **Responsive tasarım:** Masaüstü, tablet ve mobil için `@media` sorgularıyla ayrı düzenler (kırılma noktaları: 1000px ve 820px)
- **Mobil menü:** 820px altında hamburger menüye dönüşen, JavaScript ile açılıp kapanan tam ekran navigasyon
- **Sabit (fixed) navigasyon:** Sayfa kaydırıldığında arka planı koyulaşan üst menü (`scroll` event listener)
- **Bölümler arası yumuşak geçiş:** `scroll-behavior: smooth` ve sabit menünün içeriği örtmemesi için `scroll-margin-top`
- **WhatsApp entegrasyonu:** `wa.me` bağlantısı ile sabit konumlu randevu butonu
- **Tıklanabilir telefon:** Mobilde doğrudan arama başlatan `tel:` bağlantısı
- **Harita bağlantısı:** Google Maps arama URL'i ile adres yönlendirmesi
- **Performans:** Ekran dışındaki görsellerde `loading="lazy"`, görseller web için yeniden boyutlandırıldı
- **SEO temelleri:** `lang="tr"`, `meta description`, anlamlı başlık hiyerarşisi ve tüm görsellerde `alt` metinleri
- **Erişilebilirlik:** Simge butonlarında `aria-label`, dekoratif SVG'lerde `aria-hidden`

## Sayfa yapısı

| Bölüm | İçerik |
|---|---|
| Hero | Tam ekran görsel, gradyan overlay, başlık ve CTA |
| Hizmetler | Genel, estetik ve çocuk diş hekimliği (inline SVG ikonlar) |
| Tedaviler | Kanal tedavisi, dolgu, beyazlatma, diş çekimi, zirkonyum |
| Galeri | 4 sütunlu CSS Grid (mobilde 2 sütun) |
| Hakkımızda | Hekim biyografisi, eğitim bilgileri, kurslar ve kongreler |
| Randevu (CTA) | WhatsApp yönlendirmesi |
| İletişim | Adres, telefon, çalışma saatleri |

## Teknolojiler

- **HTML5**: semantik etiketler (`header`, `nav`, `section`, `footer`)
- **CSS3**: CSS değişkenleri (custom properties), Flexbox, CSS Grid, `clamp()` ile akışkan tipografi, `aspect-ratio`, `object-fit`
- **JavaScript (vanilla)**: menü ve scroll davranışları
- **Google Fonts**: Cormorant Garamond (başlıklar), Jost (metin)
- **Görseller**: Unsplash Lisansı kapsamında telifsiz fotoğraflar
- **Hosting**: Netlify (statik deploy)

## Dosya yapısı

```
├── index.html      # Sayfa yapısı ve içerik
├── style.css       # Tasarım, renk değişkenleri ve responsive kurallar
├── images/         # Optimize edilmiş görseller
└── README.md
```

## Yerelde çalıştırma

Kurulum gerekmiyor. `index.html` dosyasını doğrudan tarayıcıda açmak yeterli. İstenirse basit bir yerel sunucuyla da çalıştırılabilir:

```bash
python3 -m http.server 5500
```

Ardından tarayıcıda `http://localhost:5500` adresine gidilir.

## Yayın

Site şu anda Netlify üzerinde `*.netlify.app` alt alan adıyla yayında. Güncellemeler, dosyaların Netlify'a yeniden deploy edilmesiyle yayına alınıyor.

## Proje durumu ve sonraki adımlar

- [ ] **Alan adı (domain):** Site için özel bir alan adı alınacak ve Netlify'a bağlanacak (DNS ayarları + otomatik SSL).Klinik şu anda inşaat aşamasında olduğundan, alan adı alımı inşaatın tamamlanmasının ardından yapılacak.
- [ ] Unsplash görsellerinin kliniğin kendi fotoğraflarıyla değiştirilmesi
- [ ] Google İşletme Profili ve Google Haritalar konumunun siteye bağlanması
- [x] Tüm içerik bölümlerinin tamamlanması
- [x] Mobil uyumluluk
- [x] WhatsApp ve telefon entegrasyonu

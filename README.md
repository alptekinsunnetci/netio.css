# netio.css

**Türkçe sınıf isimli, hafif ve modern CSS framework.**

Temel özellikleri Türkçe sınıf isimleriyle sunan, sıfır bağımlılıklı, performans odaklı bir CSS kütüphanesi.

[![Sürüm](https://img.shields.io/badge/sürüm-1.0.0-blue.svg)]()
[![Boyut](https://img.shields.io/badge/boyut-~65KB-green.svg)]()
[![Lisans](https://img.shields.io/badge/lisans-MIT-yellow.svg)]()

---

## Özellikler

- **Tamamen Türkçe** — Tüm sınıf isimleri Türkçe: `.buton`, `.kart`, `.satir`, `.gezinti`...
- **12 Kolonlu Grid** — Flexbox tabanlı, responsive, mobil öncelikli ızgara sistemi
- **50+ Bileşen** — Buton, kart, modal, navbar, form, tooltip, akordiyon, sekmeler ve daha fazlası
- **Light/Dark Tema** — CSS değişkenleri ile tek satırda tema değişimi
- **Utility Sınıfları** — Margin, padding, flex, renk, gölge, kenar yuvarlaklık
- **Sıfır Bağımlılık** — Hiçbir harici kütüphane gerektirmez
- **Hafif** — ~65 KB (minify edilmeden), gereksiz kodlardan arındırılmış

---

## Hızlı Başlangıç

### CDN / Doğrudan Kullanım

```html
<link rel="stylesheet" href="dist/netio.css">
```

### Projeye Dahil Etme

`dist/netio.css` dosyasını projenize kopyalayın ve HTML dosyanızın `<head>` bölümüne ekleyin:

```html
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Benim Sitem</title>
  <link rel="stylesheet" href="dist/netio.css">
</head>
<body>
  <h1 class="baslik-1">Merhaba Dünya!</h1>
  <button class="buton buton-birincil">Tıkla</button>
</body>
</html>
```

### Modüler Kullanım (Geliştirme)

Sadece ihtiyacınız olan modülleri `src/` klasöründen içerebilirsiniz:

```css
@import "src/_degiskenler.css";
@import "src/_sifirlama.css";
@import "src/_izgara.css";
@import "src/_butonlar.css";
/* ihtiyacınız olan diğer modüller... */
```

---

## Klasör Yapısı

```
netio.css/
├── dist/
│   └── netio.css              # Birleşik üretim dosyası (~65 KB)
├── src/
│   ├── netio.css              # Ana giriş (@import ile modüller)
│   ├── _degiskenler.css       # Tema, renkler, CSS değişkenleri
│   ├── _sifirlama.css         # CSS reset/normalize
│   ├── _izgara.css            # 12 kolonlu responsive grid
│   ├── _tipografi.css         # Başlıklar, metin stilleri
│   ├── _butonlar.css          # Buton çeşitleri
│   ├── _formlar.css           # Input, select, checkbox, switch
│   ├── _gezinti.css           # Navbar, dropdown, sticky
│   ├── _modal.css             # Açılır pencere, overlay
│   ├── _ipucu.css             # Tooltip ve popover
│   ├── _bilesenler.css        # Kart, uyarı, rozet, spinner, akordiyon...
│   └── _yardimcilar.css       # Utility sınıfları
└── docs/
    └── index.html             # İnteraktif dokümantasyon sayfası
```

---

## Kullanım Örnekleri

### Izgara Sistemi

12 kolonlu, responsive grid. Mobilde tam genişlik, tablette 2'li, masaüstünde 4'lü düzen:

```html
<div class="kapsayici">
  <div class="satir bosluk-4">
    <div class="kolon-12 kolon-orta-6 kolon-buyuk-3">1. Kolon</div>
    <div class="kolon-12 kolon-orta-6 kolon-buyuk-3">2. Kolon</div>
    <div class="kolon-12 kolon-orta-6 kolon-buyuk-3">3. Kolon</div>
    <div class="kolon-12 kolon-orta-6 kolon-buyuk-3">4. Kolon</div>
  </div>
</div>
```

**Breakpoint tablosu:**

| Sınıf Öneki | Ekran Boyutu | Piksel |
|---|---|---|
| *(yok)* | Mobil (varsayılan) | 0px+ |
| `kolon-kucuk-` | Küçük ekran | 576px+ |
| `kolon-orta-` | Orta ekran | 768px+ |
| `kolon-buyuk-` | Büyük ekran | 992px+ |
| `kolon-dev-` | Çok büyük ekran | 1200px+ |

### Butonlar

```html
<!-- Dolu butonlar -->
<button class="buton buton-birincil">Birincil</button>
<button class="buton buton-basari">Başarı</button>
<button class="buton buton-tehlike">Tehlike</button>

<!-- Çizgili (outline) butonlar -->
<button class="buton buton-cizgili-birincil">Çizgili</button>

<!-- Boyutlar -->
<button class="buton buton-birincil buton-mini">Mini</button>
<button class="buton buton-birincil buton-kucuk">Küçük</button>
<button class="buton buton-birincil buton-buyuk">Büyük</button>
<button class="buton buton-birincil buton-dev">Dev</button>

<!-- Özel stiller -->
<button class="buton buton-birincil buton-yuvarlak">Yuvarlak</button>
<button class="buton buton-birincil buton-tam">Tam Genişlik</button>
<button class="buton buton-birincil" disabled>Devre Dışı</button>

<!-- Buton grubu -->
<div class="buton-grubu">
  <button class="buton buton-birincil">Sol</button>
  <button class="buton buton-birincil">Orta</button>
  <button class="buton buton-birincil">Sağ</button>
</div>
```

### Kartlar

```html
<div class="kart">
  <img src="resim.jpg" class="kart-resim kart-resim-ust" alt="Açıklama">
  <div class="kart-govde">
    <h5 class="kart-baslik">Kart Başlığı</h5>
    <p class="kart-metin">Kart içeriği burada yer alır.</p>
    <button class="buton buton-birincil buton-kucuk">Devamını Oku</button>
  </div>
</div>
```

### Navbar (Gezinti Çubuğu)

```html
<nav class="gezinti gezinti-yapisan gezinti-koyu">
  <a href="#" class="gezinti-marka">SiteAdı</a>
  <button class="gezinti-acilan">
    <span></span><span></span><span></span>
  </button>
  <ul class="gezinti-menu">
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti aktif">Ana Sayfa</a>
    </li>
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti">Hakkında</a>
    </li>
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti">İletişim</a>
    </li>
  </ul>
</nav>
```

### Modal (Açılır Pencere)

```html
<!-- Tetikleyici buton -->
<button class="buton buton-birincil" onclick="modalAc()">Modal Aç</button>

<!-- Modal -->
<div class="modal-perde" id="benimModal">
  <div class="modal-pencere">
    <div class="modal-baslik">
      <h4>Pencere Başlığı</h4>
      <button class="modal-kapat" onclick="modalKapat()"></button>
    </div>
    <div class="modal-govde">
      <p>Modal içeriği burada.</p>
    </div>
    <div class="modal-altlik">
      <button class="buton buton-ikincil buton-kucuk" onclick="modalKapat()">İptal</button>
      <button class="buton buton-birincil buton-kucuk">Onayla</button>
    </div>
  </div>
</div>

<script>
  function modalAc() {
    document.getElementById('benimModal').classList.add('acik');
    document.body.classList.add('modal-acik');
  }
  function modalKapat() {
    document.getElementById('benimModal').classList.remove('acik');
    document.body.classList.remove('modal-acik');
  }
</script>
```

### Form Elemanları

```html
<div class="form-grup">
  <label class="form-etiket">E-posta</label>
  <input type="email" class="form-girdi" placeholder="ornek@email.com">
  <span class="form-yardim">E-posta adresinizi girin</span>
</div>

<div class="form-grup">
  <label class="form-etiket">Şehir</label>
  <select class="form-secim">
    <option>İstanbul</option>
    <option>Ankara</option>
  </select>
</div>

<!-- Doğrulama durumları -->
<input type="text" class="form-girdi gecerli" value="doğru değer">
<span class="form-gecerli-mesaj">Geçerli!</span>

<input type="text" class="form-girdi gecersiz" value="yanlış değer">
<span class="form-gecersiz-mesaj">Geçersiz format</span>

<!-- Switch / Anahtar -->
<label class="form-anahtar">
  <input type="checkbox" checked>
  <span>Bildirimler Açık</span>
</label>
```

### Uyarılar (Alert)

```html
<div class="uyari uyari-basari">İşlem başarıyla tamamlandı!</div>
<div class="uyari uyari-tehlike">Bir hata oluştu!</div>
<div class="uyari uyari-uyari">Dikkat! Bu işlem geri alınamaz.</div>
<div class="uyari uyari-bilgi">Bilgilendirme mesajı.</div>
```

### Tooltip (İpucu)

```html
<span class="ipucu" data-ipucu="Bu bir ipucu!">Üzerime gel</span>
<span class="ipucu ipucu-alt" data-ipucu="Alt tarafta">Alttan göster</span>
<span class="ipucu ipucu-sol" data-ipucu="Sol tarafta">Soldan göster</span>
<span class="ipucu ipucu-sag" data-ipucu="Sağ tarafta">Sağdan göster</span>
```

### Akordiyon

```html
<div class="akordiyon">
  <div class="akordiyon-oge acik">
    <button class="akordiyon-baslik" onclick="this.parentElement.classList.toggle('acik')">
      Birinci Başlık
    </button>
    <div class="akordiyon-icerik">
      <div class="akordiyon-govde">Birinci içerik burada.</div>
    </div>
  </div>
  <div class="akordiyon-oge">
    <button class="akordiyon-baslik" onclick="this.parentElement.classList.toggle('acik')">
      İkinci Başlık
    </button>
    <div class="akordiyon-icerik">
      <div class="akordiyon-govde">İkinci içerik burada.</div>
    </div>
  </div>
</div>
```

### Sekmeler (Tabs)

```html
<div class="sekmeler">
  <button class="sekme aktif">Sekme 1</button>
  <button class="sekme">Sekme 2</button>
  <button class="sekme">Sekme 3</button>
</div>
<div class="sekme-icerik aktif">Birinci sekme içeriği</div>
<div class="sekme-icerik">İkinci sekme içeriği</div>
```

---

## Tema ve Renk Yönetimi

### Koyu Tema Aktif Etme

```html
<!-- Yöntem 1: HTML attribute -->
<html data-tema="koyu">

<!-- Yöntem 2: CSS sınıfı -->
<body class="tema-koyu">
```

```javascript
// Yöntem 3: JavaScript ile değiştirme
function temaDegistir() {
  const html = document.documentElement;
  const mevcut = html.getAttribute('data-tema');
  html.setAttribute('data-tema', mevcut === 'koyu' ? 'acik' : 'koyu');
}
```

### CSS Değişkenleri ile Özelleştirme

Kendi temanızı oluşturmak için `:root` altındaki değişkenleri ezin:

```css
:root {
  /* Renkleri değiştir */
  --birincil: #8b5cf6;
  --birincil-koyu: #7c3aed;
  --birincil-acik: #ede9fe;

  /* Yazı tipini değiştir */
  --yazi-tipi: 'Poppins', sans-serif;

  /* Kenarları daha yuvarlak yap */
  --yuvarlaklık: 0.75rem;
  --yuvarlaklık-orta: 1rem;

  /* Gölgeleri güçlendir */
  --golge: 0 2px 8px rgba(0, 0, 0, 0.15);
}
```

### Mevcut CSS Değişkenleri

| Değişken | Varsayılan | Açıklama |
|---|---|---|
| `--birincil` | `#3b82f6` | Ana tema rengi |
| `--basari` | `#22c55e` | Başarı/onay rengi |
| `--tehlike` | `#ef4444` | Hata/tehlike rengi |
| `--uyari` | `#f59e0b` | Uyarı rengi |
| `--bilgi` | `#06b6d4` | Bilgi rengi |
| `--metin` | `#1e293b` | Ana metin rengi |
| `--arkaplan` | `#ffffff` | Sayfa arkaplan rengi |
| `--kenar-renk` | `#e2e8f0` | Kenar çizgisi rengi |
| `--yazi-tipi` | `Inter, sans-serif` | Ana yazı tipi |
| `--yuvarlaklık` | `0.375rem` | Varsayılan kenar yuvarlaklık |

---

## Yardımcı Sınıflar Referansı

### Aralık (Spacing)

| Sınıf | Açıklama | Değer |
|---|---|---|
| `.m-{0-6}` | Tüm kenarlara margin | 0 - 2rem |
| `.mt-`, `.mr-`, `.mb-`, `.ml-` | Tek kenar margin | — |
| `.mx-`, `.my-` | Yatay / dikey margin | — |
| `.p-{0-6}` | Tüm kenarlara padding | 0 - 2rem |
| `.pt-`, `.pr-`, `.pb-`, `.pl-` | Tek kenar padding | — |
| `.px-`, `.py-` | Yatay / dikey padding | — |

### Display

| Sınıf | Karşılığı |
|---|---|
| `.d-yok` | `display: none` |
| `.d-blok` | `display: block` |
| `.d-flex` | `display: flex` |
| `.d-satir-blok` | `display: inline-block` |
| `.d-satir-flex` | `display: inline-flex` |
| `.d-izgara` | `display: grid` |

### Flex

| Sınıf | Karşılığı |
|---|---|
| `.flex-satir` | `flex-direction: row` |
| `.flex-sutun` | `flex-direction: column` |
| `.flex-sar` | `flex-wrap: wrap` |
| `.icerik-orta` | `justify-content: center` |
| `.icerik-arasi` | `justify-content: space-between` |
| `.oge-orta` | `align-items: center` |

### Metin

| Sınıf | Açıklama |
|---|---|
| `.metin-ortala` | Yazı ortala |
| `.metin-sola` | Sola yasla |
| `.metin-saga` | Sağa yasla |
| `.kalin` | Kalın yazı |
| `.italik` | İtalik yazı |
| `.buyuk-harf` | BÜYÜK HARFE çevir |
| `.metin-kes` | Taşmada ... ile kes |

### Metin ve Arkaplan Renkleri

```html
<!-- Metin renkleri -->
<p class="metin-birincil">Mavi metin</p>
<p class="metin-basari">Yeşil metin</p>
<p class="metin-tehlike">Kırmızı metin</p>

<!-- Arkaplan renkleri -->
<div class="ap-birincil metin-beyaz">Mavi arkaplan</div>
<div class="ap-basari metin-beyaz">Yeşil arkaplan</div>
```

### Diğer Yardımcılar

| Sınıf | Açıklama |
|---|---|
| `.golge`, `.golge-orta`, `.golge-buyuk` | Kutu gölgesi |
| `.yuvarlak`, `.yuvarlak-tam`, `.daire` | Kenar yuvarlaklık |
| `.kenar`, `.kenar-yok` | Kenar çizgisi |
| `.g-100`, `.g-50` | Genişlik (%100, %50) |
| `.y-ekran` | Yükseklik: 100vh |
| `.tasma-gizle`, `.tasma-kaydir` | Overflow kontrolü |
| `.konum-yapisan` | Sticky konumlama |
| `.gecis`, `.gecis-hizli` | Geçiş animasyonu |
| `.saydamlik-50` | %50 saydamlık |

---

## Bileşen Referansı

| Bileşen | Ana Sınıf | Alt Sınıflar |
|---|---|---|
| **Izgara** | `.kapsayici`, `.satir` | `.kolon-{1-12}`, `.kolon-orta-{1-12}` |
| **Buton** | `.buton` | `.buton-birincil`, `.buton-cizgili-*`, `.buton-kucuk` |
| **Kart** | `.kart` | `.kart-govde`, `.kart-baslik`, `.kart-altlik` |
| **Modal** | `.modal-perde` | `.modal-pencere`, `.modal-baslik`, `.modal-govde` |
| **Navbar** | `.gezinti` | `.gezinti-marka`, `.gezinti-menu`, `.gezinti-baglanti` |
| **Form** | `.form-grup` | `.form-girdi`, `.form-secim`, `.form-anahtar` |
| **Uyarı** | `.uyari` | `.uyari-basari`, `.uyari-tehlike`, `.uyari-uyari` |
| **Rozet** | `.rozet` | `.rozet-birincil`, `.rozet-basari` |
| **Spinner** | `.dondurucu` | `.dondurucu-kucuk`, `.dondurucu-buyuk` |
| **Tablo** | `.tablo` | `.tablo-seritli`, `.tablo-cizgili` |
| **Akordiyon** | `.akordiyon` | `.akordiyon-oge`, `.akordiyon-baslik` |
| **Sekmeler** | `.sekmeler` | `.sekme`, `.sekme-icerik`, `.sekmeler-hap` |
| **Tooltip** | `.ipucu` | `.ipucu-alt`, `.ipucu-sol`, `.ipucu-sag` |
| **İlerleme** | `.ilerleme` | `.ilerleme-cubuk`, `.ilerleme-cubuk-basari` |
| **Avatar** | `.avatar` | `.avatar-kucuk`, `.avatar-buyuk`, `.avatar-grubu` |
| **Breadcrumb** | `.ekmek-kirintisi` | — |
| **Liste Grubu** | `.liste-grubu` | `.liste-grubu-oge` |
| **Slider** | `.slider` | `.slider-iz`, `.slider-slayt`, `.slider-noktalar` |

---

## Tarayıcı Desteği

netio.css modern CSS özellikleri kullanır ve aşağıdaki tarayıcıları destekler:

- Chrome 80+
- Firefox 80+
- Safari 14+
- Edge 80+

---

## Lisans

Apache-2.0 ile dağıtılmaktadır.

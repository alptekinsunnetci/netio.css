# netio.css

**Türkçe sinif isimli, hafif ve modern CSS framework.**

Temel ozellikleri Türkçe sinif isimleriyle sunan, sifir bagimlilikli, performans odakli bir CSS kutuphanesi.

[![Surum](https://img.shields.io/badge/surum-1.0.0-blue.svg)]()
[![Boyut](https://img.shields.io/badge/boyut-~65KB-green.svg)]()
[![Lisans](https://img.shields.io/badge/lisans-MIT-yellow.svg)]()

---

## Ozellikler

- **Tamamen Türkçe** — Tum sinif isimleri Türkçe: `.buton`, `.kart`, `.satir`, `.gezinti`...
- **12 Kolonlu Grid** — Flexbox tabanli, responsive, mobil oncelikli izgara sistemi
- **50+ Bilesen** — Buton, kart, modal, navbar, form, tooltip, akordiyon, sekmeler ve daha fazlasi
- **Light/Dark Tema** — CSS degiskenleri ile tek satirda tema degisimi
- **Utility Siniflari** — Margin, padding, flex, renk, golge, kenar yuvarlaklik
- **Sifir Bagimlilik** — Hicbir harici kutuphane gerektirmez
- **Hafif** — ~65 KB (minify edilmeden), gereksiz kodlardan arindirilmis

---

## Hizli Baslangic

### CDN / Dogrudan Kullanim

```html
<link rel="stylesheet" href="dist/netio.css">
```

### Projeye Dahil Etme

`dist/netio.css` dosyasini projenize kopyalayin ve HTML dosyanizin `<head>` bolumune ekleyin:

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
  <h1 class="baslik-1">Merhaba Dunya!</h1>
  <button class="buton buton-birincil">Tikla</button>
</body>
</html>
```

### Moduler Kullanim (Gelistirme)

Sadece ihtiyaciniz olan modulleri `src/` klasorunden icerebilirsiniz:

```css
@import "src/_degiskenler.css";
@import "src/_sifirlama.css";
@import "src/_izgara.css";
@import "src/_butonlar.css";
/* ihtiyaciniz olan diger moduller... */
```

---

## Klasor Yapisi

```
netio.css/
├── dist/
│   └── netio.css              # Birlesik uretim dosyasi (~65 KB)
├── src/
│   ├── netio.css              # Ana giris (@import ile moduller)
│   ├── _degiskenler.css       # Tema, renkler, CSS degiskenleri
│   ├── _sifirlama.css         # CSS reset/normalize
│   ├── _izgara.css            # 12 kolonlu responsive grid
│   ├── _tipografi.css         # Basliklar, metin stilleri
│   ├── _butonlar.css          # Buton cesitleri
│   ├── _formlar.css           # Input, select, checkbox, switch
│   ├── _gezinti.css           # Navbar, dropdown, sticky
│   ├── _modal.css             # Acilir pencere, overlay
│   ├── _ipucu.css             # Tooltip ve popover
│   ├── _bilesenler.css        # Kart, uyari, rozet, spinner, akordiyon...
│   └── _yardimcilar.css       # Utility siniflari
└── docs/
    └── index.html             # Interaktif dokumantasyon sayfasi
```

---

## Kullanim Ornekleri

### Izgara Sistemi

12 kolonlu, responsive grid. Mobilde tam genislik, tablette 2'li, masaustunde 4'lu duzen:

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

| Sinif Oneki | Ekran Boyutu | Piksel |
|---|---|---|
| *(yok)* | Mobil (varsayilan) | 0px+ |
| `kolon-kucuk-` | Kucuk ekran | 576px+ |
| `kolon-orta-` | Orta ekran | 768px+ |
| `kolon-buyuk-` | Buyuk ekran | 992px+ |
| `kolon-dev-` | Cok buyuk ekran | 1200px+ |

### Butonlar

```html
<!-- Dolu butonlar -->
<button class="buton buton-birincil">Birincil</button>
<button class="buton buton-basari">Basari</button>
<button class="buton buton-tehlike">Tehlike</button>

<!-- Cizgili (outline) butonlar -->
<button class="buton buton-cizgili-birincil">Cizgili</button>

<!-- Boyutlar -->
<button class="buton buton-birincil buton-mini">Mini</button>
<button class="buton buton-birincil buton-kucuk">Kucuk</button>
<button class="buton buton-birincil buton-buyuk">Buyuk</button>
<button class="buton buton-birincil buton-dev">Dev</button>

<!-- Ozel stiller -->
<button class="buton buton-birincil buton-yuvarlak">Yuvarlak</button>
<button class="buton buton-birincil buton-tam">Tam Genislik</button>
<button class="buton buton-birincil" disabled>Devre Disi</button>

<!-- Buton grubu -->
<div class="buton-grubu">
  <button class="buton buton-birincil">Sol</button>
  <button class="buton buton-birincil">Orta</button>
  <button class="buton buton-birincil">Sag</button>
</div>
```

### Kartlar

```html
<div class="kart">
  <img src="resim.jpg" class="kart-resim kart-resim-ust" alt="Aciklama">
  <div class="kart-govde">
    <h5 class="kart-baslik">Kart Basligi</h5>
    <p class="kart-metin">Kart icerigi burada yer alir.</p>
    <button class="buton buton-birincil buton-kucuk">Devamini Oku</button>
  </div>
</div>
```

### Navbar (Gezinti Cubugu)

```html
<nav class="gezinti gezinti-yapisan gezinti-koyu">
  <a href="#" class="gezinti-marka">SiteAdi</a>
  <button class="gezinti-acilan">
    <span></span><span></span><span></span>
  </button>
  <ul class="gezinti-menu">
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti aktif">Ana Sayfa</a>
    </li>
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti">Hakkinda</a>
    </li>
    <li class="gezinti-oge">
      <a href="#" class="gezinti-baglanti">Iletisim</a>
    </li>
  </ul>
</nav>
```

### Modal (Acilir Pencere)

```html
<!-- Tetikleyici buton -->
<button class="buton buton-birincil" onclick="modalAc()">Modal Ac</button>

<!-- Modal -->
<div class="modal-perde" id="benimModal">
  <div class="modal-pencere">
    <div class="modal-baslik">
      <h4>Pencere Basligi</h4>
      <button class="modal-kapat" onclick="modalKapat()"></button>
    </div>
    <div class="modal-govde">
      <p>Modal icerigi burada.</p>
    </div>
    <div class="modal-altlik">
      <button class="buton buton-ikincil buton-kucuk" onclick="modalKapat()">Iptal</button>
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

### Form Elemanlari

```html
<div class="form-grup">
  <label class="form-etiket">E-posta</label>
  <input type="email" class="form-girdi" placeholder="ornek@email.com">
  <span class="form-yardim">E-posta adresinizi girin</span>
</div>

<div class="form-grup">
  <label class="form-etiket">Sehir</label>
  <select class="form-secim">
    <option>Istanbul</option>
    <option>Ankara</option>
  </select>
</div>

<!-- Dogrulama durumlari -->
<input type="text" class="form-girdi gecerli" value="dogru deger">
<span class="form-gecerli-mesaj">Gecerli!</span>

<input type="text" class="form-girdi gecersiz" value="yanlis deger">
<span class="form-gecersiz-mesaj">Gecersiz format</span>

<!-- Switch / Anahtar -->
<label class="form-anahtar">
  <input type="checkbox" checked>
  <span>Bildirimler Acik</span>
</label>
```

### Uyarilar (Alert)

```html
<div class="uyari uyari-basari">Islem basariyla tamamlandi!</div>
<div class="uyari uyari-tehlike">Bir hata olustu!</div>
<div class="uyari uyari-uyari">Dikkat! Bu islem geri alinamaz.</div>
<div class="uyari uyari-bilgi">Bilgilendirme mesaji.</div>
```

### Tooltip (Ipucu)

```html
<span class="ipucu" data-ipucu="Bu bir ipucu!">Uzerime gel</span>
<span class="ipucu ipucu-alt" data-ipucu="Alt tarafta">Alttan goster</span>
<span class="ipucu ipucu-sol" data-ipucu="Sol tarafta">Soldan goster</span>
<span class="ipucu ipucu-sag" data-ipucu="Sag tarafta">Sagdan goster</span>
```

### Akordiyon

```html
<div class="akordiyon">
  <div class="akordiyon-oge acik">
    <button class="akordiyon-baslik" onclick="this.parentElement.classList.toggle('acik')">
      Birinci Baslik
    </button>
    <div class="akordiyon-icerik">
      <div class="akordiyon-govde">Birinci icerik burada.</div>
    </div>
  </div>
  <div class="akordiyon-oge">
    <button class="akordiyon-baslik" onclick="this.parentElement.classList.toggle('acik')">
      Ikinci Baslik
    </button>
    <div class="akordiyon-icerik">
      <div class="akordiyon-govde">Ikinci icerik burada.</div>
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
<div class="sekme-icerik aktif">Birinci sekme icerigi</div>
<div class="sekme-icerik">Ikinci sekme icerigi</div>
```

---

## Tema ve Renk Yonetimi

### Koyu Tema Aktif Etme

```html
<!-- Yontem 1: HTML attribute -->
<html data-tema="koyu">

<!-- Yontem 2: CSS sinifi -->
<body class="tema-koyu">
```

```javascript
// Yontem 3: JavaScript ile degistirme
function temaDegistir() {
  const html = document.documentElement;
  const mevcut = html.getAttribute('data-tema');
  html.setAttribute('data-tema', mevcut === 'koyu' ? 'acik' : 'koyu');
}
```

### CSS Degiskenleri ile Ozellestirme

Kendi temanizi olusturmak icin `:root` altindaki degiskenleri ezin:

```css
:root {
  /* Renkleri degistir */
  --birincil: #8b5cf6;
  --birincil-koyu: #7c3aed;
  --birincil-acik: #ede9fe;

  /* Yazi tipini degistir */
  --yazi-tipi: 'Poppins', sans-serif;

  /* Kenarlari daha yuvarlak yap */
  --yuvarlaklık: 0.75rem;
  --yuvarlaklık-orta: 1rem;

  /* Golgeleri guclendir */
  --golge: 0 2px 8px rgba(0, 0, 0, 0.15);
}
```

### Mevcut CSS Degiskenleri

| Degisken | Varsayilan | Aciklama |
|---|---|---|
| `--birincil` | `#3b82f6` | Ana tema rengi |
| `--basari` | `#22c55e` | Basari/onay rengi |
| `--tehlike` | `#ef4444` | Hata/tehlike rengi |
| `--uyari` | `#f59e0b` | Uyari rengi |
| `--bilgi` | `#06b6d4` | Bilgi rengi |
| `--metin` | `#1e293b` | Ana metin rengi |
| `--arkaplan` | `#ffffff` | Sayfa arkaplan rengi |
| `--kenar-renk` | `#e2e8f0` | Kenar cizgisi rengi |
| `--yazi-tipi` | `Inter, sans-serif` | Ana yazi tipi |
| `--yuvarlaklık` | `0.375rem` | Varsayilan kenar yuvarlaklik |

---

## Yardimci Siniflar Referansi

### Aralik (Spacing)

| Sinif | Aciklama | Deger |
|---|---|---|
| `.m-{0-6}` | Tum kenarlara margin | 0 - 2rem |
| `.mt-`, `.mr-`, `.mb-`, `.ml-` | Tek kenar margin | — |
| `.mx-`, `.my-` | Yatay / dikey margin | — |
| `.p-{0-6}` | Tum kenarlara padding | 0 - 2rem |
| `.pt-`, `.pr-`, `.pb-`, `.pl-` | Tek kenar padding | — |
| `.px-`, `.py-` | Yatay / dikey padding | — |

### Display

| Sinif | Karsiligi |
|---|---|
| `.d-yok` | `display: none` |
| `.d-blok` | `display: block` |
| `.d-flex` | `display: flex` |
| `.d-satir-blok` | `display: inline-block` |
| `.d-satir-flex` | `display: inline-flex` |
| `.d-izgara` | `display: grid` |

### Flex

| Sinif | Karsiligi |
|---|---|
| `.flex-satir` | `flex-direction: row` |
| `.flex-sutun` | `flex-direction: column` |
| `.flex-sar` | `flex-wrap: wrap` |
| `.icerik-orta` | `justify-content: center` |
| `.icerik-arasi` | `justify-content: space-between` |
| `.oge-orta` | `align-items: center` |

### Metin

| Sinif | Aciklama |
|---|---|
| `.metin-ortala` | Yazi ortala |
| `.metin-sola` | Sola yasla |
| `.metin-saga` | Saga yasla |
| `.kalin` | Kalin yazi |
| `.italik` | Italik yazi |
| `.buyuk-harf` | BUYUK HARFE cevir |
| `.metin-kes` | Tasmada ... ile kes |

### Metin ve Arkaplan Renkleri

```html
<!-- Metin renkleri -->
<p class="metin-birincil">Mavi metin</p>
<p class="metin-basari">Yesil metin</p>
<p class="metin-tehlike">Kirmizi metin</p>

<!-- Arkaplan renkleri -->
<div class="ap-birincil metin-beyaz">Mavi arkaplan</div>
<div class="ap-basari metin-beyaz">Yesil arkaplan</div>
```

### Diger Yardimcilar

| Sinif | Aciklama |
|---|---|
| `.golge`, `.golge-orta`, `.golge-buyuk` | Kutu golgesi |
| `.yuvarlak`, `.yuvarlak-tam`, `.daire` | Kenar yuvarlaklik |
| `.kenar`, `.kenar-yok` | Kenar cizgisi |
| `.g-100`, `.g-50` | Genislik (%100, %50) |
| `.y-ekran` | Yukseklik: 100vh |
| `.tasma-gizle`, `.tasma-kaydir` | Overflow kontrolu |
| `.konum-yapisan` | Sticky konumlama |
| `.gecis`, `.gecis-hizli` | Gecis animasyonu |
| `.saydamlik-50` | %50 saydamlik |

---

## Bilesen Referansi

| Bilesen | Ana Sinif | Alt Siniflar |
|---|---|---|
| **Izgara** | `.kapsayici`, `.satir` | `.kolon-{1-12}`, `.kolon-orta-{1-12}` |
| **Buton** | `.buton` | `.buton-birincil`, `.buton-cizgili-*`, `.buton-kucuk` |
| **Kart** | `.kart` | `.kart-govde`, `.kart-baslik`, `.kart-altlik` |
| **Modal** | `.modal-perde` | `.modal-pencere`, `.modal-baslik`, `.modal-govde` |
| **Navbar** | `.gezinti` | `.gezinti-marka`, `.gezinti-menu`, `.gezinti-baglanti` |
| **Form** | `.form-grup` | `.form-girdi`, `.form-secim`, `.form-anahtar` |
| **Uyari** | `.uyari` | `.uyari-basari`, `.uyari-tehlike`, `.uyari-uyari` |
| **Rozet** | `.rozet` | `.rozet-birincil`, `.rozet-basari` |
| **Spinner** | `.dondurucu` | `.dondurucu-kucuk`, `.dondurucu-buyuk` |
| **Tablo** | `.tablo` | `.tablo-seritli`, `.tablo-cizgili` |
| **Akordiyon** | `.akordiyon` | `.akordiyon-oge`, `.akordiyon-baslik` |
| **Sekmeler** | `.sekmeler` | `.sekme`, `.sekme-icerik`, `.sekmeler-hap` |
| **Tooltip** | `.ipucu` | `.ipucu-alt`, `.ipucu-sol`, `.ipucu-sag` |
| **Ilerleme** | `.ilerleme` | `.ilerleme-cubuk`, `.ilerleme-cubuk-basari` |
| **Avatar** | `.avatar` | `.avatar-kucuk`, `.avatar-buyuk`, `.avatar-grubu` |
| **Breadcrumb** | `.ekmek-kirintisi` | — |
| **Liste Grubu** | `.liste-grubu` | `.liste-grubu-oge` |
| **Slider** | `.slider` | `.slider-iz`, `.slider-slayt`, `.slider-noktalar` |

---

## Tarayici Destegi

netio.css modern CSS ozellikleri kullanir ve asagidaki tarayicilari destekler:

- Chrome 80+
- Firefox 80+
- Safari 14+
- Edge 80+

---

## Lisans

MIT Lisansi ile dagitilmaktadir. Ticari ve kisisel projelerde serbestce kullanilabilir.

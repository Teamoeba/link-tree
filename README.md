# 🍵 Linktree Teh

Halaman Linktree bertema teh yang lucu (*kawaii*), dibangun murni dengan HTML & CSS — tanpa framework, tanpa build step. Tinggal buka file-nya di browser.

Terdiri dari dua halaman:

| File | Fungsi |
|---|---|
| `linktree-teh.html` | Halaman utama — daftar link (menu, donasi, video, kontak) |
| `about-me.html` | Halaman "About Me" — identitas diri & hobi (gaming, anime, menggambar) dengan galeri foto |

## ✨ Fitur

- **Desain bertema teh** — palet warna krem/peach, aksen matcha, madu, dan clay
- **100% responsif** — menyesuaikan dari HP kecil, HP besar, sampai tablet (pakai `clamp()` & media query)
- **Kartu link custom** dengan efek tombol 3D lembut (hover & tekan)
- **Avatar & ikon berupa foto** — semua elemen visual pakai `<img>`, jadi tinggal ganti `src` dengan fotomu sendiri
- **Halaman About Me interaktif**:
  - Kartu hobi bisa dibuka/tutup (accordion)
  - Galeri foto per hobi dalam bentuk grid
  - Lightbox — foto bisa diklik untuk dilihat lebih besar
- **Tanpa dependency berat** — hanya load Google Fonts (Baloo 2 & Quicksand) dari CDN

## 📁 Struktur folder yang disarankan

```
linktree-teh/
├── index.html          ← rename dari linktree-teh.html
├── about-me.html
└── assets/
    ├── profil.png
    ├── icon-gaming.png
    ├── icon-anime.png
    ├── icon-draw.png
    ├── ml1.jpg, ml2.jpg, ml3.jpg
    ├── sky2.jpg, sky3.jpg, sky4.jpg
    ├── eren.png, law.jpg, daisuke.png
    └── gambar1.jpg, gambar2.JPG, gambar3.JPG
```

Kalau foto-fotomu ditaruh di folder `assets/`, sesuaikan path `src`-nya, misalnya:
```html
<img src="assets/profil.png" alt="Foto profil Teamoeba" />
```

## 🔧 Cara Kustomisasi

### 1. Ganti foto & ikon
Semua gambar saat ini pakai placeholder dari [placehold.co](https://placehold.co). Cari setiap tag `<img src="...">` dan ganti dengan path foto kamu sendiri (file lokal atau link online).

### 2. Ganti link tujuan
Di `linktree-teh.html`, tiap kartu punya atribut `href`:
```html
<a class="link-card" href="https://youtube.com/@namamu" target="_blank" rel="noopener">
```
Ganti URL-nya sesuai tujuan (YouTube, WhatsApp, donasi, dll).

### 3. Ganti teks
Judul, bio, dan deskripsi hobi ada langsung di HTML sebagai teks biasa — tinggal edit sesuai kebutuhan.

### 4. Ganti warna tema
Semua warna diatur lewat CSS custom properties di `:root`, jadi cukup ubah di satu tempat:
```css
:root{
  --bg-top:#F7E3CE;
  --bg-bottom:#EFC9A8;
  --brown:#6B4226;
  --matcha:#8CA772;
  --honey:#E3A857;
  --clay:#C97B4A;
}
```

## 🚀 Cara Menjalankan

Tidak perlu instalasi apa pun — cukup buka file `.html` langsung di browser, atau:

- **GitHub Pages**: push repo ini, aktifkan Pages di Settings → set source ke branch utama, halaman langsung online di `https://username.github.io/nama-repo/`
- **Lokal**: klik dua kali file `linktree-teh.html`, atau jalankan local server sederhana:
  ```bash
  npx serve .
  ```

## 🛠️ Tech Stack

- HTML5 & CSS3 murni (custom properties, flexbox, grid, `clamp()`)
- Vanilla JavaScript (untuk accordion & lightbox di halaman About Me)
- [Google Fonts](https://fonts.google.com) — Baloo 2 & Quicksand

## 📄 Lisensi

Bebas dipakai dan dimodifikasi untuk kebutuhan pribadi.

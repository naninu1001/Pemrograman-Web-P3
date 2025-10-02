# Instagram Clone dengan Bootstrap 5

## 🎯 Deskripsi Proyek
Proyek ini adalah implementasi sederhana antarmuka Instagram menggunakan **Bootstrap 5**.  
Tujuan utamanya adalah memahami cara membuat layout web responsif dengan sistem grid Bootstrap, komponen siap pakai, dan CSS tambahan.

---

## 🚀 Fitur Utama
1. **Sidebar Desktop**
   - Dibuat dengan `position-fixed` dan `d-flex`.
   - Hanya tampil di layar besar (disembunyikan di mobile dengan `d-none d-md-flex`).

2. **Navbar bawah (mobile)**
   - Menggunakan `d-md-none` agar hanya tampil di layar kecil.
   - Ditempel ke bawah layar dengan `position-fixed bottom-0`.

3. **Header Profil**
   - Foto profil bulat menggunakan `rounded-circle`.
   - Bio menggunakan sistem grid (`row` dan `col`) agar rapih.

4. **Highlight Story**
   - Dibuat dengan CSS tambahan: `overflow-x: auto; white-space: nowrap;`.
   - Gambar bulat dengan `border-radius: 50%`.

5. **Feed Foto**
   - Grid responsif menggunakan sistem kolom Bootstrap:
     - `col-12` (mobile, 1 kolom)
     - `col-sm-6` (tablet kecil, 2 kolom)
     - `col-md-4` (tablet sedang, 3 kolom)
     - `col-lg-3` (laptop, 4 kolom)
   - Foto dijaga tetap kotak dengan CSS `aspect-ratio: 1/1` dan `object-fit: cover`.

---

## 📂 Struktur Kode
- **aside** → sidebar navigasi (desktop).
- **main** → konten utama (profil, highlight, feed).
- **div.row + col** → sistem grid feed foto.
- **nav (bawah)** → navigasi mobile.

---

## 📱 Responsivitas
- Bootstrap menggunakan sistem grid 12 kolom.
- Breakpoint Bootstrap:
  - `col-` → <576px
  - `col-sm-` → ≥576px
  - `col-md-` → ≥768px
  - `col-lg-` → ≥992px
  - `col-xl-` → ≥1200px

---

## 🎯 Alasan Pemilihan Bootstrap
- **Komponen siap pakai** → tombol, nav, grid.
- **Familiar** untuk banyak developer.
- **Dokumentasi lengkap** dan komunitas besar.
- Butuh **sedikit CSS tambahan** (contoh: highlight scroll, aspect-ratio).

---

## 📊 Perbandingan dengan Tailwind
| Fitur            | Tailwind                          | Bootstrap                              |
|------------------|----------------------------------|----------------------------------------|
| Grid Feed        | `grid-cols-1 sm:grid-cols-2 ...` | `col-12 col-sm-6 col-md-4 col-lg-3`    |
| Foto Kotak       | `aspect-square object-cover`     | CSS custom `aspect-ratio + object-fit` |
| Sidebar/Navbar   | `hidden md:flex` / `md:hidden`   | `d-md-none` / custom media query       |
| Styling          | Utility class langsung           | Komponen + utilitas (kadang extra CSS) |
| Kecepatan Dev    | Cepat & fleksibel                | Stabil & standar industri              |

---

## 📊 Kesimpulan
- Bootstrap lebih **standar & stabil**, cocok untuk proyek formal.
- Namun, untuk layout spesifik seperti feed Instagram, butuh **CSS tambahan** agar sama rapihnya dengan Tailwind.

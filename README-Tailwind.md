# Instagram Clone dengan TailwindCSS

##  Deskripsi Proyek
Proyek ini adalah implementasi sederhana antarmuka Instagram menggunakan **TailwindCSS**.  
Tujuan utamanya adalah memahami cara membuat layout web yang responsif dengan grid, flexbox, sidebar, navbar, dan elemen profil seperti di Instagram.

---

##  Fitur Utama
1. **Sidebar (desktop & tablet)**
   - Menggunakan class `hidden md:flex` → sembunyi di HP, tampil di layar ≥768px.
   - Berisi menu navigasi: Beranda, Cari, Jelajahi, Reels, Pesan, Notifikasi, Buat, Profil.

2. **Navbar bawah (khusus mobile)**
   - Menggunakan class `fixed bottom-0 w-full md:hidden`.
   - Muncul hanya di layar kecil (<768px).

3. **Header Profil**
   - Foto profil berbentuk bulat → `rounded-full border`.
   - Bio disusun dengan `flex` agar rapih di mobile & desktop.

4. **Highlight Story**
   - Menggunakan `overflow-x-auto` untuk bisa digeser horizontal.
   - Gambar bulat dengan border → mirip fitur "Highlight" Instagram.

5. **Feed Foto**
   - Grid responsif bawaan Tailwind:
     - `grid-cols-1` (mobile, 1 kolom)
     - `sm:grid-cols-2` (tablet kecil, 2 kolom)
     - `md:grid-cols-3` (tablet sedang, 3 kolom)
     - `lg:grid-cols-4` (laptop, 4 kolom)
   - Bentuk feed dijaga tetap kotak → `aspect-square object-cover`.

---

##  Struktur Kode
- **aside** → sidebar navigasi (desktop & tablet).
- **main** → konten utama (profil, highlight, feed).
- **section** → pembungkus setiap bagian (profil, highlight, feed).
- **nav (bawah)** → navigasi mobile.

---

##  Responsivitas
- Tailwind memanfaatkan **breakpoint** langsung di class:
  - `sm:` ≥640px
  - `md:` ≥768px
  - `lg:` ≥1024px
- Tidak perlu bikin CSS manual, cukup deklarasi di class.

---

##  Alasan Pemilihan Tailwind
- **Utility-first** → styling langsung di HTML.
- **Lebih presisi** untuk kontrol responsif.
- **Cocok untuk prototyping cepat**.
- **Minim CSS tambahan**, cukup pakai class bawaan.

---

##  Kesimpulan
- Versi Tailwind membuat feed lebih **mudah responsif** dan stabil di semua device.
- Class `aspect-square` sangat membantu menjaga konsistensi bentuk feed.
- Cocok dipakai kalau ingin proyek cepat dan fleksibel tanpa bikin CSS panjang.

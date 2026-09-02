# TopUpGame - Katalog Produk Responsif (Tugas Rutin 3)

## Cara jalanin
```
npm install
npm run watch   # auto rebuild pas lo edit index.html
```
Buka `index.html` di browser (double click, atau extension "Live Server" kalo pake VS Code).

## Checklist requirement — ini posisinya di mana

| Requirement | Ada di mana |
|---|---|
| 1. Mobile-first approach | Semua class ditulis default = tampilan HP dulu, breakpoint (`sm:` `md:` `lg:` `xl:`) baru nambahin/override buat layar lebih lebar. Lihat komentar di HTML. |
| 2. Minimal 3 breakpoint | Grid produk pake `sm` (640px), `lg` (1024px), `xl` (1280px) — itu 3 breakpoint tambahan di luar mobile. Navbar pake `md` (768px). |
| 3. Grid responsif 1→2→3/4 kolom | Section `#produk`: `grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4` — sekarang isinya 5 card (Valorant, PUBG Mobile, Blood Strike, Free Fire, Mobile Legends) |
| 4. Card produk (gambar+info+harga+btn) | Tiap `<article>` di grid produk |
| 5. Navbar responsif (hamburger di mobile) | `<header>` — tombol hamburger + `app.js` buat toggle |
| 6. Responsive images | Semua `<img>` pake `w-full aspect-square object-cover` — gambar di-crop otomatis biar penuh ngisi kotak persegi, jadi semua card konsisten satu ukuran di kolom manapun. |
| 7. `clamp()` buat typography (opsional) | Judul hero: `text-[clamp(1.75rem,5vw,3rem)]` — tetep dibiarin ada, gapapa dihapus kalo mau |
| 8. Footer | Paling bawah, section `#kontak` |
| 9. Dokumentasi testing | **Ini bagian lo kerjain sendiri, lihat panduan di bawah** |

## Cara bikin "Dokumentasi Testing (screenshot 3 breakpoint)"

Dosen biasanya minta bukti kalo halamannya beneran dites di beberapa ukuran layar. Caranya:

1. Buka `index.html` di Chrome.
2. Buka DevTools (`F12` atau klik kanan → Inspect).
3. Klik ikon device toggle (bentuknya kayak HP+tablet) di pojok kiri atas DevTools, atau tekan `Ctrl+Shift+M` (Windows/Linux) / `Cmd+Shift+M` (Mac).
4. Di dropdown ukuran layar (biasanya tulisan "Responsive"), coba 3 lebar ini (matching breakpoint yang dipake di project ini):
   - **375px** → tampilan mobile (1 kolom, hamburger muncul)
   - **768px** → tampilan tablet (2-3 kolom, navbar udah horizontal)
   - **1280px** → tampilan desktop (4 kolom penuh)
5. Screenshot tiap ukuran (`Ctrl+Shift+P` → ketik "screenshot" → pilih "Capture screenshot", atau screenshot manual pake tools OS lo).
6. Susun 3 screenshot itu di dokumen (Word/Google Docs/slide), kasih label ukuran layarnya, terus itu jadi dokumentasi testing lo.

## Ganti produk / harga

Semua card ada di bagian `<section id="produk">` di `index.html`. Tinggal copy salah satu `<article>...</article>`, ganti nama game, harga, dan link gambar di `src="https://placehold.co/..."` (ganti teks setelah `?text=` buat ganti tulisan di gambar placeholder-nya, atau ganti jadi foto produk asli kalo udah punya).

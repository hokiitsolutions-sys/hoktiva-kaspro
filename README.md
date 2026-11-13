# HOKTIVA KasPro — PWA untuk GitHub Pages

Paket ini disiapkan untuk repository GitHub `hoktiva-kaspro`.

## Isi paket
- `index.html` — HTML HOKTIVA KasPro dari revisi beranda terakhir.
- `manifest.webmanifest` — nama, ikon, dan konfigurasi instalasi PWA.
- `service-worker.js` — cache app shell dan fallback navigasi offline.
- `icons/` — ikon 192×192 dan 512×512.
- `.nojekyll` — menonaktifkan pemrosesan Jekyll pada GitHub Pages.

## Upload ke GitHub
1. Unduh dan ekstrak ZIP ini di komputer.
2. Buka repository `hoktiva-kaspro` pada GitHub.
3. Pilih branch `main`.
4. Hapus file lama di repository (cadangkan dahulu jika masih diperlukan).
5. Upload seluruh ISI folder hasil ekstrak ke root repository, bukan folder induknya.
6. Commit ke branch `main`.
7. Buka **Settings → Pages**.
8. Pada **Build and deployment**, pilih **Deploy from a branch**.
9. Pilih branch `main`, folder `/(root)`, lalu **Save**.
10. Tunggu deployment selesai, kemudian buka URL GitHub Pages yang diberikan GitHub.

## PWABuilder
Masukkan URL HTTPS GitHub Pages ke https://www.pwabuilder.com/ setelah situs berhasil dibuka.

## Catatan penting tentang offline
Service Worker ini menyimpan app shell dan aset lokal pada kunjungan pertama. Namun HTML sumber saat ini masih memanggil Tailwind CSS, Font Awesome, dan Google Fonts dari CDN eksternal. Karena itu, tampilan penuh tanpa internet belum dapat dijamin pada cold start atau cache yang dibersihkan. Perlu tahap lanjutan untuk mengemas CSS/font eksternal secara lokal dan menguji semua fitur offline sebelum menyatakan offline penuh.

PWA/TWA juga membutuhkan situs HTTPS yang dapat dijangkau saat instalasi dan verifikasi. GitHub Pages menyediakan HTTPS tanpa perlu membeli domain sendiri.

## Versi
- App version: 1.0.0
- Build: 1 (Preview)

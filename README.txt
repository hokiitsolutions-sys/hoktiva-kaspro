# HOKTIVA KasPro PWA

Paket Progressive Web App dari file HTML sumber. Ikon aplikasi memakai gambar HOKTIVA KasPro yang diberikan.

## Isi paket
- `index.html` — aplikasi utama (logika aplikasi dipertahankan).
- `manifest.webmanifest` — nama, warna, mode standalone, dan ikon instalasi.
- `service-worker.js` — cache app shell dan aset yang berhasil dimuat agar dapat dibuka kembali secara offline.
- `icons/` — ikon 192x192, 512x512, dan maskable.

## Menjalankan / memasang
1. Upload seluruh isi folder ini ke hosting yang mendukung HTTPS (misalnya GitHub Pages). Jangan hanya meng-upload `index.html`.
2. Buka alamat HTTPS tersebut di Chrome Android.
3. Pilih menu **Install app / Tambahkan ke layar utama**.

Untuk uji lokal, jalankan server web dari folder ini (jangan membuka `index.html` dengan `file://`). Contoh Python: `python -m http.server 8080`, lalu buka `http://localhost:8080`.

## Catatan offline
Service worker menyimpan halaman dan aset lokal serta menyimpan aset CDN/font setelah berhasil dimuat saat online. Karena Tailwind, Font Awesome, dan Google Fonts pada HTML sumber masih memakai CDN, lakukan pembukaan pertama saat online agar aset tersebut masuk cache. Fitur yang memerlukan WhatsApp atau layanan eksternal tetap memerlukan internet. Data aplikasi yang disimpan melalui localStorage tetap berada di browser/perangkat yang memasangnya; PWA ini tidak otomatis menyinkronkan data antarperangkat.

## Versi
Cache service worker: `hoktiva-kaspro-v1`. Naikkan nama versi tersebut saat memperbarui aset agar cache lama diganti.

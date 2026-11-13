# HOKTIVA KasPro — GitHub Pages + PWABuilder

## Upload ke GitHub
1. Buat repository baru bernama `hoktiva-kaspro` (Public).
2. Ekstrak ZIP ini.
3. Upload seluruh ISI folder proyek ke root repository (pastikan `index.html` berada di root).
4. Commit ke branch `main`.
5. Buka tab **Actions** dan tunggu workflow **Deploy HOKTIVA KasPro PWA to GitHub Pages** selesai dengan status hijau.
6. Buka **Settings → Pages**. Source harus **GitHub Actions**.
7. URL aplikasi akan berbentuk `https://USERNAME.github.io/hoktiva-kaspro/`.

## Buat APK dengan PWABuilder
1. Buka https://www.pwabuilder.com/
2. Masukkan URL GitHub Pages di atas.
3. Tekan **Start** / **Build My PWA**.
4. Pilih **Android** → **Package for Stores** atau opsi Android yang tersedia.
5. Isi nama aplikasi `HOKTIVA KasPro`, package ID `com.hoktiva.kaspro`, lalu buat paket.
6. Unduh hasil Android yang disediakan PWABuilder. Jika yang dihasilkan AAB, gunakan opsi APK jika tersedia atau build/sign sesuai petunjuk PWABuilder.

## Catatan
- File HTML aplikasi asli dipertahankan; perubahan hanya menambahkan manifest PWA, service worker, dan referensi ikon lokal.
- Aplikasi menggunakan localStorage browser untuk data. Data tersimpan pada perangkat/browser yang digunakan dan tidak otomatis tersinkron antarperangkat.
- Beberapa tampilan memuat Tailwind CDN, Font Awesome CDN, dan Google Fonts; koneksi internet diperlukan untuk memuat aset eksternal tersebut.
- Uji aplikasi di URL HTTPS GitHub Pages sebelum membuat paket Android.

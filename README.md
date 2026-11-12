# NexaBuild

Ubah proyek menjadi APK atau AAB lewat GitHub Actions, langsung dari HP. Gratis, tanpa server, dan berjalan di akun GitHub-mu sendiri.

## Cara pakai
1. Buka aplikasi, tekan ikon menu, lalu hubungkan GitHub dengan personal access token (classic, scope `repo` dan `workflow`).
2. Di tab **Build**, pilih sumber proyek: unggah file ZIP atau HTML, tempel URL (situs web, repo Git, atau link ZIP), atau mulai dari nol.
3. Periksa identitas aplikasi (terisi otomatis dari proyek), atur kustomisasi, lalu tekan **Build**.
4. Unduh APK dari Ringkasan hasil, atau dari tab Riwayat.

## Yang didukung
Flutter, Capacitor, React Native / Expo, Gradle Android (Kotlin dan Java), situs web (HTML, Vite, React, Vue), WebView dari URL, dan aplikasi dasar.

## Privasi
Token hanya disimpan di perangkatmu (localStorage) dan hanya dikirim ke `api.github.com`. Build berjalan di repo `apk-builder` milikmu, sehingga menit Actions dan hasil build adalah milikmu. Tombol **Putuskan** menghapus token dari perangkat.

## Struktur
- `index.html`, `css/app.css`, `js/*.js`: aplikasi (tanpa proses build, tanpa dependensi npm)
- `js/template.js`: salinan generator yang dipasang otomatis ke repo `apk-builder`
- `manifest.json`, `sw.js`, `icons/`: PWA

## Batasan
Python/Kivy dan Unity tidak didukung. ZIP maksimal 50 MB (untuk proyek lebih besar pakai URL repo). Repo privat membutuhkan secret `SRC_TOKEN` di repo build.

# Kokurikulum SK Rimba Terjun

Laman GitHub Pages untuk sistem pelaporan kokurikulum SK Rimba Terjun.

| Alamat | Isi |
|---|---|
| https://koku-skrt.github.io/ | Menu utama |
| https://koku-skrt.github.io/mingguan/ | e-Laporan Mingguan Kokurikulum |
| https://koku-skrt.github.io/program/ | Sistem ePelaporan Kokurikulum (Laporan Program) |

Setiap halaman `mingguan/` dan `program/` membenamkan web app Google Apps Script dalam satu skrin penuh
supaya banner "This application was created by a Google Apps Script user" tidak dipaparkan.

- Untuk tukar web app, ubah nilai `WEB_APP_URL` dalam `mingguan/index.html` atau `program/index.html`.
- Web app mesti menggunakan `setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)` dalam `doGet`,
  dan memanggil `window.top.postMessage({ type: 'elaporan-koku-ready' }, '*')` bila borang siap dimuatkan.

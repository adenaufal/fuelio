# Roadmap (Development)

## 0.1 — Stabilitas & UX
- [ ] Tambah state “saving error” untuk quota/localStorage gagal (toast + retry).
- [ ] Confirm dialog khusus saat hapus (bukan `confirm()`), dengan undo 5 detik.
- [ ] Improve tooltip & helper copy untuk pengguna non-teknis.
- [ ] Audit aksesibilitas: focus trap dialog, ARIA live untuk pesan error/sukses.

## 0.2 — Data & Ekspor
- [ ] Ekspor CSV via data URI (tanpa impor).
- [ ] Opsi backup/restore JSON (manual download/upload) jika aman.
- [ ] Sorting/filter: rentang tanggal, pencarian catatan.

## 0.3 — Visual & Grafik
- [ ] Tren konsumsi (Canvas) dengan smoothing sederhana.
- [ ] Mode “dense list” untuk layar kecil + opsi compact card.
- [ ] Animasi ringan untuk tambah/edit/hapus.

## 0.4 — PWA & Perangkat
- [ ] Badge/notification ringan (misal pengingat isi full-tank) jika diizinkan.
- [ ] Optimasi offline: versi cache dengan busting yang jelas.
- [ ] Dukungan instalasi iOS (ikon, splash metadata).

## 0.5 — Input Jarak yang Lebih Mudah (tanpa API key)
- [ ] Otomasi parsing teks Maps: auto-detect pola “km” di clipboard saat dialog terbuka.
- [ ] Bookmarklet/extension desktop untuk menyalin jarak dari maps.google.com ke clipboard dengan 1 klik.
- [ ] Peningkatan helper mobile: instruksi singkat copy-paste dari app Maps.

## 0.6 — (Opsional, butuh API key)
- [ ] Endpoint jarak/rute (Google Directions atau OpenRoute) berdasar link yang ditempel.
- [ ] Cache hasil rute untuk hemat kuota; fallback ke input manual jika gagal.***

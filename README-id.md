# Fuel Tracker PWA

PWA sederhana untuk mencatat konsumsi BBM motor dengan metode full-tank. Seluruh aplikasi ada di satu `index.html` (inline CSS/JS, tanpa dependensi eksternal) dan bekerja offline dengan LocalStorage + service worker.

## Fitur Utama
- Catat/edit/hapus entri: jarak tempuh, liter BBM, tanggal, catatan (opsional).
- Hitung rasio otomatis (km/L), dengan warna indikator (hijau/kuning/merah) pada kartu riwayat.
- Header statistik: rata-rata, terbaik, terburuk, total km/L.
- Persisten lokal (LocalStorage) + cache-first service worker, dark mode mengikuti sistem.
- Bantuan jarak: buka Google Maps dari form, lalu “Tempel & Isi” untuk mengisi jarak dari clipboard (atau tempel manual).
- Validasi inline (tidak boleh 0/negatif, batas angka) dan guard “Invalid” jika pembagian nol.

## Cara Pakai (MVP)
1) Buka `index.html` di browser (bisa diinstal sebagai PWA).  
2) Klik tombol `+` untuk membuka form.  
3) Isi jarak (pakai helper peta untuk menempel jarak dari Google Maps jika perlu), isi liter BBM, tanggal, dan catatan opsional.  
4) Simpan. Riwayat dan statistik akan muncul dan tersimpan lokal.  
5) Tap kartu untuk edit; tahan lama untuk hapus.

## Struktur Data (LocalStorage)
```json
{
  "entries": [
    {
      "id": "timestamp_rand",
      "date": "2025-11-21",
      "distance": 55,
      "fuel": 12,
      "ratio": 4.58,
      "notes": "full throttle test",
      "timestamp": 1763683200000
    }
  ],
  "settings": { "darkMode": "auto", "language": "id" }
}
```

## Pengembangan
- Tidak ada build step: cukup edit `index.html`.  
- Service worker dan manifest di-inline (Blob).  
- Untuk reset data lokal, hapus kunci `fuelTrackerData` di DevTools (Application/Storage).

## Batasan
- Tidak menarik jarak otomatis dari link Google Maps tanpa API; gunakan salin-tempel.  
- Clipboard baca perlu gesture pengguna dan izin browser; jika gagal, tempel manual lalu klik “Isi”.  
- Tidak ada sinkronisasi cloud atau impor CSV.***

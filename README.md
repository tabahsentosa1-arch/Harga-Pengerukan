# Harga Pengerukan (Android)

Aplikasi Android yang membungkus `perhitungan_harga_pengerukan.html` (offline, tanpa izin internet).

## Cara mendapat APK (tanpa Android Studio)

1. Buat repositori baru di github.com (boleh privat).
2. Unggah **seluruh isi folder ini** (termasuk folder `.github`) ke repositori, cabang `main`.
   Cara mudah: di halaman repo pilih "Add file" > "Upload files", lalu seret semua isi folder.
   Pastikan folder `.github/workflows/build-apk.yml` ikut terunggah.
3. Buka tab **Actions**. Workflow "Build APK" jalan otomatis (sekitar 3-6 menit).
   Jika tidak jalan, pilih "Build APK" > "Run workflow".
4. Setelah centang hijau, buka run tersebut, lalu unduh **HargaPengerukan-APK** di bagian Artifacts (berisi `app-debug.apk` dalam ZIP).
5. Salin APK ke HP dan pasang. Izinkan "Pasang dari sumber tidak dikenal" bila diminta.

## Catatan
- Ini APK debug (ditandatangani kunci debug). Cukup untuk pemakaian pribadi/internal, tidak untuk Play Store.
- Android minimum: 10 (API 29).
- Isi aplikasi ada di `app/src/main/assets/index.html`. Ganti file itu lalu push ulang untuk memperbarui APK.
- Dua perubahan kecil dibanding HTML asli, agar berfungsi di WebView:
  tombol Ekspor CSV menyimpan ke folder Download, dan tombol Cetak membuka dialog cetak/simpan PDF Android.
  Di browser biasa, perilakunya tetap seperti semula.

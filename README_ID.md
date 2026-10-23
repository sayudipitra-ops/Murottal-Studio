# Murottal Studio — Proyek Android awal

Proyek sumber awal untuk aplikasi Android pembuat video murottal Reels.

## Fitur pada prototipe
- UI Android berbasis WebView.
- Memuat daftar 114 surah dan teks/terjemahan dari API online.
- Pilihan qari online (ID edisi audio dapat berbeda menurut ketersediaan penyedia).
- Background visual bawaan berbasis SVG yang ikut disertakan di aplikasi.
- Pratinjau vertikal 9:16.
- Tombol ekspor video prototipe berbasis browser MediaRecorder; dukungan ekspor audio/video bergantung pada versi WebView dan dukungan CORS penyedia audio.

## Penting
Ini adalah **proyek sumber/prototipe**, bukan APK yang sudah dikompilasi atau diuji. Untuk menghasilkan APK:
1. Buka folder proyek di Android Studio.
2. Pastikan Android SDK dan Gradle tersedia.
3. Sinkronkan Gradle.
4. Build > Build Bundle(s) / APK(s) > Build APK(s).

API dan audio memerlukan internet. Verifikasi teks Al-Qur'an dan kecocokan audio sebelum menerbitkan konten. Periksa ketentuan penggunaan/atribusi setiap penyedia. Background SVG lokal boleh digunakan sebagai aset visual aplikasi.

## Data online
Prototipe menggunakan endpoint publik api.alquran.cloud untuk data surah dan ayat. Ketersediaan ID qari/audio perlu diuji dan dapat berubah.


## Build otomatis dari HP dengan GitHub Actions
1. Buat repository baru di GitHub melalui browser HP.
2. Unggah seluruh isi ZIP ini ke repository (pastikan folder `.github/workflows/android-build.yml` ikut terunggah).
3. Buka tab **Actions**, pilih **Build Murottal Studio APK**, lalu tekan **Run workflow** bila workflow belum berjalan otomatis.
4. Tunggu job selesai dengan status hijau.
5. Buka hasil run dan unduh artifact `murottal-studio-debug-apk`. Ekstrak ZIP artifact untuk mendapatkan `app-debug.apk`.

Catatan: build pertama bisa gagal jika versi Android Gradle Plugin/SDK atau konfigurasi proyek perlu penyesuaian. Workflow ini belum membuktikan bahwa aplikasi sudah berhasil dibangun atau diuji. APK debug bukan APK rilis bertanda tangan untuk distribusi luas.

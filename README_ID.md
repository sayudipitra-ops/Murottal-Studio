# Murottal Studio — Proyek Android

**Penting:** Ini kode sumber/prototipe, bukan APK siap instal dan belum diuji pada perangkat nyata. APK dicoba dibangun melalui GitHub Actions.

## Isi proyek
- `app/` — kode aplikasi Android dan aset.
- `build.gradle`, `settings.gradle`, `gradle.properties` — konfigurasi Gradle.
- `.github/workflows/android-build.yml` — otomatisasi build APK di GitHub Actions.

## Upload lewat HP
1. Unduh ZIP ini lalu ekstrak.
2. Di GitHub, buka repository `Murottal-Studio` → **Add file** → **Upload files**.
3. Upload isi folder `MurottalStudio_Project`, bukan file ZIP-nya. Pastikan folder `app` beserta isinya ikut terunggah.
4. Folder `.github` diawali titik dan mungkin disembunyikan File Manager. Aktifkan **Tampilkan file tersembunyi / Show hidden files** dan pastikan `.github/workflows/android-build.yml` ikut terunggah.
5. Setelah upload, buka tab **Actions**. Pilih workflow **Build Murottal Studio APK** dan jalankan **Run workflow** jika belum berjalan otomatis.
6. Jika build berhasil, buka hasil run dan unduh artifact `murottal-studio-debug-apk`.

Catatan: build belum dijamin berhasil; jika GitHub Actions menampilkan error, perlu diperbaiki berdasarkan log error tersebut.


## Catatan Gradle Wrapper

Proyek ini tidak membutuhkan file `gradlew` atau folder `gradle/wrapper` untuk workflow GitHub Actions yang disertakan. Workflow memasang Gradle 8.9 di runner GitHub, lalu menjalankan `gradle --no-daemon assembleDebug`. Pastikan folder `.github/workflows` ikut diunggah agar workflow tersedia.

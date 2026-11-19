# Padu Releases

Repo publik khusus rilis APK Padu. Aplikasi Padu mengecek rilis terbaru
di sini tiap dibuka (`api.github.com/repos/bg-dw/padu-releases/releases/latest`)
dan mengunduh APK dari asset rilis.

## Cara merilis versi baru

1. Naikkan `versionCode` dan `versionName` di `app/build.gradle.kts` di repo `bg-dw/padu`, lalu build APK.
2. Buat rilis dengan tag `vX.Y.Z`, lampirkan APK, dan tulis baris pertama
   catatan rilis sebagai `versionCode: N`:

```bash
gh release create v0.3.0 --repo bg-dw/padu-releases \
  --title "Padu v0.3.0" \
  --notes "versionCode: 3
- Update via GitHub Releases" \
  app-debug.apk
```

Kode aplikasi Padu tetap private di `bg-dw/padu`; repo ini hanya berisi APK rilis.

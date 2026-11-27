# Panduan Instalasi Aplikasi Native iOS — Celenganku & Devide FF (Rp 0 / Gratis)

Paket ini adalah proyek **Capacitor iOS** lengkap yang membungkus aplikasi **Celenganku & Devide FF** menjadi aplikasi iOS native (`.ipa`) dengan penyimpanan permanen internal iOS (`@capacitor/preferences`).

## Mengapa Versi Ini Aman & Tidak Perlu Dibuka Rutin?
1. **Penyimpanan Native Permanen:** Data tabungan, target, dan portofolio saham disimpan langsung di memori internal iOS (`UserDefaults` via `@capacitor/preferences`), bukan *cache* browser Safari—sehingga **data tidak akan pernah terhapus** walau aplikasi tidak dibuka selama berbulan-bulan.
2. **Tanpa Biaya (Rp 0):** Anda bisa membangun file `.ipa` secara gratis menggunakan **GitHub Actions** (tanpa perlu punya Mac) dan menginstalnya ke iPhone menggunakan **SideStore** (gratis, tanpa komputer setelah instalasi awal).
3. **Auto-Refresh Sertifikat Otomatis (Tanpa Buka Aplikasi):** Dengan bantuan aplikasi bawaan **Shortcuts (Pintasan)** di iPhone, SideStore akan memperpanjang sertifikat aplikasi secara otomatis di latar belakang setiap 3–5 hari saat iPhone terhubung ke Wi-Fi.

---

## Langkah 1: Membuat File `.ipa` (Pilih Salah Satu Cara)

### Cara A: Tanpa Mac (Gratis via GitHub Actions Cloud)
1. Buat akun gratis di [github.com](https://github.com) dan buat *repository* baru (misalnya `celenganku-ios`, boleh diatur ke **Private**).
2. Unggah seluruh isi folder `capacitor_ios_project` ini (termasuk folder `.github` dan `www`) ke *repository* tersebut.
3. Buka tab **Actions** di GitHub → pilih workflow **Build Unsigned iOS IPA** → klik **Run workflow**.
4. Tunggu sekitar 3–5 menit hingga selesai, lalu unduh file **`Celenganku-DevideFF-unsigned.ipa`** di bagian **Artifacts**.

### Cara B: Jika Anda Memiliki Mac (Xcode)
1. Buka Terminal di dalam folder `capacitor_ios_project`, jalankan:
   ```bash
   npm install
   npx cap add ios
   npx cap sync ios
   npx cap open ios
   ```
2. Di Xcode, hubungkan iPhone dengan kabel, pilih **Signing & Capabilities** → masukkan Apple ID pribadi Anda pada bagian **Team**, lalu tekan tombol **Play (Run)**.

---

## Langkah 2: Instal di iPhone Tanpa Kabel & Auto-Refresh (SideStore — Rp 0)
1. Pasang **SideStore** di iPhone Anda (panduan resmi tersedia di [sidestore.io](https://sidestore.io) — hanya butuh PC/Mac sekali di awal untuk pemasangan SideStore).
2. Buka aplikasi **SideStore** di iPhone → masuk ke tab **My Apps** → ketuk ikon **`+`** di pojok kiri atas → pilih file **`Celenganku-DevideFF-unsigned.ipa`**.
3. Aplikasi **Celenganku FF** langsung terpasang di *Home Screen* iPhone Anda!

### Mengaktifkan Auto-Refresh Agar Tidak Perlu Dibuka Rutin:
1. Buka aplikasi bawaan **Shortcuts (Pintasan)** di iPhone → pilih tab **Automation (Automasi)** di bagian bawah.
2. Ketuk **`+`** → pilih **Time of Day (Waktu Hari)** (misal pukul `08:00`, ulangi setiap hari atau tiap 3 hari) → pilih **Run Immediately (Jalankan Segera)**.
3. Pilih aksi **Refresh All Apps** dari aplikasi **SideStore**.
4. Selesai! Selama iPhone terhubung ke Wi-Fi, sertifikat aplikasi akan terus diperpanjang otomatis di latar belakang tanpa biaya dan tanpa perlu Anda buka secara rutin.

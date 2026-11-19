# 0157_LaSanteCoffeeRoasters

**La Sante Coffee Roasters** adalah aplikasi mobile Android berbasis **Kotlin** dan **100% Jetpack Compose** dengan arsitektur **MVVM** untuk membantu operasional kedai kopi (UMKM), mulai dari pengelolaan kategori produk, menu kopi, data pelanggan, pencatatan pesanan, hingga catatan harian kasir.

## Teknologi yang Digunakan
- **Bahasa & UI:** Kotlin, 100% Jetpack Compose (Material Design 3)
- **Arsitektur:** MVVM (*Model-View-ViewModel*)
- **Navigasi:** Navigation Compose
- **Autentikasi & Otorisasi:** JWT (*Access Token* & *Refresh Token*) + *Role-Based UI* (`Admin` & `Kasir`)
- **Jaringan & Database:** Retrofit (REST API + JSON Parsing) & MySQL (Tanpa Room Database)
- **Penyimpanan Lokal:** Internal File Storage (`context.filesDir` untuk membaca & menulis catatan harian/struk lokal)

## Entitas Data Utama (5 Tabel Berelasi)
1. `users` — Data akun pegawai beserta peran (`admin` / `kasir`) dan *refresh token*.
2. `kategori` — Kategori produk kedai kopi (misal: *Espresso Based*, *Manual Brew*, *Non-Coffee*).
3. `menu_kopi` — Daftar menu kopi beserta harga dan relasi ke `kategori`.
4. `pelanggan` — Data pelanggan kedai kopi beserta kontak.
5. `pesanan` — Pencatatan transaksi pesanan yang terhubung ke `users`, `pelanggan`, dan `menu_kopi`.

## Checklist 10 Persyaratan Wajib Project Akhir
- [ ] **1. Authentication:** Login & Register dengan Access Token (JWT) dan Refresh Token
- [ ] **2. Authorization:** Role-Based UI (`Admin/Owner` akses penuh; `Kasir` akses pesanan, pelanggan, & catatan)
- [ ] **3. Navigasi & Routing:** Multi-page menggunakan Navigation Compose
- [ ] **4. State Management:** Arsitektur MVVM (`ViewModel` + `StateFlow`)
- [ ] **5. Tabel / Data:** 5 Entitas data utama saling berelasi & *field* dinamis
- [ ] **6. Features (5 CRUDS Penuh):**
    - [ ] CRUDS Kategori Produk
    - [ ] CRUDS Daftar Menu Kopi
    - [ ] CRUDS Data Pelanggan
    - [ ] CRUDS Transaksi Pesanan
    - [ ] CRUDS Catatan Harian Kasir / Struk (File Lokal)
- [ ] **7. REST API Integration:** Request & parsing JSON menggunakan Retrofit
- [ ] **8. Database:** MySQL Server (tanpa Room Database)
- [ ] **9. File Storage:** Simpan & baca file lokal (`.txt`/`.json`) di `filesDir`
- [ ] **10. UI/UX:** Desain Material 3 matang, 100% Jetpack Compose

## Laporan Progres Mingguan (Minimal 30 Commit Bertahap)

| Minggu        | Target Fitur & Pekerjaan | Status | Keterangan Commit |
|:--------------| :--- | :--- | :--- |
| **Minggu 1**  | Setup Repo, `README.md`, Tema UI, & Data Class Model | Proses | Commit 1–5 |
| **Minggu 2**  | UI Formulir & Daftar (Kategori, Menu, Pelanggan, Pesanan) | Belum | Commit 6–12 |
| **Minggu 3**  | Implementasi MVVM (`ViewModel`) & Navigation Compose | Belum | Commit 13–18 |
| **Minggu 4**  | Fitur CRUDS ke-5 & File Storage Lokal (`filesDir`) + Role-Based UI | Belum | Commit 19–22 |
| **Minggu 5**  | Setup Database MySQL & Backend REST API + JWT | Belum | Commit 23–26 |
| **Minggu 6**  | Integrasi Retrofit, Access/Refresh Token JWT, & Testing Akhir | Belum | Commit 27–32 |
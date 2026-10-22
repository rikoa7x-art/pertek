# Pertek TRS - Sistem Desain & Pemetaan Jaringan Pipa Air Bersih

Aplikasi web interaktif untuk pemetaan, perencanaan teknis (Pertek), dan penggambaran jaringan pipa distribusi air bersih dengan latar belakang Google Maps, katalog pipa PVC/HDPE berwarna per diameter, aksesoris jaringan air bersih, notasi panah petunjuk (*leader callout*), kalkulasi BOQ (*Bill of Quantities*), serta lembar keluaran cetak ber-Kop Gambar (*Etiket*) standar PDAM / Dinas PUPR format A3/A4 Landscape.

---

## 🌟 Fitur Utama

1. **Peta Dasar Google Maps Interaktif:**
   - Google Maps Roadmap (Jalan)
   - Google Maps Satelit Hybrid (Citra Satelit + Nama Jalan)
   - Google Maps Satelit Murni
   - Google Maps Terrain (Kontur & Medan)
   - Google Maps Traffic (Lalu Lintas Real-time)
   - Fitur pencarian lokasi (nama tempat atau koordinat Lat, Lng).

2. **Katalog Pipa & Warna Pembeda Diameter:**
   - **Pipa PVC (AW):** Standar JIS/SNI dari diameter 1/2" (20 mm) hingga 12" (315 mm).
   - **Pipa HDPE (PE-100):** Standar SDR 11/17 (OD) dari OD 25 mm (3/4") hingga OD 500 mm (20").
   - Tiap diameter memiliki kode warna pembeda kontras tinggi sesuai standar teknik.

3. **Pengaturan Gaya & Ketebalan Garis (*Line Style & Weight*):**
   - **Gaya Garis:** Solid (menerus), Dot (titik-titik melingkar), dan Dash (putus-putus).
   - **Ketebalan Garis:** Slider kustom 2 px – 22 px dengan opsi `Auto Ø` (mengikuti standar tebal diameter).
   - Pratinjau garis interaktif real-time.

4. **Katalog Aksesoris & Fitting Jaringan Pipa (12 Item):**
   - Gate Valve (Katup Sorong)
   - Air Valve (Katup Pelepas Udara)
   - Check Valve (Katup Satu Arah)
   - Pressure Reducing Valve / PRV (Pengurang Tekanan)
   - Water Meter Induk
   - Pilar Hidran Kebakaran
   - Tee Branch & Reducer Tee
   - Reservoir / Bak Penampung Air
   - Pompa Distribusi (Booster Pump)
   - Elbow Fitting (Tikungan 90° / 45°)
   - Clamp Saddle (Sambungan Rumah)
   - Washout / Penguras Endapan Pipa

5. **Notasi Keterangan Jalur Pipa dengan Tanda Panah (*Leader Callout*):**
   - Tanda panah penunjuk (*leader arrow*) langsung mengarah ke garis pipa.
   - Kotak notasi dapat digeser (*drag*) agar tidak menutupi objek lain di peta, dengan garis petunjuk yang dinamis.
   - Teks notasi dapat diedit secara manual atau dikembalikan ke format otomatis standar.

6. **Smart Snapping & Vertex Editing:**
   - Kursor otomatis menempel (*snap*) pada ujung pipa, percabangan, dan aksesoris.
   - Titik lekukan pipa (*vertex*) dapat digeser atau dihapus dengan klik kanan untuk merevisi rute.

7. **Rekapitulasi Material (BOQ) & Ekspor Excel:**
   - Perhitungan otomatis total panjang pipa per material dan per diameter (meter dan km).
   - Perhitungan total jumlah unit masing-masing tipe aksesoris yang terpasang.
   - Ekspor data rekapitulasi ke file CSV (Excel) dengan 1 klik.

8. **Lembar Gambar Kerja & Kop Gambar (Etiket Standar PU / PDAM):**
   - Format standar gambar kerja teknik landscape (rasio A3 / A4).
   - Kop gambar memuat Logo Instansi Resmi, Keterangan Potongan Melintang Galian Pipa (*Trench*), Tabel Standar Kedalaman Galian Bina Marga, Legenda Diameter, Nama Kegiatan & Pekerjaan, Lokasi, Judul Gambar, Kolom Pengesahan 3 Pejabat (Pemeriksa, Mengetahui, Mengesahkan), Tanggal, Skala, dan Nomor Lembar.
   - Fitur **Skala Auto** untuk menyesuaikan skala teknik gambar secara otomatis berdasarkan tingkat pembesaran (*zoom level*) peta.
   - Semua data Kop dapat diedit melalui modal editor dan tersimpan di penyimpanan lokal (*localStorage*).
   - Fitur cetak langsung ke printer atau simpan sebagai PDF beresolusi vektor.

9. **Penyimpanan Format GeoJSON & Auto-Save:**
   - Fitur **Auto-Save otomatis** setiap 30 detik ke browser `localStorage` dengan prompt pemulihan cerdas saat halaman dibuka kembali.
   - Simpan seluruh proyek jaringan pipa, aksesoris, kustomisasi notasi, dan data kop ke file `.geojson`.
   - Buka kembali file proyek kapan saja (*Import GeoJSON*).

10. **Produktivitas & Fitur Modern Terbaru:**
    - **Sistem Undo / Redo Global (Ctrl+Z / Ctrl+Y):** Membatalkan dan mengulang aksi penggambaran pipa, pemasangan fitting, pengeditan, atau penghapusan elemen.
    - **Panel Panduan Keyboard Shortcut (? / F1):** Bantuan interaktif ringkas seluruh pintasan keyboard langsung di layar.
    - **Sistem Notifikasi Toast Elegan:** Pengganti pop-up alert yang halus dan tidak memblokir interaksi pengguna.
    - **Mini-Map (Peta Inset Navigasi):** Peta kecil di pojok kanan bawah untuk navigasi cepat dan orientasi area.
    - **Bilah Sisi Responsif (Collapsible Sidebar):** Sidebar dapat disembunyikan/ditampilkan dengan tombol toggle atau shortcut `B`.
    - **Mode Tampilan Gelap & Terang (Dark / Light Mode):** Pilihan tema dengan penyimpanan preferensi otomatis.
    - **Salin Koordinat (1-Click Copy Lat, Lng):** Tombol cepat untuk menyalin koordinat kursor ke clipboard.
    - **Pencarian Cerdas & Riwayat:** Pencarian tempat otomatis mengingat riwayat pencarian sebelumnya.
    - **Statistik Header Real-time:** Penghitung segmen pipa, aksesori, dan total panjang jaringan secara langsung di topbar.

---

## 🚀 Cara Menjalankan Secara Lokal

Aplikasi ini bersifat *standalone* tanpa memerlukan server backend atau build tools tambahan (seperti Node/Webpack):

1. Unduh atau clone repository ini:
   ```bash
   git clone https://github.com/rikoa7x-art/pertek.git
   ```
2. Buka file `index.html` langsung di browser favorit Anda (Google Chrome, Microsoft Edge, Firefox, dll.).

---

## 🌐 Menjalankan Melalui GitHub Pages (Live Online)

Untuk mengaktifkan website ini agar dapat diakses oleh siapa saja secara online via browser:

1. Buka repository [rikoa7x-art/pertek](https://github.com/rikoa7x-art/pertek) di GitHub.
2. Masuk ke menu **Settings** > **Pages** (di bilah kiri).
3. Pada bagian **Build and deployment** > **Branch**:
   - Pilih branch `main` (atau `master`).
   - Pilih folder `/ (root)`.
   - Klik **Save**.
4. Dalam 1-2 menit, aplikasi akan aktif dan dapat diakses di:
   ```
   https://rikoa7x-art.github.io/pertek/
   ```

---

## 📁 Struktur File

```
pertek/
├── index.html       # Aplikasi utama (HTML, CSS, JS terintegrasi)
├── logo.jpg         # Logo resmi Perumda Air Minum Tirta Rangga Kab. Subang
├── logo.jpeg        # Cadangan logo
├── lib/             # Pustaka pemetaan lokal (Leaflet.js, Leaflet.css, icon)
│   ├── leaflet.js
│   ├── leaflet.css
│   └── images/
├── README.md        # Dokumentasi aplikasi
└── .gitignore       # Konfigurasi file yang diabaikan Git
```

---

*Dikembangkan untuk efisiensi perencanaan teknis jaringan pipa air bersih.*

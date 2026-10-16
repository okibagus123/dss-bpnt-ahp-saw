# 🏛️ Sistem Pendukung Keputusan (SPK) Kombinasi AHP & SAW Calon Penerima BPNT

Sistem berbasis web (*PHP Native*) yang dikembangkan untuk menentukan peringkat dan menyeleksi calon penerima Bantuan Pangan Non-Tunai (BPNT) secara objektif dan akurat di tingkat kelurahan (Studi Kasus: Kelurahan Pekelingan). 

Sistem ini menerapkan metode hibrida **Analytic Hierarchy Process (AHP)** untuk pembobotan kriteria berbasis penilaian multi-pakar (*Multi-Expert*) dan **Simple Additive Weighting (SAW)** untuk perankingan alternatif penerima bantuan.

---

## 🚀 Fitur Unggulan

* **Manajemen Kriteria Dinamis:** Pengelolaan kriteria penilaian utama seperti Penghasilan, Usia, Tanggungan Keluarga, dan Kondisi Rumah.
* **Pendekatan Multi-Expert (Responden):** Mendukung penginputan dan pengelolaan penilaian dari banyak pakar/responden (perangkat desa, pekerja sosial, tokoh masyarakat).
* **Agregasi Geomean:** Menggabungkan matriks perbandingan berpasangan dari seluruh pakar menggunakan metode *Geometric Mean* (Rata-rata Geometrik).
* **Uji Konsistensi AHP:** Perhitungan otomatis nilai $\lambda_{max}$, *Consistency Index* (CI), dan *Consistency Ratio* (CR) untuk memastikan validitas penilaian pakar (Standar $CR < 0.1$).
* **Perankingan SAW:** Melakukan normalisasi matriks keputusan dan mengalikannya dengan bobot prioritas AHP untuk menghasilkan nilai preferensi akhir bagi setiap alternatif.
* **Impor Data Excel:** Fitur unggulan untuk mengimpor data alternatif warga secara massal menggunakan pustaka `PhpSpreadsheet`.

---

## 🛠️ Tech Stack & Metode

* **Bahasa Pemrograman:** PHP (Native / OOP)
* **Basis Data:** MySQL (PDO Connection)
* **Frontend:** Tailwind CSS (Modern & Responsive UI)
* **Library Eksternal:** PhpSpreadsheet (Excel Parsing)
* **Metode Analisis:** 
  1. *Analytic Hierarchy Process (AHP)* – Bobot Kriteria
  2. *Geometric Mean (GEOMEAN)* – Agregasi Multi-Pakar
  3. *Simple Additive Weighting (SAW)* – Perankingan Alternatif

---

## 📊 Kriteria Penilaian
Sistem memproses beberapa kriteria utama penyeleksian:
1. **C1 (Penghasilan):** Tingkat pendapatan bulanan keluarga.
2. **C2 (Usia):** Faktor usia kepala keluarga / penerima.
3. **C3 (Tanggungan Keluarga):** Jumlah anggota keluarga yang menjadi tanggungan.
4. **C4 (Kondisi Rumah):** Penilaian fisik kelayakan tempat tinggal.

---

## ⚙️ Cara Instalasi Lokal

1. Clone repositori ini ke dalam direktori `htdocs` XAMPP Anda:
   ```bash
   git clone [https://github.com/okibagus123/dss-bpnt-ahp-saw.git](https://github.com/okibagus123/dss-bpnt-ahp-saw.git)

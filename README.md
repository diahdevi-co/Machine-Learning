# Dokumentasi Tugas Magang — MACHINE-LEARNING

**Versi:** 1.0
**Tanggal:** 2025-12-18

## 1. Ringkasan Eksekutif

Dokumentasi ini bertujuan untuk menyajikan instruksi formal dan langkah-langkah reproduksi hasil yang dibuat selama pelaksanaan tugas magang pada proyek machine learning (gaya Home Credit). Dokumen mencakup tujuan tugas, ruang lingkup, prasyarat lingkungan, langkah reproduksi eksperimen, format keluaran, dan panduan penyerahan.

## 2. Tujuan Magang

- Membangun pipeline pra-pemrosesan data dan model prediksi risiko kebangkrutan nasabah menggunakan dataset Home Credit.
- Menghasilkan file submission yang sesuai dengan format kompetisi untuk evaluasi (mis. `submission_lgb.csv`).
- Menerapkan praktik yang dapat direproduksi, terdokumentasi dengan baik, serta menjaga privasi data sensitif.

## 3. Ruang Lingkup Tugas

- Analisis dan pra-pemrosesan dataset (missing values, feature engineering).
- Pelatihan model LightGBM untuk prediksi probabilitas default.
- Evaluasi model menggunakan metrik yang relevan (contoh: AUC-ROC) pada data validasi.
- Pembuatan file submission sesuai format kompetisi.

## 4. Struktur Repository

- `CODE/` — Notebook dan skrip (contoh: `data_prep.ipynb`, `lightgbm_modeling.ipynb`)
- `DATA/` — Tempat menaruh dataset yang diunduh (tidak disertakan dalam repo)
- `OUTPUT/` — Hasil keluaran seperti `submission_lgb.csv`
- `requirements.txt` — Daftar dependency Python

## 5. Prasyarat

- Sistem operasi: Windows / Linux / macOS
- Python 3.9+ direkomendasikan
- Dependensi: lihat `requirements.txt`
- Akun Kaggle dan akses ke kompetisi Home Credit untuk mengunduh dataset

## 6. Cara Mendapatkan Data

Data asli tidak disertakan di repository karena pembatasan distribusi. Unduh dataset resmi dari halaman kompetisi:

https://www.kaggle.com/competitions/home-credit-default-risk/code

Setelah diunduh, taruh file CSV yang diperlukan ke folder `DATA/` (misal `application_train.csv`, `application_test.csv`, `bureau.csv`, dll.).


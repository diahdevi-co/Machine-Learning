# MACHINE-LEARNING

Repository ini berisi Jupyter notebook dan skrip untuk proyek machine learning (gaya Home Credit).

> ⚠️ Data asli **disembunyikan** dari repository. Anda dapat mengakses dan mengunduh dataset resmi dari kompetisi Kaggle berikut:
>
> https://www.kaggle.com/competitions/home-credit-default-risk/code

## Struktur proyek

- `CODE/` - Notebook dan skrip untuk pra-pemrosesan dan modelling
- `DATA/` - Folder untuk menempatkan file CSV dataset yang Anda unduh dari Kaggle (tidak disertakan di repo)
- `OUTPUT/` - Hasil keluaran, mis. `submission_lgb.csv`

## Cara mendapatkan data 🔒

1. Kunjungi halaman kompetisi di Kaggle: [Home Credit - Default Risk (Kaggle)](https://www.kaggle.com/competitions/home-credit-default-risk/code)
2. Bergabung/ikuti kompetisi lalu unduh file dataset (mis. `application_train.csv`, `application_test.csv`, `bureau.csv`, dll.)
3. Letakkan file-file CSV hasil unduhan ke dalam folder `DATA/` di root repository.

## Detail Proyek — Data, Tujuan, & Hasil 📄

### Data — isi utama
- **`application_train.csv` / `application_test.csv`**: data pelanggan (demografi, pekerjaan, pendapatan, dll.) dan fitur utama untuk prediksi kredit.
- **`bureau.csv`**: ringkasan riwayat kredit nasabah dari lembaga lain.
- **`bureau_balance.csv`**: histori status tagihan terkait entri pada `bureau.csv`.
- **`previous_application.csv`**: riwayat aplikasi kredit sebelumnya oleh pemohon.
- **`installments_payments.csv`**: catatan pembayaran cicilan untuk aplikasi tertentu.
- **`POS_CASH_balance.csv`**, **`credit_card_balance.csv`**: data saldo dan perilaku penggunaan kredit pada transaksi ritel dan kartu kredit.

> Keterangan: file-file di atas merupakan bagian dari dataset kompetisi dan **tidak disertakan** dalam repository; unduh dari halaman kompetisi Kaggle (link tersedia di atas).

### Tujuan
- Membangun pipeline pra-pemrosesan dan model prediksi **probabilitas default** (risiko gagal bayar) untuk nasabah baru.
- Menghasilkan model yang dapat dievaluasi secara reproducible (cross-validation) dan siap menghasilkan file submission untuk kompetisi/penilaian.
- Menerapkan praktik dokumentasi, versioning dependencies, dan menjaga kerahasiaan data.

### Hasil yang dihasilkan
- **File submission**: `OUTPUT/submission_lgb.csv` (format sesuai kompetisi; kolom contoh: `SK_ID_CURR`, `TARGET`).
- **Model artefak**: model yang dilatih (mis. LightGBM), catatan hyperparameter, serta skor evaluasi (mis. mean AUC-ROC pada CV).
- **Notebook & logs**: notebook terurut di `CODE/` (`data_prep.ipynb`, `lightgbm_modeling.ipynb`) yang menjelaskan langkah pra-pemrosesan, fitur, dan evaluasi.

> Catatan: Nilai metrik (mis. AUC-ROC) dan kualitas model dapat bervariasi tergantung strategi feature engineering, pemilihan hyperparameter, dan seed random. Semua keluaran utama disimpan di folder `OUTPUT/`.

## Setup lingkungan (singkat) 🔧

1. Buat virtual environment:
   - venv (Windows):
     ```powershell
     python -m venv .venv
     .\.venv\Scripts\activate
     ```
   - Conda:
     ```bash
     conda create -n ml-env python=3.10
     conda activate ml-env
     ```

2. Install dependensi:
   ```bash
   pip install -r requirements.txt
   ```

3. Jalankan JupyterLab dan buka notebook di `CODE/`:
   ```bash
   jupyter lab
   ```

## Catatan penting 💡

- Jangan commit file dataset (`DATA/`) ke repository publik.
- Untuk reproduksibilitas, pertimbangkan untuk **men-pin versi** paket di `requirements.txt` atau membuat `environment.yml` untuk Conda.

---

Jika Anda mau, saya dapat:
- Membuat `environment.yml` untuk Conda, atau
- Mem-pin versi paket di `requirements.txt`, atau
- Menambahkan `CONTRIBUTING.md` dan `LICENSE`.

Beritahu saya opsi mana yang Anda inginkan.
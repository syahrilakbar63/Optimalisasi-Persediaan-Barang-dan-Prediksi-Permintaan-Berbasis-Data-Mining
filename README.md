# Optimalisasi Persediaan Barang dan Prediksi Permintaan Berbasis Data Mining

Proyek ini menggunakan metode regresi linear untuk memprediksi permintaan barang berdasarkan data penjualan dari Favorita stores di Ekuador. Data penjualan historis dan informasi tambahan seperti harga minyak, transaksi harian, dan hari libur digunakan untuk melatih model prediksi. Hasil prediksi diharapkan dapat membantu dalam mengoptimalkan persediaan barang di masa depan.

## Dataset
Dataset yang digunakan berasal dari kompetisi [Kaggle Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data).

### Deskripsi File:
- **train.csv:** Data penjualan historis.
- **test.csv:** Data untuk prediksi.
- **stores.csv:** Informasi mengenai toko.
- **oil.csv:** Harga minyak harian.
- **holidays_events.csv:** Informasi mengenai hari libur dan acara.
- **transactions.csv:** Data transaksi harian.

## Langkah-langkah Analisis:
1. Mengimpor Libraries yang Dibutuhkan
2. Membaca Dataset
3. Pra-Pemrosesan Data
4. Eksplorasi Data
5. Menggabungkan Data
6. Feature Engineering
7. Membangun Model Regresi Linear
8. Melakukan Prediksi dan Evaluasi Model
9. Menggunakan Model untuk Memprediksi Data Uji

## Hasil
Proyek ini menghasilkan prediksi penjualan yang dapat digunakan untuk mengoptimalkan persediaan barang. Evaluasi model menggunakan Mean Squared Error (MSE) dan R-squared (R2) menunjukkan kinerja model yang memadai untuk tujuan prediksi ini.

## Penggunaan
1. Jalankan setiap cell dalam Jupyter Notebook secara berurutan.
2. File `submission.csv` yang dihasilkan dapat digunakan untuk mengirim prediksi Anda.
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

## Langkah-langkah
1. **Mengimpor Libraries yang Dibutuhkan:** Mengimpor pustaka yang diperlukan seperti pandas, numpy, matplotlib, seaborn, dan sklearn.
2. **Membaca Dataset:** Membaca file dataset menggunakan `pd.read_csv()`.
3. **Pra-Pemrosesan Data:** Mengonversi kolom 'date' menjadi tipe datetime dan mengisi nilai yang hilang pada data oil dengan metode forward fill.
4. **Eksplorasi Data:** Melakukan visualisasi data penjualan untuk melihat tren penjualan dari waktu ke waktu.
5. **Menggabungkan Data:** Menggabungkan dataset tambahan seperti oil, transactions, dan stores ke dalam dataset utama.
6. **Feature Engineering:** Menambahkan fitur-fitur baru yang berguna seperti hari, bulan, tahun, dan hari dalam minggu dari kolom 'date'.
7. **Membangun Model Regresi Linear:** Membuat dan melatih model regresi linear menggunakan fitur yang telah dipilih.
8. **Melakukan Prediksi dan Evaluasi Model:** Melakukan prediksi menggunakan model yang telah dilatih dan mengevaluasi kinerjanya dengan metrik seperti Mean Squared Error dan R-squared.
9. **Menggunakan Model untuk Memprediksi Data Uji:** Melakukan pra-pemrosesan yang sama pada data uji dan menggunakan model untuk memprediksi nilai sales pada data uji. Hasil prediksi disimpan dalam file `submission.csv`.

## Penggunaan
1. Jalankan setiap cell dalam Jupyter Notebook secara berurutan.
2. File `submission.csv` yang dihasilkan dapat digunakan untuk mengirim prediksi.

## Hasil
Data dari `submission.csv` berisi hasil prediksi penjualan (`sales`) untuk setiap baris data uji (`test.csv`). Kolom `id` merujuk pada identitas unik dari setiap baris dalam data uji, dan kolom `sales` berisi nilai prediksi penjualan untuk baris tersebut.

### Penjelasan Hasil
- **id**: Identitas unik untuk setiap entri dalam data uji.
- **sales**: Nilai prediksi penjualan yang dihasilkan oleh model regresi linear.

### Analisis Hasil
- Nilai prediksi negatif menunjukkan bahwa model regresi linear perlu disesuaikan lebih lanjut atau menggunakan metode pemodelan yang lebih kompleks untuk menghindari hasil yang tidak realistis.
- Prediksi penjualan dapat digunakan untuk mengatur stok barang dengan lebih efisien, memastikan ketersediaan produk yang cukup, dan menghindari kelebihan atau kekurangan stok.

### Langkah Selanjutnya
- **Normalisasi Output**: Menerapkan fungsi aktivasi seperti ReLU (Rectified Linear Unit) pada output model untuk memastikan semua prediksi non-negatif.
- **Penambahan Fitur**: Mempertimbangkan penambahan fitur baru yang relevan yang dapat mempengaruhi penjualan.
- **Pemilihan Model Alternatif**: Menggunakan model machine learning lain seperti Decision Trees, Random Forests, atau metode deep learning yang mungkin lebih cocok untuk data ini.

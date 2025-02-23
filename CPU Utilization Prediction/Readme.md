# Panduan Penggunaan

## 1. TechnicalTest\_DA\_LNK.ipynb

### Deskripsi

Notebook ini berfungsi untuk memproses data, melatih model forecasting, mengevaluasi performa model, dan menyimpan model hasil training yang nantinya digunakan di notebook **Forecasting\_System\_LNK.ipynb** untuk melakukan prediksi penggunaan CPU bulan Desember.

### Cara Menggunakan

1. Jalankan setiap sel satu per satu untuk memproses data.
2. Notebook akan membersihkan dan menyiapkan data sebelum pelatihan model.
3. Beberapa model forecasting akan diterapkan, dan hasil evaluasinya akan ditampilkan.
4. Model terbaik akan disimpan dan dapat diunduh untuk digunakan dalam notebook lain.

### Metode yang Digunakan

- **Simple Exponential Smoothing**: Metode smoothing untuk menangkap tren dalam data.
- **ARIMA (AutoRegressive Integrated Moving Average)**: Model statistik untuk forecasting data time-series.
- **SARIMAX (Seasonal ARIMA with Exogenous Variables)**: Perluasan ARIMA yang mempertimbangkan faktor musiman.
- **LSTM (Long Short-Term Memory)**: Model deep learning yang kuat untuk memprediksi data time-series.

### Evaluasi Model

Setiap model dievaluasi menggunakan metrik berikut:

- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**

---

## 2. Forecasting\_System\_LNK.ipynb

### Deskripsi

Notebook ini digunakan untuk melakukan forecasting terhadap tingkat penggunaan CPU server menggunakan model yang telah dilatih pada **TechnicalTest\_DA\_LNK.ipynb**.

### Cara Menggunakan

1. Pastikan model hasil training telah diunduh dari **TechnicalTest\_DA\_LNK.ipynb** dan tersedia untuk digunakan.
2. Jalankan setiap sel secara berurutan.
3. Model akan memprediksi tingkat penggunaan CPU per jam untuk periode 1-31 Desember 2023.
4. Hasil prediksi akan ditampilkan dalam bentuk visualisasi dan disimpan dalam format `npy` untuk penggunaan selanjutnya.

### Metode yang Digunakan

- **LSTM Model**: Model deep learning berbasis jaringan saraf untuk analisis data time-series.
- **S-Curve Fitting**: Pendekatan non-linear untuk menangkap pola pertumbuhan progresif.

---


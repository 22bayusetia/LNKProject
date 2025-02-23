# Panduan Penggunaan dan Penjelasan

## 1. TechnicalTest_DA_LNK.ipynb

### Deskripsi

Notebook ini berfungsi untuk memproses data, melatih model forecasting, mengevaluasi performa model, dan menyimpan model hasil training yang nantinya digunakan di notebook **Forecasting_System_LNK.ipynb** untuk melakukan prediksi penggunaan CPU bulan Desember.

### Cara Menggunakan

1. Jalankan setiap sel satu per satu untuk memproses data.
2. Notebook akan membersihkan dan menyiapkan data sebelum pelatihan model.
3. Beberapa model forecasting akan diterapkan, dan hasil evaluasinya akan ditampilkan.
4. Model terbaik akan disimpan dan dapat diunduh untuk digunakan dalam notebook lain.

### Metode yang Digunakan

- **SARIMA (Seasonal AutoRegressive Integrated Moving Average)**: Model statistik yang mempertimbangkan faktor musiman dalam data time-series.
- **Moving Average**: Teknik perataan data historis untuk menangkap tren dalam data time-series.
- **S-Curve Trend Model**: Model non-linear yang digunakan untuk menangkap pola pertumbuhan progresif.
- **LSTM (Long Short-Term Memory)**: Model deep learning berbasis jaringan saraf yang kuat dalam menganalisis data time-series.

### Evaluasi Model

Setiap model dievaluasi menggunakan metrik berikut:

- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **Root Mean Square Error (RMSE)**

---

## 2. Forecasting_System_LNK.ipynb

### Deskripsi

Notebook ini digunakan untuk melakukan forecasting terhadap tingkat penggunaan CPU server menggunakan model yang telah dilatih pada **TechnicalTest_DA_LNK.ipynb**.

### Cara Menggunakan

1. Pastikan model hasil training telah diunduh dari **TechnicalTest_DA_LNK.ipynb** dan tersedia untuk digunakan.
2. Jalankan setiap sel secara berurutan.
3. Model akan memprediksi tingkat penggunaan CPU per jam untuk periode 1-31 Desember 2023.
4. Hasil prediksi akan ditampilkan dalam bentuk visualisasi dan disimpan dalam format `npy` untuk penggunaan selanjutnya.

---

## Penjelasan Hasil Analisis
### Tahap Persiapan --> TechnicalTest_DA_LNK.ipynb
* Data yang tersedia tidak memiliki missing value.
* Terdapat 4 data outliers, akan tetapi berapa dalam rentang angka yang masuk akal (1-100). Selain itu, tidak ada keterangan mengenai data ourlier tersebut, sehingga saya asumsikan bahwa data tersebut merupakan peristiwa yang normal dan natural. Oleh karenanya, saya tetap menyertakan data outlier dalam analisis.
* Time Series Chart menunjukkan adanya lonjakkan penggunaan yang dimulai pada bulan Mei. Adanya peristiwa ini menyebabkan pemilihan metode forecasting harus lebih spesifik.
![Time Series Chart](https://drive.google.com/uc?export=view&id=1k6ZO1CRjRX9DoY-oc5Fg90uZouP4LSgI)
* Langkah persiapan selanjutnya membagi data yang sudah dimiliki (Januari-November) menjadi data training dan testing; training 80%, testing 20%.
* Setelahnya dilakukan training model dengan 4 metode yang sudah dijelaskan. Berikut ringkasan hasil evaluasi model yang dihasilkan:
<table>
    <tr>
        <th>Metriks</th>
        <th>SARIMA</th>
        <th>Moving Average</th>
        <th>S-curved Trend Model</th>
        <th>LSTM</th>
    </tr>
    <tr>
        <td>MSE</td>
        <td>44.88457267678008</td>
        <td>27.511286933828732</td>
        <td>26.610715112311755</td>
        <td>25.961660385131836</td>
    </tr>
    <tr>
        <td>RMSE</td>
        <td>6.69959496363624</td>
        <td>5.24512029736485</td>
        <td>5.158557464283184</td>
        <td>5.095258618081307</td>
    </tr>
    <tr>
        <td>MAD</td>
        <td>5.5656533338088945</td>
        <td>3.5356422505307847</td>
        <td>3.6763420581820117</td>
        <td>3.488595485687256</td>
    </tr>
</table>



Terlihat bahwa LSTM memiliki hasil evaluasi yang terbaik dibandingkan dengan metode lainnya.
* Setelahnya dilakukan visualisasi forecast data testing (yang dibandingkan dengan data asli)
![Visualisasi Forecast Data Testing](https://drive.google.com/uc?export=view&id=1oQlwHlFTU4i_6ocJecn6OtU5GgNFOZVn)

**Pengerjaan tugas Store Transaction saya lakukan di Tableau yang dapat diakses melalui link berikut:**


[**Dashboard Transaksi Penjualan**](https://public.tableau.com/app/profile/bayusetia/viz/StoreTransactionInsights/DashboardTransaksiPenjualan)

**Preview**:
![**Dashboard Transaksi Penjualan**](https://drive.google.com/uc?export=view&id=1KdQ-uMBkmdKinafFGcId-uaphzDS6KMb)
_Data awal yang disediakan memiliki 26 missing balue pada customer_province, yang mana bisa dilakukan imputasi dengan melihat customer_city. Oleh karenanya, data yang digunakan dalam analisis ini merupakan data setelah dilakukan imputasi setelah dilakukan research asal provinsi customer_city yang ternyata merupakan kelurahan/kecamatan yang ada di Kalimantan Utara._

---

## Pembahasan Hasil Analisis
1. Time Series Chart menunjukkan tren penjualan yang terus naik. Fluktuasi terjadi, namun dapat dilihat bahwa tren utama sejak awal tahun 2022 hingga Desember 2023 terus menunjukkan kenaikan.  
![Tren Penjualan](https://drive.google.com/uc?export=view&id=186dVO3Mhq3Ci0c4M6N9UhGRI-2hgl1Q2)
- Tren kenaikan ini dapat dimanfaatkan untuk meningkatkan stok produk di periode high-demand.
- Analisis lebih lanjut pada titik-titik fluktuasi dapat membantu memahami faktor-faktor yang mempengaruhi kenaikan dan penurunan, misalnya musim, promosi, atau faktor eksternal lainnya.
- Dapat dilakukan perencanaan kampanye pemasaran yang lebih agresif pada periode yang cenderung mengalami kenaikan penjualan.

---

2. Visualisasi Segmentasi Pelanggan menunjukkan distribusi penjualan berdasarkan customer_segment. Grafik ditujukan untuk mengetahui pelangan dengan pembelian terbanyak. Adanya filter menurut provinsi juga akan memungkinkan tersampaikannya informasi pelanggan setia tiap-tiap daerah. Sebagai contoh, berikut merupakan pelanggan dengan sales value tertinggi di Jawa Timur:  
![Segmentasi Pelanggan](https://drive.google.com/uc?export=view&id=1nHT3dzdG5jHdYss0b8qPMtEX2_Nmu-Ww)
- Dengan mengetahui pelanggan terbesar di setiap provinsi, tim sales dapat menerapkan strategi personalisasi, seperti program loyalitas atau penawaran khusus bagi pelanggan top-tier.
- Provinsi dengan pelanggan loyal yang tinggi dapat menjadi target utama dalam peluncuran produk baru atau strategi pemasaran yang lebih fokus.
- Jika ada provinsi dengan kontribusi rendah, dapat dilakukan analisis lebih lanjut untuk memahami hambatan dan peluang pertumbuhan di wilayah tersebut.

---
 
3. Ada pula visualisasi Segmentasi Pelanggan berdasarkan Customer Segmen yang menunjukkan penjualan tertinggi berasal dari segmen pelanggan National Account.  
![Segmentasi Pelanggan](https://drive.google.com/uc?export=view&id=12RnYzwzLVwSioUb_F_0LcyZVIf50RrIv)
- Mengingat National Account adalah penyumbang terbesar, maka strategi retensi pelanggan seperti diskon eksklusif atau layanan premium dapat meningkatkan loyalitas mereka.
- Peluang ekspansi dapat difokuskan pada segmen lain yang saat ini memiliki kontribusi lebih rendah, misalnya dengan penyesuaian harga atau strategi pemasaran yang lebih spesifik untuk segmen tersebut.
- Evaluasi hubungan dengan pelanggan di segmen utama perlu dilakukan secara berkala untuk menjaga kestabilan kontribusi mereka terhadap total penjualan.

---

4. Visualisasi Analisis Produk menunjukkan bahwa Produk 1 memiliki penjualan tertinggi dibandingkan dengan produk lain. Salah satu faktor yang mungkin menjadi penyebab adalah harga yang lebih terjangkau. Produk 1 merupakan ~80% daari total penjualan yang ada.  
Selain itu, adanya filter menurut provinsi juga akan memungkinkan didapatkannya informasi produk terlaris di setiap daerah, yang mana Produk 1 tetap menjadi favorit di banyak wilayah.  
![Analisis Produk](https://drive.google.com/uc?export=view&id=13QAwY_jzQpkpdeBWigj8hZnZtORYgrAH)  
- Produk 1 yang mendominasi pasar menunjukkan peluang untuk mempertimbangkan diversifikasi produk terkait atau paket bundling guna meningkatkan nilai pembelian pelanggan.
- Analisis lebih dalam terhadap margin keuntungan Produk 1 perlu dilakukan, apakah kontribusi terhadap profit sebanding dengan volume penjualannya.
- Untuk meningkatkan penjualan produk lain, dapat diterapkan strategi cross-selling atau bundling dengan Produk 1.

---

5. Distribusi Penjualan berdasarkan Provinsi dapat digunakan untuk melihat provinsi mana yang menjadi penyumbang terbanyak atas total sales dari store dari waktu ke waktu dengan adanya filter rentang waktu.  
![Analisis Produk](https://drive.google.com/uc?export=view&id=1HRgrAvsXekbMX2kFdZ_s-6se6ko3S1px)  
- Provinsi dengan kontribusi tinggi dapat menjadi prioritas untuk ekspansi gudang atau pusat distribusi guna meningkatkan efisiensi pengiriman.
- Jika ada provinsi dengan pertumbuhan lebih lambat dibandingkan daerah lain, maka strategi pemasaran lokal atau promosi khusus dapat diterapkan untuk meningkatkan penetrasi pasar.
- Memantau perubahan distribusi penjualan dapat membantu mengantisipasi kebutuhan stok di berbagai daerah dan menghindari masalah keterlambatan pengiriman.
 

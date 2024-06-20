# Marketing-Campaign-Customer-Analysis-using-Machine-Learning


## Overview

Sebuah perusahaan dapat berkembang dengan pesat saat mengetahui perilaku customer personality nya, sehingga dapat memberikan layanan serta manfaat lebih baik kepada customers yang berpotensi menjadi loyal customers. Dengan mengolah data historical marketing campaign guna menaikkan performa dan menyasar customers yang tepat agar dapat bertransaksi di platform perusahaan, dari insight data tersebut fokus kita adalah membuat sebuah model prediksi kluster sehingga memudahkan perusahaan dalam membuat keputusan 

## Objective

1. Melakukan eksplorasi data historis marketing campaign untuk memahami distribusi, outliers, dan pola-pola penting serta visualisasi data untuk mengidentifikasi tren dan hubungan antar variabel.

2. Membuat dan memilih fitur-fitur relevan, menggunakan teknik transformasi dan standarisasi data, serta metode statistik untuk mengevaluasi pentingnya setiap fitur.

3. Mengimplementasikan algoritma clustering seperti K-Means dan mengevaluasi hasil clustering dengan metrik seperti silhouette score untuk memastikan kualitas dan akurasi klaster yang dihasilkan.


## EDA & Insight
![image](https://github.com/txtmeyen11/Marketing-Campaign-Customer-Analysis-using-Machine-Learning/assets/126081314/65d959a7-21e3-4a78-8336-5ab19d8009b2)

Variabel Conversion_Rate, yang merupakan hasil bagi antara ‘Response’ terhadap kampanye pemasaran dengan jumlah kunjungan ke situs web dalam sebulan ‘NumWebVisitsMonth’. Variabel ini memberikan gambaran tentang efektivitas kampanye dalam menghasilkan respons dari pengunjung situs.

![image](https://github.com/txtmeyen11/Marketing-Campaign-Customer-Analysis-using-Machine-Learning/assets/126081314/127821c6-ccd9-4c7f-93ef-726da608dcce)

Kelompok Dewasa memiliki tingkat konversi di antara 0,25 dan 0,3. Hal tersebut menunjukkan bahwa konversi dalam kelompok usia ini cukup stabil namun relatif lebih rendah dibandingkan kelompok lainnya.

Kelompok Muda menunjukkan tingkat konversi yang lebih tinggi, berada di atas 0,35 namun di bawah 0,4. Hal ini menandakan bahwa pelanggan muda lebih cenderung melakukan konversi dibandingkan kelompok usia lainnya.

Kelompok Lansia memiliki tingkat konversi yang berkisar antara 0,3 dan 0,35, sedikit lebih tinggi dibandingkan kelompok dewasa namun lebih rendah dibandingkan kelompok muda.

## Clustering

Analisis segmentasi customer akan menggunakan LRFM, yakni:

Length (L) : Mengukur durasi pelanggan sejak pertama kali berbelanja dalam sebuah market

Recency (R) : Mengukur waktu sejak transaksi terakhir pelanggan

Frequency (F): Mengukur seberapa sering pelanggan melakukan transaksi dalam periode waktu tertentu.

Monetary (M): Mengukur jumlah uang yang dihabiskan pelanggan selama periode waktu tertentu.

Fitur yang sesuai dalam metode segmentasi tersebut adalah:
L : Total_Day_Membership
R : Recency
F : total_purchases
M : total_spent

![image](https://github.com/txtmeyen11/Marketing-Campaign-Customer-Analysis-using-Machine-Learning/assets/126081314/3bc13054-8844-4e2d-a833-e3014bf1b875)

**Cluster 0: Low Value Customer**

590 Pelanggan (26.72%)

Cluster ini terdiri dari pelanggan yang menunjukkan nilai terendah berdasarkan berdasarkan hasil analisis clustering. Pelanggan dalam cluster ini memiliki masa keanggotaan yang lama dan cukup sering kembali, namun memiliki jumlah pembelian yang sedikit, frekuensi yang rendah, dan pengeluaran total yang minimal. Strategi yang dapat diambil untuk kelompok ini termasuk program loyalitas atau diskon untuk mendorong peningkatan pembelian

**Cluster 1: High Value Customer**

1254 Pelanggan (56.79%)

Cluster ini berisi pelanggan yang sangat bernilai, dengan masa keanggotaan yang panjang, sering kembali, melakukan repeat order, serta mengeluarkan uang dalam jumlah besar. Untuk kelompok ini, penawaran eksklusif, layanan prioritas, dan program penghargaan dapat membantu mempertahankan dan meningkatkan nilai mereka lebih lanjut.

**Cluster 2: Medium Value Customers**

364 Pelanggan (16.49%)

Pelanggan dalam cluster ini berada di antara dua kelompok sebelumnya. Mereka menunjukkan aktivitas pembelian yang stabil dengan pengeluaran yang moderat. Pelanggan dalam cluster ini juga memiliki masa keanggotaan yang panjang dan sering kembali, namun mereka mirip dengan Cluster 1 dalam hal perilaku pembelian dan pengeluaran.

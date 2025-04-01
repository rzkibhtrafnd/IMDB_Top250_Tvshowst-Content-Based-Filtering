# Laporan Proyek Sistem Rekomendasi

## 1. Project Overview (Ulasan Proyek)
**Latar Belakang:**  
Proyek ini bertujuan untuk mengembangkan sistem rekomendasi yang dapat membantu pengguna menemukan TV series atau film yang relevan berdasarkan data dari IMDB Top 250 TV Shows. Permasalahan utamanya adalah bagaimana memberikan rekomendasi yang akurat dengan menggabungkan informasi teks (seperti kategori, usia penonton, dan tipe konten) dan informasi numerik (seperti rating dan jumlah vote).

**Pentingnya Proyek:**  
Sistem rekomendasi ini sangat berguna dalam membantu pengguna mengatasi banyaknya pilihan dalam industri hiburan. Dengan rekomendasi yang tepat, pengguna dapat lebih mudah menemukan konten yang sesuai dengan preferensi mereka.

**Riset dan Referensi:**  
Pendekatan yang digunakan mengacu pada teknik content based filtering, dengan representasi teks menggunakan TF-IDF dan pengukuran kemiripan antar entitas menggunakan cosine similarity. Pendekatan ini didukung oleh beberapa referensi, salah satunya dari [Sumber Jurnal](https://pdf.sciencedirectassets.com/280203/1-s2.0-S1877050924X00174/1-s2.0-S1877050924031211/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEM%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJGMEQCIHo%2BkpxXemo1LVKfaEQ8jnODCFfzoNSvOb8fjgmHrQ1LAiB%2Fdy0poCK1eabNHpH4sJGLACEk6nWQX6KyWRGnruUyOSqxBQg3EAUaDDA1OTAwMzU0Njg2NSIMgUimvAIHi0CH65IfKo4FFthFFXbmEwJTmGsRJLM4v%2BPIIjjOjnJDhMNbHc1hxx%2B0U0PxVHmALkua%2Fro7Guc5RGv56GNjaEN0pwQI7mUeMGqBXd79RNYv31DoqHZdHNlOytmLD2kxhVELSDJDqmIceiuARdUdioBFPdyEvNfNTovBkxdjxZP5%2FLX%2FdOAYWAaYbYDx75iX%2FhMVJfKI%2FtMv9ihpmauK9proyHAEnIEDvelgAHKiIiXgz46y6QNu%2BKDxdlWiBXdys%2Bi9sHOhmgO3b6WYXYG8mthh86LjxTv7%2B%2FGw%2F9eupI7OYbpbYrp44gPS%2BueihfLQkqHG6%2Fu3oZYLXKmXMrF7BJa1NeLTW0P8kkowdymd%2Byf2gEhCGp5xkpsSwp4Qxl2gy5%2Bo9abdHJJPYzwQIuhalm4jOm8c1af6DDukXKvab8jlm0x7jNksKWYrvDo309VHLtAV3LawX22Mqfp7u4gfQ0Dp3YFgxi4J4IqJuMtq8EaAcE8q6vo8MWY2jfZ5CAqFl44BWuOnoYKFw9AaiWd5%2F4ZdT8Fo7wX4tZVcUyC0HPXF3RiHOa75eUlJcFMBJjfpr6QsEQAC%2B8GBg8fa9l6togUMR%2F6vRG6sOfYMwA8CngHFt5I9615HYUiIfsGhkXYtkXxbfNskgnwqiSqQbE1gAWV2o6dDadkElCnIfOLt71rqvAOF1eumLYw5m7InfJBNCwCDdggauI8PpHAQ%2BmVhSwhEKZQidPBj7ICe23nifO2SSyHsC6nYAiDQVtxeTvUH387DWmij6nR%2FCncvIgakQ1MZ4mfsUgX94bUdWHfppXxOlxIuqUMOJ5cfdVCmKNuev9rROYxeaXOXHI7FREUwJekJNJtiiFDxFwm6YY35qcegoelZ%2BPE%2FMNv5kb8GOrIBpzSUPVQ37yI5b6FxUleef%2ByeKBGVpWZ444XTrUvstfpcdvXhNAQU4lsYzcLu6BVvCvdPU%2BF1r%2BI8NE9KYUVpgi0rEN%2Bqx8ju6dU8kqBRYoJtwZdKK4dMNdn2N2lrx3b%2FE%2Bgw2xlbBplxWy3jZ6iGmvYybaE0kfHqM3i0HD201BnaZK69unlQz4q%2BMqvXulz7R7Vx%2FHsVrY0zz%2FIy52ygdAiaySXE0dDa%2BZJzlmoMzy8Vmg%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250326T225442Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTY4Y3JI7D7%2F20250326%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=6b2d1d562b75c7bf7d239a028684d66fa33b348d2d46cc15b10004d003657002&hash=f86130932dbe050d2f4004a94cb9f9cbf95a0b8ced2960724038ba0fc4891f0c&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1877050924031211&tid=spdf-dfa889ef-97d7-4306-ac5d-1aec02985b9a&sid=1a3204af2666844f4c89abc40a11cae723a7gxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&rh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=13025f5751025c01540308&rr=926a3b3cfef2b59f&cc=id.)

## 2. Business Understanding
**Problem Statement:**  
Bagaimana cara memberikan rekomendasi TV series atau film yang sesuai dengan preferensi pengguna berdasarkan dataset IMDB Top 250 TV Shows?

**Goals:**  
- Membangun sistem rekomendasi yang dapat mengeluarkan top-5 rekomendasi untuk setiap judul yang diminta.  
- Menyediakan analisis terkait performa rekomendasi dengan menggabungkan fitur teks dan numerik.

**Solution Approach:**  
Untuk mencapai goals tersebut, kami mengusulkan dua pendekatan:
- **Content Based Filtering:** Menggunakan fitur teks (kategori, usia, tipe konten) dan fitur numerik (rating, vote count) untuk menghitung kemiripan antar entitas.  
- **Collaborative Filtering:** (Untuk pengembangan lebih lanjut) Menggunakan data interaksi pengguna untuk memberikan rekomendasi berdasarkan preferensi pengguna lain.

Pendekatan yang telah diimplementasikan pada kode ini adalah content based filtering dengan kombinasi TF-IDF dan normalisasi numerik.

## 3. Data Understanding
**Deskripsi Dataset:**  
Dataset yang digunakan merupakan IMDB Top 250 TV Shows yang terdiri dari 250 entri. Setiap entri memiliki kolom-kolom berikut:
- **Title:** Judul TV series atau film.
- **Year:** Tahun rilis.
- **Total_episodes:** Jumlah episode (nilai numerik setelah dibersihkan).
- **Age:** Rating usia (misalnya, 15, Unknown, dsb).
- **Rating:** Rating rata-rata dari pengguna.
- **Vote_count:** Jumlah vote (dikonversi dari format yang mengandung 'K' atau 'M').
- **Category:** Kategori atau genre dari konten.

Dataset ini diunduh dari [Sumber Dataset](https://drive.google.com/uc?id=1Cwyn6wG6OSP_o2n3kXx-En7axj7JDmyq).

**Penjelasan Variabel/Fitur:**  
- **Title:** Nama konten yang dijadikan acuan untuk rekomendasi.  
- **Year:** Menunjukkan era pembuatan konten.  
- **Total_episodes:** Penting untuk membedakan antara serial dan film, serta memberikan gambaran durasi konten.  
- **Age:** Indikator usia penonton yang direkomendasikan.  
- **Rating:** Indikator kualitas konten berdasarkan penilaian pengguna.  
- **Vote_count:** Mengindikasikan popularitas konten.  
- **Category:** Kategori atau genre yang membantu mengklasifikasikan konten.

**Exploratory Data Analysis (EDA):**  
Analisis awal dilakukan dengan memvisualisasikan distribusi rating (menggunakan histogram) dan hubungan antara rating dengan vote count (menggunakan scatter plot). Hasil deskriptif juga ditampilkan untuk memberikan gambaran statistik nilai-nilai utama.

## 4. Data Preparation
**Teknik Data Preparation:**  
- **Pembersihan Nama Kolom:** Mengubah nama kolom `Titile` menjadi `Title` agar konsisten.  
- **Pembersihan Vote_count:** Menghapus tanda kurung, spasi, serta mengkonversi notasi 'K' dan 'M' ke dalam nilai numerik.  
- **Pembersihan Total_episodes:** Menghapus kata "eps" dan spasi, lalu mengkonversinya menjadi nilai integer.  
- **Penanganan Missing Value:** Mengisi nilai yang hilang pada kolom `Age` dengan 'Unknown'.

**Ekstraksi Fitur dan Penggabungan:**
- **Pembuatan Fitur Metadata:** Menggabungkan informasi dari kolom 'Category', 'Age', dan menambahkan label jenis konten (misalnya, "Series") sehingga didapat kolom 'Metadata'.
- **Ekstraksi Fitur Teks:** Mengubah teks pada kolom 'Metadata' menjadi vektor fitur menggunakan TF-IDF.
- **Normalisasi Fitur Numerik:** Fitur numerik 'Rating' dan 'Vote_count' dinormalisasi menggunakan 'MinMaxScaler'.
- **Penggabungan Fitur:** Fitur teks (TF-IDF) dan fitur numerik yang sudah dinormalisasi digabungkan dengan teknik sparse matrix (menggunakan hstack) untuk perhitungan cosine similarity.

**Alasan Penerapan:**  
Tahapan-tahapan ini dilakukan untuk memastikan bahwa data yang digunakan konsisten dan dapat diolah secara numerik maupun tekstual, sehingga meminimalkan error dalam proses modeling dan meningkatkan akurasi sistem rekomendasi.

## 5. Modeling and Result
**Pembuatan Sistem Rekomendasi:**  
Sistem rekomendasi dibangun dengan menggabungkan dua jenis fitur:
- **Fitur Teks:** Dibuat dari kolom `Metadata` yang merupakan penggabungan informasi `Category`, `Age`, dan penanda konten sebagai "Series" atau "Movie". Representasi teks dilakukan dengan menggunakan TF-IDF.
- **Fitur Numerik:** Meliputi `Rating` dan `Vote_count` yang dinormalisasi menggunakan MinMaxScaler.

Kedua fitur tersebut digabungkan dengan menggunakan teknik sparse matrix (hstack). Kemudian, cosine similarity digunakan untuk menghitung tingkat kemiripan antar entitas. Fungsi get_recommendations mengembalikan top-5 rekomendasi untuk judul input dengan mengecualikan judul itu sendiri.

**Output Rekomendasi:**
Hasil rekomendasi ditampilkan dalam bentuk tabel (melalui print statement) dan divisualisasikan dengan bar plot yang menunjukkan skor cosine similarity.


## 6. Evaluation
**Metrik Evaluasi:**  
Dalam proyek ini, cosine similarity digunakan untuk mengukur kemiripan antar entitas sebagai dasar rekomendasi. Namun, untuk evaluasi performa sistem rekomendasi secara kuantitatif, sebaiknya digunakan metrik relevansi seperti:
- **Precision:** Proporsi rekomendasi yang relevan dari total rekomendasi yang diberikan.
- **Recall@K:** Persentase item relevan yang berhasil direkomendasikan pada top-K.
- *NDCG@K (Normalized Discounted Cumulative Gain):* Mengukur kualitas urutan rekomendasi dengan memberikan diskon pada item yang relevan namun berada di posisi lebih rendah.

**Keterbatasan Data:**  
Ground truth untuk menentukan relevansi rekomendasi tidak tersedia dalam dataset IMDB Top 250 TV Shows. Oleh karena itu, evaluasi secara kuantitatif dapat dilakukan melalui:
- **Validasi Manual:** Menilai relevansi rekomendasi secara subjektif.
- **Data Interaksi Pengguna:** Mengumpulkan data klik, rating atau histori tontonan sebagai ground truth untuk evaluasi lebih lanjut.
- **Simulasi Ground Truth (Dummy):** Membuat ground truth dummy untuk pengujian awal metrik evaluasi, meskipun hasilnya tidak mencerminkan performa sebenarnya.


Contoh kode evaluasi dummy telah disediakan dalam Notebook untuk menghitung Precision dan Recall, namun perhitungan metrik yang sebenarnya memerlukan data relevansi yang valid.

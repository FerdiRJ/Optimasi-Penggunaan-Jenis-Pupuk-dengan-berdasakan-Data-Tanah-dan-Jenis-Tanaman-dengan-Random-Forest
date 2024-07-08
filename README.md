# Optimasi-Penggunaan-Jenis-Pupuk-dengan-berdasakan-Data-Tanah-dan-Jenis-Tanaman-dengan-Random-Forest
Proyek ini bertujuan untuk mengembangkan sistem rekomendasi jenis pupuk yang optimal berdasarkan analisis data tanah dan jenis tanaman dengan menggunakan berbagai algoritma klasifikasi machine learning. Fokus utama dari proyek ini adalah untuk mengatasi masalah ketidakseimbangan kelas dalam dataset dan meningkatkan akurasi prediksi untuk membantu petani memilih jenis pupuk yang tepat sesuai dengan kondisi tanah dan jenis tanaman yang akan ditanam.

## Algoritma dan Teknik yang Digunakan

Dalam proyek ini, beberapa algoritma klasifikasi telah diterapkan dan dibandingkan untuk menemukan pendekatan yang paling efektif, yaitu:

- **K-Nearest Neighbors (KNN)**: Algoritma berbasis instance yang digunakan untuk menentukan jenis pupuk berdasarkan kedekatan dengan data pelatihan.
- **Random Forest (RF)**: Algoritma ensemble yang membangun banyak pohon keputusan dan menggabungkan hasilnya untuk meningkatkan akurasi prediksi.
- **Multi-Layer Perceptron (MLP)**: Jaringan saraf tiruan dengan beberapa lapisan tersembunyi yang digunakan untuk memodelkan hubungan non-linear antara fitur dan kelas.
- **Oversampling dengan SMOTE (Synthetic Minority Over-sampling Technique)**: Teknik oversampling untuk menyeimbangkan distribusi kelas dalam dataset dengan menciptakan sampel sintetik untuk kelas minoritas.
- **Seleksi Fitur dengan Chi-Square (SelectKBest)**: Metode statistik untuk memilih fitur yang paling relevan dengan mengeliminasi fitur yang tidak relevan atau redundan.

## Hasil dan Pembahasan

Hasil eksperimen menunjukkan bahwa KNN dengan kombinasi resampling SMOTE dan seleksi fitur Chi-Square memberikan performa terbaik dibandingkan dengan Random Forest dan MLP. Berikut adalah ringkasan hasil yang diperoleh:

| **Algoritma** | **Data Asli** | **Resampling** | **Seleksi Fitur** | **Seleksi Fitur dan Resampling** |
|:------------:|:-------------:|:--------------:|:-----------------:|:-------------------------------:|
| **KNN**       | 0,96          | 0,93           | 0,95              | 0,90                            |
| **RF**        | 0,93          | 0,88           | 0,87              | 0,81                            |
| **MLP**       | 0,55          | 0,61           | 0,46              | 0,52                            |

Dari tabel di atas, dapat disimpulkan bahwa:
- **KNN**: Akurasi tertinggi pada data asli adalah 0,96, dengan sedikit penurunan menjadi 0,93 setelah resampling, dan nilai 0,95 dengan seleksi fitur. Kombinasi seleksi fitur dan resampling menghasilkan akurasi 0,90.
- **Random Forest (RF)**: Akurasi tertinggi pada data asli adalah 0,93, namun mengalami penurunan menjadi 0,88 dengan resampling, 0,87 dengan seleksi fitur, dan 0,81 dengan kombinasi keduanya.
- **Multi-Layer Perceptron (MLP)**: Akurasi awal 0,55 meningkat menjadi 0,61 dengan resampling, tetapi menurun menjadi 0,46 dengan seleksi fitur dan sedikit meningkat menjadi 0,52 dengan kombinasi seleksi fitur dan resampling.

KNN terbukti lebih stabil dan efektif dalam menangani ketidakseimbangan kelas dan mengurangi dimensionalitas data dibandingkan dengan Random Forest dan MLP.

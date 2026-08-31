# Analisis Sentimen Opini Publik tentang Hantavirus pada TikTok

## Deskripsi

Repository ini berisi implementasi penelitian Tugas Akhir berjudul **“Implementasi Metode Support Vector Machine dan Naive Bayes untuk Analisis Opini Publik Tentang Hantavirus pada Platform TikTok”**.

Penelitian ini bertujuan untuk melakukan klasifikasi sentimen terhadap komentar TikTok yang membahas Hantavirus menggunakan dua algoritma klasifikasi, yaitu **Linear Support Vector Classifier (LinearSVC)** dan **Multinomial Naive Bayes**.

## Dataset

Dataset merupakan kumpulan komentar TikTok mengenai Hantavirus pada periode **Mei–Juni 2026**.

* Jumlah data awal: **5.199 komentar**
* Data setelah proses cleaning: **4.891 komentar**
* Atribut utama: tanggal, nama akun, dan teks komentar

Dataset awal dimuat dari file `dataset_hantavirus_mei_juni_2026.csv`.

## Tahapan Penelitian

Alur pengolahan data dalam repository ini terdiri dari:

1. **Load Dataset**

   * Memuat dataset komentar TikTok.
   * Dataset disimpan dan diproses menggunakan Google Drive dan Google Colab.

2. **Text Preprocessing**

   * Cleaning
   * Case Folding
   * Normalization
   * Tokenizing
   * Stopword Removal
   * Stemming

   Pada tahap cleaning dilakukan penghapusan emoji, URL, mention, hashtag, angka, tanda baca, karakter non-huruf, serta spasi berlebih. Data yang menjadi kosong setelah cleaning dihapus.

3. **Normalisasi**

   * Menggunakan kamus normalisasi bahasa Indonesia.
   * Kamus yang digunakan terdiri dari **4.331 pasangan kata slang dan kata formal**.

4. **Labeling Sentimen**

   * Data diberi label sentimen dan disimpan dalam `dataset_hantavirus_labeled.csv`.

5. **Ekstraksi Fitur TF-IDF**

   * Teks hasil preprocessing diubah menjadi representasi numerik menggunakan **TF-IDF**.
   * Matriks TF-IDF yang dihasilkan berukuran **4.891 × 4.210**.

6. **Pembagian Dataset**

   * Data dibagi menjadi data training dan testing untuk proses klasifikasi.

7. **Klasifikasi**

   Dua algoritma digunakan dalam penelitian:

   * **Linear Support Vector Classifier (LinearSVC)**
   * **Multinomial Naive Bayes**

   LinearSVC dilatih menggunakan data training dan kemudian digunakan untuk melakukan prediksi terhadap data testing.

   Multinomial Naive Bayes juga dilatih menggunakan data training dan digunakan untuk menghasilkan prediksi pada data testing.

8. **Evaluasi Model**

   Performa kedua model dievaluasi menggunakan:

   * Accuracy
   * Precision
   * Recall
   * F1-Score
   * Confusion Matrix

## Hasil Evaluasi

Berdasarkan hasil pengujian pada notebook:

| Model                   | Accuracy | Precision | Recall | F1-Score |
| ----------------------- | -------: | --------: | -----: | -------: |
| LinearSVC               |   85,19% |    85,14% | 85,19% |   85,16% |
| Multinomial Naive Bayes |   66,19% |    73,34% | 66,19% |   62,20% |

Hasil tersebut menunjukkan bahwa **LinearSVC menghasilkan performa lebih tinggi dibandingkan Multinomial Naive Bayes** pada dataset penelitian ini.

## Output

Beberapa hasil pengolahan yang dihasilkan dalam penelitian meliputi:

* Dataset hasil cleaning
* Dataset hasil case folding
* Dataset hasil normalization
* Dataset hasil tokenizing
* Dataset hasil stopword removal
* Dataset hasil stemming
* Dataset hasil labeling
* Matriks dan vectorizer TF-IDF
* Data train dan test
* Model LinearSVC
* Model Multinomial Naive Bayes
* Hasil prediksi
* Confusion Matrix
* Perbandingan performa model
* Distribusi label sentimen

## Tools dan Library

Penelitian ini menggunakan:

* Python
* Google Colab
* Google Drive
* Pandas
* Scikit-learn
* Sastrawi
* NumPy
* Matplotlib
* Pickle

## Struktur Utama

```text
Codingan_Akhir_Miftahul_Jannah.ipynb
│
├── Setup & Load Data
├── Text Preprocessing
│   ├── Cleaning
│   ├── Case Folding
│   ├── Normalization
│   ├── Tokenizing
│   ├── Stopword Removal
│   └── Stemming
├── Labeling Sentimen
├── Ekstraksi Fitur TF-IDF
├── Train-Test Split
├── Klasifikasi
│   ├── LinearSVC
│   └── Multinomial Naive Bayes
└── Evaluasi Model
    ├── Accuracy
    ├── Precision
    ├── Recall
    ├── F1-Score
    └── Confusion Matrix
```

## Kesimpulan Singkat

Berdasarkan hasil pengujian, **LinearSVC memberikan performa klasifikasi yang lebih baik dibandingkan Multinomial Naive Bayes** pada dataset komentar TikTok mengenai Hantavirus. LinearSVC memperoleh accuracy sebesar **85,19%**, sedangkan Multinomial Naive Bayes memperoleh accuracy sebesar **66,19%**.

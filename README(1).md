# Analisis Sentimen Opini Publik tentang Hantavirus di TikTok

## Deskripsi

Proyek ini merupakan implementasi analisis sentimen terhadap opini
masyarakat mengenai **Hantavirus** pada platform TikTok. Penelitian ini
membandingkan kinerja dua algoritma klasifikasi teks, yaitu
**LinearSVC** dan **Multinomial Naive Bayes**.

Data komentar dikumpulkan melalui teknik **web scraping menggunakan
Apify** pada periode Mei--Juni 2026. Selanjutnya, data diproses melalui
tahapan text preprocessing, pelabelan sentimen berbasis InSet Lexicon,
pembobotan TF-IDF, penanganan ketidakseimbangan kelas menggunakan Random
Oversampling, serta klasifikasi dan evaluasi model.

## Tujuan

1.  Menganalisis kecenderungan sentimen opini masyarakat mengenai
    Hantavirus pada TikTok.
2.  Mengklasifikasikan komentar ke dalam sentimen positif, negatif, dan
    netral.
3.  Membandingkan performa algoritma LinearSVC dan Multinomial Naive
    Bayes.

## Dataset

-   **Sumber data:** Komentar TikTok
-   **Akun sumber:** SCTV dan Liputan6
-   **Jumlah data hasil web scraping:** 5.203 komentar
-   **Jumlah data setelah proses filtering dan penghapusan data
    kosong:** 4.818 komentar
-   **Periode pengumpulan:** Mei--Juni 2026
-   **Kategori sentimen:** Positif, negatif, dan netral

## Tahapan Pengolahan Data

1.  Web scraping komentar TikTok menggunakan Apify.
2.  Filtering berdasarkan rentang waktu.
3.  Filtering kandidat bahasa daerah.
4.  Penghapusan data kosong.
5.  Text preprocessing:
    -   Cleaning
    -   Case folding
    -   Normalization
    -   Tokenizing
    -   Stopword removal
    -   Stemming
6.  Pelabelan sentimen menggunakan pendekatan rule-based berbasis InSet
    Lexicon.
7.  Pembobotan kata menggunakan TF-IDF.
8.  Pembagian data menggunakan rasio train-test split 80:20.
9.  Penanganan ketidakseimbangan kelas menggunakan Random Oversampling.
10. Klasifikasi menggunakan LinearSVC dan Multinomial Naive Bayes.
11. Evaluasi menggunakan confusion matrix, accuracy, precision, recall,
    dan F1-score.

## Distribusi Sentimen

Hasil analisis sentimen menunjukkan distribusi sebagai berikut:

-   **Sentimen negatif:** 44,77%
-   **Sentimen positif:** 28,21%
-   **Sentimen netral:** 27,02%

Sentimen negatif menjadi kategori yang paling dominan dalam dataset
penelitian.

## Hasil Evaluasi Model

### LinearSVC

-   **Accuracy:** 83,71%

### Multinomial Naive Bayes

-   **Accuracy:** 75,00%

Berdasarkan nilai accuracy, LinearSVC menghasilkan performa klasifikasi
yang lebih tinggi dibandingkan Multinomial Naive Bayes pada dataset
penelitian ini.

## Teknologi yang Digunakan

-   Python
-   Google Colab
-   Pandas
-   Scikit-learn
-   Sastrawi
-   Matplotlib
-   Apify
-   Microsoft Excel

## Struktur Proses

``` text
Data Komentar TikTok
        |
        v
Web Scraping
        |
        v
Filtering Data
        |
        v
Text Preprocessing
        |
        v
Pelabelan InSet Lexicon
        |
        v
TF-IDF
        |
        v
Random Oversampling
        |
        v
Train-Test Split
        |
        v
LinearSVC dan Multinomial Naive Bayes
        |
        v
Evaluasi Model
```

## Keterbatasan

-   Data penelitian hanya berasal dari sejumlah unggahan TikTok
    tertentu.
-   Pelabelan sentimen menggunakan pendekatan berbasis aturan dengan
    InSet Lexicon.
-   Metode berbasis kamus memiliki keterbatasan dalam memahami konteks,
    sarkasme, bahasa tidak baku, dan makna tersirat.
-   Hasil penelitian tidak dapat secara langsung mewakili keseluruhan
    opini masyarakat Indonesia.

## Penulis

**Miftahul Jannah**\
Program Studi Teknik Informatika\
Universitas Bakrie

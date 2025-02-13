# Pemodelan Analisis Sentimen Di Twitter Terhadap Harga Tiket Konser 
## Pendahuluan
Proyek ini berfokus pada analisis sentimen teks di media sosial Twitter (X), dengan topik sentimen penggemar K-pop terhadap harga tiket konser. Analisis ini dilakukan untuk memahami opini positif dan negatif yang muncul dalam diskusi di Twitter. 

Dengan pendekatan machine learning, proyek ini mengklasifikasikan sentimen ke dalam dua kategori: positif dan negatif.

## Tujuan Proyek
-	Memahami pola sentimen penggemar K-pop di Twitter terhadap harga tiket konser.
-	Mengembangkan model klasifikasi sentimen menggunakan Support Vector Machine (SVM).

## Dataset
Dataset yang digunakan dalam proyek ini bersumber dari Twitter (X) melalui proses crawling data menggunakan Tweet-Harvest. Data bersifat publik dan mencakup skala area nasional.
-	Periode Pengumpulan Data: 8 November 2023 - 8 Januari 2024
-	Jumlah Data: 2.698 tweet
-	Klasifikasi Sentimen:
    - Sentimen Positif: 1.017 tweet
    - Sentimen Negatif: 1.681 tweet

       ![image](https://github.com/user-attachments/assets/0a7e1762-0b6c-4748-a611-b2e59cfc8c52)

## Metodologi
Proyek ini terdiri dari beberapa tahapan utama:
1.	Pengumpulan Data: Data dikumpulkan dari Twitter menggunakan Tweet-Harvest.
2.	Preprocessing Data: Tahapan preprocessing meliputi:
    -	Cleansing: Menghapus karakter yang tidak diperlukan seperti URL, emoji, dan tanda baca.
    -	Case folding: Mengubah teks menjadi huruf kecil.
    -	Tokenizing: Memisahkan teks menjadi token.
    -	Normalization: Mengubah kata-kata tidak baku menjadi baku.
    -	Stopword removal: Menghapus kata-kata umum yang tidak bermakna (contoh: "yang", "dan").
3.	Data Labeling: Tweet diberi label sentimen positif atau negatif secara manual.
4.	Resampling Data: Setelah split data, dilakukan upsampling untuk menyeimbangkan distribusi data.
5.	Pemodelan:
    -	Representasi vektor menggunakan Word2Vec.
    - Klasifikasi menggunakan Support Vector Machine (SVM) dengan empat kernel: 
        -	Linear
        -	RBF
        -	Sigmoid
        -	Polynomial
6.	Evaluasi Model: Evaluasi dilakukan menggunakan metrik seperti akurasi dan confusion matrix.

## Hasil
-	**Akurasi Tertinggi**:
    - Skenario split data 90:10 dengan kernel polynomial mencapai akurasi 85,19%.

      ![image](https://github.com/user-attachments/assets/03a0ffdb-3e5d-47ab-9532-01f34e5ee4e6)

-	**Evaluasi Confusion Matrix (90:10)**:
    -	True Negative (TN): 137 data
    -	False Positive (FP): 19 data
    -	False Negative (FN): 21 data
    -	True Positive (TP): 93 data

      ![image](https://github.com/user-attachments/assets/5f97b684-b92f-45b8-b5af-359c0988b3bc)

-	**Wordcloud Sentimen Positif**: Kata-kata yang dominan menunjukkan antusiasme menonton, pembelian tiket, dan harga tiket yang dianggap layak.

      ![image](https://github.com/user-attachments/assets/9298667d-39f0-4017-884b-03afa2f9c352)

-	**Wordcloud Sentimen Negatif**: Kata-kata yang muncul mencerminkan keluhan terhadap harga tiket yang dianggap mahal dan ketidakpuasan terhadap kebijakan promotor.

      ![image](https://github.com/user-attachments/assets/527c1605-5163-4ab8-9c1e-f9e802719263)


## Kesimpulan
Proyek ini menunjukkan bahwa metode machine learning dengan pendekatan Word2Vec dan SVM dapat secara efektif menganalisis sentimen penggemar K-pop terhadap harga tiket konser. 

Hasil analisis ini memberikan wawasan yang relevan untuk memahami opini penggemar, yang dapat digunakan oleh promotor atau pihak terkait dalam menentukan kebijakan harga tiket.

## Pengembangan Selanjutnya
-	Menggunakan dataset dengan skala yang lebih besar.
-	Mengintegrasikan model dengan aplikasi berbasis web untuk analisis sentimen secara real-time.

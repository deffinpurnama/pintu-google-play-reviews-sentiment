# Analisis Sentimen Ulasan Aplikasi PINTU (Google Play Store)

![Pintu App Reviews Sentiment Analysis](https://via.placeholder.com/800x300?text=Visualisasi+Distribusi+Sentimen+PINTU)
*Ganti placeholder ini dengan visualisasi kunci dari hasil sentimen Anda (misalnya, grafik batang distribusi sentimen Positif/Negatif/Netral, atau word cloud dari masing-masing kategori).*

## 📌 Deskripsi Proyek

Proyek ini berfokus pada **analisis sentimen ulasan pengguna aplikasi PINTU** yang dikumpulkan langsung dari Google Play Store. Dalam lanskap investasi kripto yang dinamis di Indonesia, aplikasi seperti PINTU memainkan peran sentral. Memahami sentimen pengguna menjadi sangat krusial bagi pengembang, analis pasar, dan calon pengguna untuk mengevaluasi pengalaman, mengidentifikasi area peningkatan, dan memahami persepsi publik terhadap aplikasi.

Proyek ini mencakup seluruh alur kerja data science di bidang Natural Language Processing (NLP):
1.  **Pengumpulan Data (Scraping):** Mengunduh ribuan ulasan pengguna secara otomatis.
2.  **Pra-pemrosesan Teks Komprehensif:** Mengubah teks mentah menjadi format yang siap untuk analisis, termasuk penanganan *slang words* dan *stemming* Bahasa Indonesia.
3.  **Pelabelan Sentimen:** Mengategorikan ulasan menjadi positif, negatif, atau netral.
4.  **Pemodelan Klasifikasi Sentimen:** Membangun dan membandingkan beberapa model Machine Learning untuk klasifikasi sentimen otomatis.
5.  **Analisis dan Visualisasi:** Menginterpretasi hasil dan menyajikan wawasan kunci.

## 🎯 Tujuan Proyek

* Mengumpulkan data ulasan pengguna aplikasi PINTU yang ekstensif dari Google Play Store.
* Melakukan pra-pemrosesan teks yang canggih untuk membersihkan dan menormalisasi data ulasan.
* Mengembangkan dan membandingkan performa model klasifikasi sentimen menggunakan algoritma **Random Forest, Logistic Regression, dan Decision Tree**.
* Memberikan wawasan mendalam tentang sentimen pengguna, mengidentifikasi poin kuat dan area yang perlu ditingkatkan dari aplikasi PINTU.
* Menyajikan hasil analisis secara visual untuk pemahaman yang lebih mudah.

## 🚀 Fitur Utama & Metodologi

### 1. Pengumpulan Data
* Menggunakan pustaka `google_play_scraper` untuk menambang ulasan aplikasi PINTU secara efisien.
* Data ulasan disimpan dalam format Excel (`ulasan_pintu.xlsx`).

### 2. Pra-pemrosesan Teks (NLP Pipeline)
Pipeline pra-pemrosesan yang komprehensif diterapkan pada setiap ulasan, meliputi:
* **Cleaning:** Menghilangkan *mentions*, *hashtags*, *RT*, *links*, angka, dan tanda baca.
* **Casefolding:** Mengubah semua teks menjadi huruf kecil.
* **Fixing Slangwords:** Mengganti kata-kata *slang* (bahasa gaul) yang umum dengan padanan baku mereka menggunakan kamus kustom (disertakan dalam kode). Ini sangat penting untuk data ulasan pengguna di Indonesia.
* **Tokenizing:** Memecah teks menjadi unit-unit kata (token).
* **Stopword Removal:** Menghapus kata-kata umum yang tidak bermakna (misal: "yang", "dan", "nya"), menggunakan daftar *stopwords* bawaan Bahasa Indonesia dan Inggris, serta *custom stopwords* yang relevan dengan domain kripto/aplikasi.
* **Stemming:** Mengubah kata-kata menjadi bentuk dasarnya menggunakan Sastrawi Stemmer untuk Bahasa Indonesia.
* **To Sentence:** Menggabungkan kembali token menjadi kalimat yang bersih.

### 3. Pelabelan Sentimen & Ekstraksi Fitur
* **Pelabelan:** Sentimen ulasan dilabeli (Positif, Negatif, Netral) (Sebutkan metode pelabelan di sini: apakah manual, menggunakan kamus sentimen, atau *pre-trained model*?)
* **Ekstraksi Fitur:** Menggunakan metode seperti TF-IDF (Term Frequency-Inverse Document Frequency) atau CountVectorizer untuk mengubah teks menjadi representasi numerik yang dapat diproses oleh model Machine Learning.

### 4. Pemodelan Klasifikasi Sentimen
Tiga algoritma klasifikasi Machine Learning telah diimplementasikan dan dibandingkan:
* **Random Forest**
* **Logistic Regression**
* **Decision Tree**
Setiap model dilatih pada data yang telah dipisahkan (training/testing) dan dievaluasi performanya.

### 5. Evaluasi dan Wawasan
* Model dievaluasi menggunakan metrik standar klasifikasi seperti **Accuracy, Precision, Recall, dan F1-score**.
* (Sebutkan secara spesifik model mana yang berkinerja terbaik dan mengapa, misal: "Model Random Forest menunjukkan akurasi terbaik sebesar X% dalam memprediksi sentimen.")
* Hasil analisis divisualisasikan untuk memberikan pemahaman yang jelas tentang distribusi sentimen dan tema-tema kunci yang muncul dalam ulasan.

## 📂 Struktur Repositori

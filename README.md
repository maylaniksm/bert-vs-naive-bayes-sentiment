# 🎬 Analisis Sentimen Menggunakan Naïve Bayes dan BERT (NLP)

![NLP](https://img.shields.io/badge/Domain-NLP-blue)
![Sentiment](https://img.shields.io/badge/Task-Sentiment%20Analysis-green)
![Model](https://img.shields.io/badge/Models-Naïve%20Bayes%20%7C%20BERT-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 👩‍🎓 Informasi Mahasiswa
- **Nama**  : Maylani Kusuma Wardhani  
- **NIM**   : 202210370311123  
- **Kelas** : Pemrosesan Bahasa Alami C  

📌 **Google Colab**  
https://colab.research.google.com/drive/1CTzc4auwzycXelWHU44uTsJinRrvce6_  

---

## 📖 Pendahuluan

### 🔍 Latar Belakang
Analisis sentimen merupakan salah satu penerapan penting dalam **Natural Language Processing (NLP)** yang bertujuan untuk menentukan polaritas suatu teks, seperti **positif** atau **negatif**. Teknik ini banyak digunakan dalam berbagai bidang, seperti analisis ulasan produk, media sosial, pemasaran, dan layanan pelanggan.

Pada proyek ini, dilakukan analisis sentimen terhadap **ulasan film** menggunakan dataset **Rotten Tomatoes**. Dua pendekatan model digunakan dan dibandingkan, yaitu **Naïve Bayes** sebagai model klasik machine learning dan **BERT** sebagai model deep learning berbasis transformer, untuk melihat perbedaan performa keduanya dalam klasifikasi sentimen.

---

### 🎯 Tujuan
Tujuan dari implementasi ini adalah:
1. Menganalisis sentimen ulasan film menggunakan teknik NLP
2. Melatih model **Naïve Bayes** dan **BERT** untuk klasifikasi sentimen
3. Membandingkan performa kedua model berdasarkan metrik evaluasi
4. Memberikan rekomendasi model terbaik berdasarkan hasil evaluasi

---

## 🧪 Metodologi

### 📂 Dataset
Dataset yang digunakan adalah **Rotten Tomatoes** dari Hugging Face Datasets. Dataset ini berisi ulasan film yang telah dilabeli menjadi dua kelas sentimen:
- **0** : Sentimen Negatif  
- **1** : Sentimen Positif  

Pembagian dataset:
- **Train** : 8.530 data  
- **Validation** : 1.066 data  
- **Test** : 1.066 data  

---

### 🧹 Preprocessing Teks
Tahapan preprocessing dilakukan untuk membersihkan data teks agar dapat diproses oleh model dengan optimal, meliputi:
1. Menghapus karakter khusus, angka, dan tanda baca
2. Mengubah seluruh teks menjadi huruf kecil (*lowercase*)
3. Menghapus stopwords untuk mengurangi kata yang tidak informatif
4. Melakukan tokenisasi teks
5. Menerapkan stemming atau lemmatization untuk mengubah kata ke bentuk dasarnya

---

### 🔢 Representasi Fitur
Untuk mengubah teks menjadi bentuk numerik, digunakan beberapa teknik representasi fitur, yaitu:

- **Bag of Words (BoW)**  
  Menghitung frekuensi kemunculan kata dalam dokumen tanpa mempertimbangkan konteks.

- **TF-IDF (Term Frequency – Inverse Document Frequency)**  
  Memberikan bobot lebih besar pada kata yang jarang muncul namun informatif.

- **Word Embeddings**  
  Menggunakan representasi kata berbasis embedding, termasuk embedding kontekstual dari BERT, untuk menangkap makna dan hubungan antar kata.

---

### 🤖 Model yang Digunakan

#### 1️⃣ Naïve Bayes
Model **Multinomial Naïve Bayes** digunakan dengan dua pendekatan fitur:
- Naïve Bayes + BoW
- Naïve Bayes + TF-IDF  

Model ini bersifat sederhana, cepat, dan sering digunakan sebagai baseline dalam klasifikasi teks.

#### 2️⃣ BERT
Model **DistilBERT (distilbert-base-uncased)** digunakan sebagai pendekatan deep learning. DistilBERT merupakan versi ringan dari BERT dengan performa yang mendekati model aslinya, namun lebih efisien dari segi komputasi.

---

## 📊 Hasil dan Analisis

### 📈 Evaluasi Model
Hasil evaluasi model berdasarkan metrik **Accuracy**, **Precision**, **Recall**, dan **F1-score** adalah sebagai berikut:

| Model | Accuracy | Precision | Recall | F1-score |
|------|----------|-----------|--------|----------|
| Naïve Bayes (BoW) | 77.78% | 77.79% | 77.78% | 77.78% |
| Naïve Bayes (TF-IDF) | 77.96% | 77.98% | 77.96% | 77.96% |
| BERT | **86.87%** | **86.90%** | **86.87%** | **86.87%** |

---

### 📉 Analisis Performa Model

#### 🔹 Naïve Bayes (BoW)
- Proses training dan prediksi sangat cepat
- Mudah diinterpretasikan
- Performa lebih rendah karena tidak memahami konteks kata

#### 🔹 Naïve Bayes (TF-IDF)
- Performa lebih baik dibandingkan BoW
- Mempertimbangkan bobot kata yang lebih informatif
- Masih terbatas dalam memahami konteks semantik

#### 🔹 BERT
- Mampu memahami konteks dan hubungan antar kata secara mendalam
- Memberikan performa terbaik di semua metrik evaluasi
- Membutuhkan sumber daya komputasi dan waktu training lebih besar

---

## 🏁 Kesimpulan
Berdasarkan hasil eksperimen dan evaluasi, dapat disimpulkan bahwa:
1. **BERT** memberikan performa terbaik dalam klasifikasi sentimen dibandingkan Naïve Bayes
2. **Naïve Bayes** tetap relevan untuk kebutuhan model yang cepat dan ringan
3. Pendekatan **TF-IDF** lebih efektif dibandingkan BoW pada Naïve Bayes
4. Model berbasis transformer seperti BERT lebih cocok untuk analisis sentimen yang kompleks dan kontekstual

---

## 📌 Catatan Akhir
Repository ini dibuat sebagai bagian dari tugas mata kuliah **Pemrosesan Bahasa Alami (NLP)** dan bertujuan untuk memahami perbandingan antara model klasik machine learning dan model deep learning berbasis transformer dalam analisis sentimen.

✨ *Feel free to explore, reuse, and improve this project!*

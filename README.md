# Hate Speech Detection - Indonesian Language

Klasifikasi Ujaran Kebencian (Hate Speech) dalam Bahasa Indonesia menggunakan **Naive Bayes** dan **TF-IDF**. Proyek ini merupakan implementasi dari tugas UTS Kecerdasan Buatan untuk mendeteksi konten berbahaya di media sosial.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk **mendeteksi ujaran kebencian** dalam tweet berbahasa Indonesia menggunakan pendekatan Machine Learning. Dataset yang digunakan adalah **ID Hate Speech Dataset** yang terdiri dari 713 tweet dengan label:
- **Non_HS** (Non Hate Speech): Tweet yang tidak mengandung ujaran kebencian
- **HS** (Hate Speech): Tweet yang mengandung ujaran kebencian

Model yang dibangun mampu mengklasifikasikan teks dengan akurasi **~88%** menggunakan algoritma **Multinomial Naive Bayes** dan representasi fitur **TF-IDF**.

---

## 🎯 Fitur Utama

- ✅ **Preprocessing Teks Lengkap** (Case folding, Cleaning, Tokenisasi, Stopword Removal, Stemming)
- ✅ **Handling Imbalanced Data** dengan Under-Sampling
- ✅ **TF-IDF Feature Extraction** (Unigram + Bigram)
- ✅ **Model Training** dengan Naive Bayes
- ✅ **Evaluasi Komprehensif** (Confusion Matrix, Accuracy, Precision, Recall, F1-Score)
- ✅ **Visualisasi Data** (Word Cloud, Charts, Heatmap)
- ✅ **Prediksi Real-time** untuk teks baru
- ✅ **Save & Load Model** untuk deployment

---

## 📊 Dataset

**Sumber:** ID Hate Speech Dataset https://github.com/ialfina/id-hatespeech-detection.git

**Catatan:** Dataset tidak seimbang (imbalanced), sehingga dilakukan **Random Under-Sampling** untuk menciptakan distribusi 50%-50%.

---

## 🚀 Instalasi & Penggunaan
### 1️⃣ Clone Repository

```bash
git clone https://github.com/username/hate-speech-detection.git
cd hate-speech-detection
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

**Dependencies:**
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn
- Sastrawi
- wordcloud

### 3️⃣ Jalankan di Google Colab

1. Upload file **`hate_speech_detection.ipynb`** ke Google Colab
2. Upload dataset **`unbalanced_dataset.csv`**
3. Run semua cell
4. Lihat hasil analisis dan visualisasi

---

## 🔬 Metodologi

### **1. Preprocessing Teks**
- **Case Folding**: Mengubah semua teks menjadi huruf kecil
- **Cleaning**: Menghapus URL, mention (@), hashtag (#), angka, dan tanda baca
- **Tokenisasi**: Memecah teks menjadi token/kata
- **Stopword Removal**: Menghapus kata-kata umum (Bahasa Indonesia)
- **Stemming**: Mengubah kata ke bentuk dasar (menggunakan Sastrawi)

### **2. Feature Extraction**
- **TF-IDF (Term Frequency-Inverse Document Frequency)**
- Max features: 1000
- N-gram range: (1, 2) - Unigram + Bigram

### **3. Model Training**
- **Algoritma**: Multinomial Naive Bayes
- **Train-Test Split**: 80% Training - 20% Testing
- **Balancing**: Random Under-Sampling

### **4. Evaluasi Model**
| Metric | Score |
|--------|-------|
| **Accuracy** | 88.10% |
| **Precision** | 90.48% |
| **Recall** | 86.36% |
| **F1-Score** | 88.37% |

---

## 📝 Laporan Lengkap

Untuk dokumentasi lengkap proyek ini, silakan baca:
- 📄 [Laporan UTS (PDF)](docs/Laporan_UTS_Hate_Speech_Detection.pdf)

---

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan fork repository ini dan buat pull request untuk:
- Peningkatan akurasi model
- Penambahan algoritma lain (SVM, LSTM, BERT)
- Perbaikan preprocessing
- Penambahan dataset

---

## 📚 Referensi

1. Davidson, T., et al. (2017). "Automated Hate Speech Detection and the Problem of Offensive Language"
2. IndoBERT: Pre-trained Language Models for Indonesian NLP
3. Sastrawi - Indonesian Stemmer Library
4. Scikit-learn Documentation

---

## ⭐ Support

Jika proyek ini bermanfaat, jangan lupa berikan ⭐ di repository ini!

---

## 📌 Catatan

**Disclaimer:** Model ini dibuat untuk tujuan edukatif dan penelitian. Penggunaan untuk deteksi ujaran kebencian di dunia nyata memerlukan pengembangan lebih lanjut dengan dataset yang lebih besar dan diverse.

---

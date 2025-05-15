# Sentiment Analysis with SVM

Proyek ini merupakan implementasi sederhana dari analisis sentimen menggunakan algoritma **Support Vector Machine (SVM)** dengan data teks ulasan. Dataset yang digunakan berasal dari file _Training.txt_, berisi berbagai opini terhadap film/buku seperti _The Da Vinci Code_ dan _Mission Impossible_.

---

## Dataset

- File: _Training.txt_
- Format: _label [tab] ulasan_
- Label:
  - 1 → Positif / Suka
  - 0 → Negatif / Tidak Suka (jika tersedia, saat ini hanya positif)

Contoh:

- _The Da Vinci Code was awesome!_
- _Mission Impossible 3 is amazing._

---

## Tools & Library

- Python
- Scikit-learn (_SVC_, _TfidfVectorizer_, _train_test_split_)
- Pandas & NumPy
- NLTK (lemmatization)
- Matplotlib & Seaborn (visualisasi)

---

## Langkah-langkah

1. **Preprocessing:**
   - Lowercasing
   - Regex tokenization
   - Lemmatization menggunakan _WordNetLemmatizer_
2. **Fitur:**

   - TF-IDF Vectorization

3. **Training Model:**

   - Algoritma: _SVC(kernel='linear')_
   - Evaluasi: _classification_report_, confusion matrix

4. **Prediksi Contoh Teks:**
   - _"the da vinci code is awesome"_ → Liked
   - _"the movie was boring and bad"_ → Disliked

---

## Hasil

- Model berhasil dilatih dan menghasilkan klasifikasi yang baik pada data positif.
- Karena dataset hanya berisi label `1`, model tidak bisa sepenuhnya dievaluasi untuk klasifikasi biner. Tambahan data negatif diperlukan untuk akurasi menyeluruh.

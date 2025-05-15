# Sentiment Analysis with SVM

Proyek ini merupakan implementasi sederhana dari analisis sentimen menggunakan algoritma **Support Vector Machine (SVM)** dengan data teks ulasan. Dataset yang digunakan berasal dari file `Training.txt`, berisi berbagai opini terhadap film/buku seperti _The Da Vinci Code_ dan _Mission Impossible_.

---

## Dataset

- File: `Training.txt`
- Format: `label [tab] ulasan`
- Label:
  - `1` → Positif / Suka
  - `0` → Negatif / Tidak Suka (jika tersedia, saat ini hanya positif)

Contoh:

- `The Da Vinci Code was awesome!`
- `Mission Impossible 3 is amazing.`

---

## Tools & Library

- Python
- Scikit-learn (`SVC`, `TfidfVectorizer`, `train_test_split`)
- Pandas & NumPy
- NLTK (lemmatization)
- Matplotlib & Seaborn (visualisasi)

---

## Langkah-langkah

1. **Preprocessing:**
   - Lowercasing
   - Regex tokenization
   - Lemmatization menggunakan `WordNetLemmatizer`
2. **Fitur:**

   - TF-IDF Vectorization

3. **Training Model:**

   - Algoritma: `SVC(kernel='linear')`
   - Evaluasi: `classification_report`, confusion matrix

4. **Prediksi Contoh Teks:**
   - `"the da vinci code is awesome"` → Liked
   - `"the movie was boring and bad"` → Disliked

---

## Hasil

- Model berhasil dilatih dan menghasilkan klasifikasi yang baik pada data positif.
- Karena dataset hanya berisi label `1`, model tidak bisa sepenuhnya dievaluasi untuk klasifikasi biner. Tambahan data negatif diperlukan untuk akurasi menyeluruh.

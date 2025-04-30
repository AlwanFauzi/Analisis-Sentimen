
# 💬 Sentiment Analysis of Indonesian Tweets Using CNN

Proyek ini bertujuan untuk melakukan **klasifikasi sentimen** terhadap teks berbahasa Indonesia (contohnya dari Twitter) menjadi dua kelas: **positif** dan **negatif**. Proyek ini menggunakan pendekatan **deep learning dengan model CNN (Convolutional Neural Network)** dan pre-trained word embeddings.

---

## 🔧 Teknologi yang Digunakan
- Python
- TensorFlow / Keras
- Scikit-learn
- NLTK
- Pandas
- Pre-trained Word2Vec (Indonesia)
- Jupyter Notebook atau Python Script

---


## 🧪 Dataset
Dataset terdiri dari teks-teks berbahasa Indonesia yang telah diberi label `positif` atau `negatif`. Dataset dibersihkan dan diseimbangkan sebelum digunakan untuk pelatihan.

---

## ⚙️ Alur Proyek

1. **Preprocessing Teks**  
   Setiap teks akan diproses melalui:
   - Pembersihan karakter spesial
   - Case folding
   - Normalisasi kata gaul (slang)
   - Tokenisasi
   - Stopword removal
   - Konversi kembali menjadi kalimat bersih

2. **Embedding**  
   Model menggunakan embedding dari pre-trained Word2Vec Bahasa Indonesia dengan dimensi 300.

3. **Model CNN**  
   Arsitektur model:
   ```python
   Embedding(...)
   Conv1D(128, 5, activation='relu')
   MaxPooling1D(pool_size=4)
   Flatten()
   Dense(64, activation='relu')
   Dropout(0.5)
   Dense(1, activation='sigmoid')
   ```

4. **Evaluasi Model**  
   Model diuji dengan 2 skenario:
   - **Train-Test Split 80:20** (terbaik)
   - Train-Test Split 70:30  
   Model terbaik adalah **CNN dengan pembagian data 80:20**, dengan akurasi tertinggi pada data uji.

5. **Inference Kalimat Baru**  
   Pengguna dapat memasukkan kalimat baru yang akan diproses dan diprediksi sebagai *positif* atau *negatif* dengan confidence score.

---

## 📌 Catatan

- Model ini hanya membedakan dua kelas (positif dan negatif).

---

## 👨‍💻 Kontributor
- **Nama**: M. Alwan Fauzi  
- **NIM**: 225150700111008  
- **Universitas**: Universitas Brawijaya  
- **Tugas**: Proyek Analisis Sentimen — Klasifikasi Teks Bahasa Indonesia

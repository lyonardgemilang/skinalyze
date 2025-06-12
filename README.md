# Skinalyze: Deteksi Dini Kanker Kulit dengan AI

**Skinalyze** adalah proyek Machine Learning berbasis web yang dirancang untuk klasifikasi dan deteksi dini terhadap **tujuh jenis lesi kulit**, termasuk **melanoma**, menggunakan arsitektur **Convolutional Neural Network (CNN)** dengan pendekatan **Transfer Learning**.

---

## 👨‍💻 Tim Pengembang (Kelompok CC25-CF029)

| Nama                              | Peran                        |
|-----------------------------------|------------------------------|
| Andreas Wirawan Dananjaya         | Machine Learning Engineer    |
| Rakha Alif Athallah               | Machine Learning Engineer    |
| Lyonard Gemilang Putra MG         | Machine Learning Engineer    |
| Maurits Brian Anthonius Sitinjak | Front-End & Back-End Developer |
| Achmad Fauzi Aranda              | Front-End & Back-End Developer |

---

## 🔍 Latar Belakang

Kanker kulit, khususnya **melanoma**, merupakan tantangan kesehatan global dengan tingkat **mortalitas tinggi**. Di negara tropis seperti Indonesia, risiko meningkat karena **tingginya paparan sinar UV**, namun akses terhadap **skrining dini** yang cepat dan terjangkau masih terbatas.  
Skinalyze hadir untuk menjembatani kesenjangan ini dengan menyediakan solusi teknologi berbasis AI untuk **skrining awal yang mudah diakses siapa saja**.

---

## 🚀 Solusi yang Ditawarkan

Skinalyze menyediakan platform web yang memungkinkan pengguna untuk **mengunggah gambar lesi kulit** dan mendapatkan hasil klasifikasi awal secara **instan**.

---

## 🧠 Teknologi yang Digunakan

- **Machine Learning**: TensorFlow, Keras, Scikit-learn  
- **Data Analysis**: Pandas, NumPy, Matplotlib, Seaborn  
- **Platform**: Google Colab + GPU T4  
- **Dataset**: [HAM10000 - Skin Cancer MNIST](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)

---

## ⚙️ Cara Menjalankan Notebook

1. **Persiapan Awal**
   - Buka file `.ipynb` di Google Colab
   - Aktifkan GPU: *Runtime > Change runtime type > GPU (T4)*

2. **Siapkan Kaggle API**
   - Dapatkan `kaggle.json` dari akun Kaggle Anda
   - Upload dan jalankan:
     ```python
     from google.colab import files
     files.upload()

     !mkdir -p ~/.kaggle
     !cp kaggle.json ~/.kaggle/
     !chmod 600 ~/.kaggle/kaggle.json
     print("Kaggle API berhasil disiapkan.")
     ```

3. **Unduh Dataset**
   ```bash
   !kaggle datasets download -d kmader/skin-cancer-mnist-ham10000
   !unzip skin-cancer-mnist-ham10000.zip -d ./dataset

4. **Jalankan Semua Sel**
- Runtime > Run all


🔄 Langkah-Langkah dalam Notebook
- Prapemrosesan Data

- Augmentasi & Normalisasi

- Transfer Learning dengan MobileNetV3-Large

- Pelatihan & Fine-tuning

- Evaluasi Model (Accuracy, Recall, Confusion Matrix)

- Inferensi & Ekspor Model (.keras, .tflite, TensorFlow.js)


🧩**Arsitektur Model**
- Base Model: MobileNetV3-Large

- Classifier Head:

- GlobalAveragePooling2D

- Dense (ReLU)

- Dropout

- Output (Softmax)




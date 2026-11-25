## Kelompok 2: Kecerdasan Buatan B

| No. | Nama | NPM |
|---|---|---|
| 1 | Hazairin | 2408107010001 |
| 2 | Rijaluddin Abdul Ghani | 2408107010008 |
| 3 | Khairul Fikri | 2408107010032 |
| 4 | Muhammad Yazid Arrazi | 2408107010072 |
| 5 | Muhammad Rizkan Rajabi | 2408107010110 |

# 🌿 LeafCare : Klasifikasi Citra Daun Cabai Berbasis CNN

LeafCare merupakan proyek berbasis **Artificial Intelligence (AI)** yang menerapkan metode **Deep Learning** untuk melakukan klasifikasi citra daun cabai. Proyek ini menggunakan **Convolutional Neural Network (CNN)** sebagai metode utama dengan arsitektur **MobileNetV2** melalui teknik *Transfer Learning*.

LeafCare dikembangkan untuk mengenali karakteristik visual daun cabai dan mengelompokkannya ke dalam enam kelas kondisi daun berdasarkan dataset yang digunakan. Selain proses klasifikasi, proyek ini menerapkan **Grad-CAM (Gradient-weighted Class Activation Mapping)** sebagai teknik visualisasi untuk menunjukkan bagian citra yang berkontribusi terhadap hasil prediksi model.

Aplikasi dikembangkan menggunakan Streamlit sehingga proses klasifikasi dapat dilakukan melalui antarmuka berbasis web.

---

## 🎯 Tujuan Proyek

Tujuan pengembangan LeafCare adalah:

1. Menerapkan metode Deep Learning menggunakan arsitektur CNN untuk klasifikasi citra daun cabai.
2. Memanfaatkan teknik Transfer Learning dengan arsitektur MobileNetV2 untuk proses klasifikasi.
3. Mengelompokkan citra daun cabai ke dalam enam kelas kondisi daun berdasarkan dataset.
4. Memvisualisasikan bagian citra yang berkontribusi terhadap hasil prediksi menggunakan Grad-CAM.

---

## 🧠 Metode dan Teknologi Utama

### 1. Convolutional Neural Network (CNN)

CNN merupakan metode Deep Learning yang dirancang untuk mengolah data berbentuk citra. CNN menjadi metode utama dalam proyek LeafCare karena mampu mempelajari karakteristik visual melalui proses ekstraksi fitur secara bertahap.

Secara umum, CNN memiliki beberapa komponen utama, yaitu:

- **Convolution Layer:** Mengekstraksi fitur dari citra, seperti pola, tekstur, dan bentuk.
- **Pooling Layer:** Mengurangi dimensi fitur dengan mempertahankan informasi penting.
- **Fully Connected Layer:** Mengolah fitur yang telah diekstraksi untuk menghasilkan prediksi kelas.

### 2. MobileNetV2 dan Transfer Learning

LeafCare menggunakan MobileNetV2 sebagai arsitektur CNN. MobileNetV2 merupakan arsitektur jaringan saraf konvolusional yang dirancang agar efisien dalam penggunaan komputasi.

Teknik Transfer Learning digunakan dengan memanfaatkan bobot model yang telah dilatih sebelumnya sebagai dasar pembelajaran untuk tugas klasifikasi citra daun cabai.

### 3. Grad-CAM

Grad-CAM digunakan sebagai teknik visualisasi pendukung untuk memahami bagian citra yang berkontribusi terhadap prediksi model CNN.

Hasil visualisasi berupa *heatmap* yang ditampilkan pada citra masukan. Area dengan aktivasi lebih tinggi menunjukkan bagian citra yang memiliki kontribusi lebih besar terhadap prediksi model.

Grad-CAM tidak digunakan sebagai metode klasifikasi utama dan hasil visualisasinya tidak secara langsung membuktikan kebenaran biologis dari prediksi model.

---

## 🍃 Dataset dan Kelas Klasifikasi

Dataset yang digunakan dalam proyek LeafCare berasal dari Mendeley Data dengan judul:

**Image Dataset on Chili Leaf Diseases in the Krishna River Basin of the Deccan Plateau, India**

- Penulis: Malghan, R. L. et al.
- Versi: 3
- Tahun: 2026
- DOI: [10.17632/ymt8k9bjkn.3](https://doi.org/10.17632/ymt8k9bjkn.3)
- Lisensi: CC BY 4.0

Dataset tersebut terdiri dari enam kelas kondisi daun cabai, yaitu:

| No. | Kelas | Keterangan |
|---|---|---|
| 1 | Bacterial Spot | Gejala bercak bakteri |
| 2 | Curl Virus | Gejala keriting akibat virus |
| 3 | Cercospora Leaf Spot | Gejala bercak daun Cercospora |
| 4 | Nutrition Deficiency | Kondisi kekurangan nutrisi |
| 5 | White Spot | Gejala bercak putih |
| 6 | Healthy Leaves | Daun dalam kondisi sehat |

Keenam kelas tersebut digunakan sebagai kategori klasifikasi dalam model CNN.

---

## 🚀 Fitur Aplikasi LeafCare

Aplikasi LeafCare menyediakan fitur-fitur berikut sesuai dengan implementasi aplikasi:

- **Klasifikasi Citra Daun:** Melakukan prediksi kelas kondisi daun cabai menggunakan model CNN MobileNetV2.
- **Visualisasi Grad-CAM:** Menampilkan heatmap untuk memperlihatkan bagian citra yang berkontribusi terhadap hasil prediksi.
- **Unggah Citra:** Memungkinkan pengguna memasukkan citra daun cabai untuk diproses oleh model.
- **Validasi Citra:** Mendukung proses pemeriksaan citra masukan sebelum klasifikasi.
- **Informasi Kondisi Daun:** Menyediakan informasi terkait kelas hasil klasifikasi melalui modul informasi yang tersedia pada aplikasi.

---

## 🛠️ Teknologi yang Digunakan

| Teknologi | Kegunaan |
|---|---|
| Python | Bahasa pemrograman utama |
| PyTorch | Pengembangan dan pemrosesan model Deep Learning |
| CNN | Metode utama klasifikasi citra |
| MobileNetV2 | Arsitektur CNN yang digunakan |
| Transfer Learning | Teknik pemanfaatan model pralatih |
| Grad-CAM | Visualisasi bagian citra yang berkontribusi terhadap prediksi |
| Streamlit | Pengembangan antarmuka aplikasi |
| OpenCV | Pemrosesan citra |

---

## 📁 Struktur Direktori Proyek

```text
LeafCare/
│
├── .streamlit/
│   └── config.toml
│
├── assets/
│   ├── samples/
│   ├── bg_cabai.jpg
│   ├── favicon.png
│   ├── studio-bg.jpg
│   └── style.css
│
├── models/
│   └── mobilenetv2_chi...
│
├── utils/
│   ├── __pycache__/
│   ├── class_names.json
│   ├── disease_info.py
│   ├── gradcam.py
│   ├── icons.py
│   ├── leaf_validator.py
│   ├── model_loader.py
│   ├── predict.py
│   └── preprocess.py
│
├── app.py
├── README.md
└── requirements.txt
```

### Keterangan Direktori

- **`.streamlit/`**: Menyimpan konfigurasi tampilan aplikasi Streamlit.
- **`assets/`**: Menyimpan aset pendukung aplikasi, seperti gambar, sampel citra, ikon, dan stylesheet.
- **`models/`**: Menyimpan file model CNN MobileNetV2 yang telah dilatih.
- **`utils/`**: Menyimpan modul pendukung untuk klasifikasi, prapemrosesan citra, validasi, informasi kelas, pemuatan model, dan visualisasi Grad-CAM.
- **`app.py`**: File utama untuk menjalankan aplikasi LeafCare.
- **`requirements.txt`**: Berisi daftar dependensi Python yang dibutuhkan proyek.
- **`README.md`**: Dokumentasi proyek LeafCare.

---

## 💻 Instalasi dan Menjalankan Aplikasi

### 1. Clone Repository

```bash
git clone <URL-REPOSITORY>
```

### 2. Masuk ke Direktori Proyek

```bash
cd LeafCare
```

Sesuaikan nama direktori apabila nama folder repository berbeda.

### 3. Instalasi Dependensi

```bash
pip install -r requirements.txt
```

### 4. Jalankan Aplikasi

```bash
streamlit run app.py
```

Setelah berhasil dijalankan, aplikasi dapat diakses melalui alamat lokal yang ditampilkan oleh Streamlit, umumnya:

```text
http://localhost:8501
```

---

## 📊 Evaluasi Model

Evaluasi dilakukan untuk mengetahui kemampuan model CNN MobileNetV2 dalam mengklasifikasikan citra daun cabai.

Beberapa metrik evaluasi yang dapat digunakan meliputi:

- **Accuracy:** Mengukur proporsi prediksi yang benar terhadap seluruh data pengujian.
- **Precision:** Mengukur ketepatan model dalam memprediksi suatu kelas.
- **Recall:** Mengukur kemampuan model dalam mengenali data dari suatu kelas.
- **F1-Score:** Mengukur keseimbangan antara precision dan recall.
- **Confusion Matrix:** Menampilkan perbandingan antara kelas aktual dan kelas hasil prediksi.

---

## 📚 Referensi

1. Abade, A., Ferreira, P. A. and Vidal, F. B. (2021). Plant diseases recognition on images using convolutional neural networks: A systematic review. *Computers and Electronics in Agriculture*, 185, 106125. https://doi.org/10.1016/j.compag.2021.106125

2. Barbedo, J. G. A. (2016). A review on the main challenges in automatic plant disease identification based on visible range images. *Biosystems Engineering*, 144, pp. 52–60. https://doi.org/10.1016/j.biosystemseng.2016.01.017

3. Malghan, R. L. et al. (2026). *Image Dataset on Chili Leaf Diseases in the Krishna River Basin of the Deccan Plateau, India*. Version 3. Mendeley Data. https://doi.org/10.17632/ymt8k9bjkn.3

4. Selvaraju, R. R. et al. (2017). Grad-CAM: Visual explanations from deep networks via gradient-based localization. *Proceedings of the IEEE International Conference on Computer Vision (ICCV)*, pp. 618–626. https://doi.org/10.1109/ICCV.2017.74

5. Thakur, P. S., Khanna, P., Sheorey, T. and Ojha, A. (2022). Trends in vision-based machine learning techniques for plant disease identification: A systematic review. *Expert Systems with Applications*, 208, 118117. https://doi.org/10.1016/j.eswa.2022.118117

6. Tugrul, B., Elfatimi, E. and Eryigit, R. (2022). Convolutional neural networks in detection of plant leaf diseases: A review. *Agriculture*, 12(8), 1192. https://doi.org/10.3390/agriculture12081192

---

# 📘 Judul Proyek
*(Analisis Perbandingan Algoritma Klasifikasi Machine Learning untuk Prediksi Hasil Permainan Tic Tac Toe Berdasarkan Dataset Tic Tac Toe)*

## 👤 Informasi
- **Nama:** [Azzahra Wahyu Olivia]  
- **Repo:** [https://github.com/azzahrawahyu21/UAS_Dataset_TicTacToe.git]  
- **Video:** [...]  

---

# 1. 🎯 Ringkasan Proyek
Proyek ini bertujuan untuk menerapkan dan membandingkan beberapa algoritma klasifikasi machine learning dalam memprediksi hasil permainan Tic Tac Toe berdasarkan kondisi papan permainan.
Tahapan yang dilakukan meliputi:
- Pemahaman permasalahan pada domain game analytics
- Analisis dan eksplorasi dataset Tic Tac Toe
- Data preparation (encoding, scaling, dan splitting)
- Pembangunan tiga model: Baseline, Advanced, dan Deep Learning
- Evaluasi performa model dan penentuan model terbaik berdasarkan metrik evaluasi

---

# 2. 📄 Problem & Goals
**Problem Statements:**  
- Bagaimana memprediksi hasil permainan Tic Tac Toe secara otomatis berdasarkan konfigurasi papan permainan?
- Algoritma klasifikasi machine learning apa yang memberikan performa terbaik untuk dataset Tic Tac Toe?
- Bagaimana perbandingan kinerja antara model baseline, advanced machine learning, dan deep learning?

**Goals:**  
- Membangun sistem klasifikasi untuk memprediksi hasil permainan Tic Tac Toe
- Membandingkan performa Logistic Regression, Random Forest, dan Multilayer Perceptron
- Menentukan model terbaik berdasarkan accuracy, precision, recall, dan F1-score
- Menghasilkan eksperimen yang dapat dijalankan ulang secara konsisten

---
## 📁 Struktur Folder
```
project/
│
├── data/                   # Dataset (tidak di-commit, download manual)
|   └── tic-tac-toe.data
│
├── environment
|
├── images/                 # Visualizations
│   ├── Confusion_Matrix_Logistic_Regression.png
│   ├── Confusion_Matrix_MLP.png
│   ├── Confusion_Matrix_Random_Forest.png
│   ├── EDA_Distribusi_Kelas.png
│   ├── EDA_Distribusi_Nilai.png
│   ├── EDA_Heatmap_Korelasi_Antar_Fitur.png
│   ├── Feature_Importance_Random_Forest.png
│   ├── Perbandingan_Acuuracy_Antar_Model.png
│   └── Visualisai_Loss_dan_Accuracy.png
|
├── models/                 # Saved models
│   ├── model_baseline.pkl
│   ├── model_mpl.h5
│   └── model_fr.pkl
|
├── notebooks/              # Jupyter notebooks
│   └── Azzahra_Wahyu_Olivia_UAS.ipynb
│
├── src/                    # Source code
│   
├── .gitignore
├── Checklist Submit.md
├── README.md
└── requirements.txt        # Dependencies
```
---

# 3. 📊 Dataset
- **Sumber:** [UCI Machine Learning Repository – Tic Tac Toe Endgame Dataset]  
- **Jumlah Data:** [958 baris]  
- **Jumlah Fitur:** [9 fitur + 1 label]  
- **Tipe:** [Categorical]  

### Fitur Utama
| Fitur | Deskripsi |
| top-left-square | Kondisi kotak kiri atas |
| top-middle-square | Kondisi kotak tengah atas |
| top-right-square | Kondisi kotak kanan atas |
| middle-left-square | Kondisi kotak kiri tengah |
| middle-middle-square | Kondisi kotak tengah |
| middle-right-square | Kondisi kotak kanan tengah |
| bottom-left-square | Kondisi kotak kiri bawah |
| bottom-middle-square | Kondisi kotak tengah bawah |
| bottom-right-square | Kondisi kotak kanan bawah |
| class | Hasil permainan |

---

# 4. 🔧 Data Preparation
Tahapan data preparation meliputi:
- Data cleaning: Tidak ditemukan missing value dan data duplikat
- Encoding: Label Encoding untuk fitur dan target
- Scaling: MinMaxScaler untuk normalisasi fitur
- Splitting:
    - Training set: 80%
    - Test set: 20%
    - Stratified split untuk menjaga distribusi kelas

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:** [Logistic Regression]  
- **Model 2 – Advanced ML:** [Random Forest Classifier]  
- **Model 3 – Deep Learning:** [Multilayer Perceptron (MLP)]  

---

# 6. 🧪 Evaluation
**Metrik:** Accuracy, Precision, Recall, F1-Score, dan Confusion Matrix

### Hasil Singkat
| Model | Accuracy |Precision | Recall | F1-Score | Catatan | 
|-------|----------|----------|--------|----------|---------|
| Baseline (LR)	| 0.67	| 0.69	| 0.89	| 0.78	| Recall tinggi, precision rendah
| Advanced (RF)	| 0.95	| 0.93	| 1.00	| 0.96	| Performa terbaik
| Deep Learning (MLP) | 0.68	| 0.68	| 0.96	| 0.79	| Tidak optimal untuk data kecil

---

# 7. 🏁 Kesimpulan
- Model terbaik: [Random Forest]  
- Alasan: [Memberikan accuracy dan F1-score tertinggi serta prediksi paling stabil]  
- Insight penting:
    - Model yang lebih kompleks tidak selalu lebih baik
    - Dataset tabular kecil lebih cocok menggunakan machine learning tradisional
    - Feature importance membantu interpretasi hasil model

---

# 8. 🔮 Future Work
- [✅]Menambah variasi dan jumlah data permainan
- [✅]Melakukan hyperparameter tuning lebih lanjut
- [✅]Mencoba arsitektur deep learning yang berbeda
- [✅]Mengembangkan aplikasi prediksi berbasis web atau API

---

# 9. 🔁 Reproducibility
Gunakan environment:
Main Libraries:
- numpy==1.24.3
- pandas==2.0.3
- scikit-learn==1.3.0
- matplotlib==3.7.2
- seaborn==0.12.2
- tensorflow==2.14.0
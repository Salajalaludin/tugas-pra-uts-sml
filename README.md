# Bank Term Deposit Prediction

Proyek ini bertujuan untuk memprediksi apakah seorang nasabah akan berlangganan produk deposito berjangka berdasarkan data karakteristik demografi, riwayat interaksi bank, dan indikator sosial-ekonomi.

## 📊 Dataset
- **Dataset A (Labelled):** 37.071 observasi (Digunakan untuk training & validasi).
- **Dataset B (Unlabelled):** 4.117 observasi (Digunakan untuk prediksi final).

## 🚀 Alur Kerja (Pipeline)
1. **EDA & Preprocessing:** - Imputasi nilai `unknown` dengan modus.
   - Penanganan *Data Leakage* dengan menghapus fitur `duration`.
   - Feature scaling pada variabel numerik.
2. **Model Development:** Implementasi Random Forest, SVM, dan Neural Network (ANN).
3. **Threshold Optimization:** Mengkalibrasi ambang batas probabilitas untuk mengoptimalkan F1-Score karena adanya *class imbalance*.
4. **Prediction:** Menggunakan model ANN terbaik untuk memprediksi Dataset B.

## 📈 Performa Model Terbaik
- **Model:** Artificial Neural Network (ANN)
- **Threshold:** 0.26
- **F1-Score:** 0.4977
- **Accuracy:** 86.77%

## 📂 Struktur File
- `Hasil_Prediksi_Dataset_B.csv`: Hasil prediksi target (y) untuk 4.117 nasabah baru.
- `realselesai.rmd`: Kode sumber pengerjaan di R.

## 🛠 Requirements
Library R yang dibutuhkan:
- `caret`
- `randomForest`
- `e1071`
- `nnet`
- `MLmetrics`
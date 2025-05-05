# Kidney Tumor Detection and Classification (Modifikasi dari Dalia Alzubi)

Notebook ini merupakan pengembangan dari proyek awal milik [Dalia Alzubi](https://github.com/DaliaAlzubi/Kidney_Tumor), yang awalnya hanya mendeteksi keberadaan tumor ginjal. Versi ini, dimodifikasi  menambahkan sejumlah fitur penting untuk mengklasifikasikan *jenis tumor ginjal* secara lebih komprehensif dan praktis.

---

## Tujuan Proyek

- *Dalia Alzubi*: Deteksi keberadaan tumor ginjal (3 kelas)
- *modifikasi: Klasifikasi **empat jenis citra ginjal*: cyst, normal, stone, tumor

---

## Perubahan & Peningkatan

### 1. Dataset & Kelas
- *Asli*: 3 kelas (tergantung dataset)
- *Modifikasi*: 4 kelas → cyst, normal, stone, tumor
- Struktur dataset dirancang per direktori kelas agar dapat diproses otomatis

### 2. Arsitektur Model CNN
- *Asli*: CNN sederhana
- *Modifikasi*:
  - CNN dengan 3+ Conv2D layers
  - Penambahan Dropout, BatchNormalization
  - Lebih dalam dan robust untuk klasifikasi multi-kelas

### 3. Visualisasi & Evaluasi Model
- Penambahan grafik:
  - Accuracy vs Validation Accuracy
  - Loss vs Validation Loss
- Performa evaluasi:
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)

### 4. Fitur Prediksi Gambar Individu
- Fungsi prediksi gambar tunggal
- Gambar yang diklasifikasi akan *disimpan dalam folder output* sesuai kelas hasil prediksi (misal: /result/tumor/filename.jpg)

### 5. Ukuran Gambar
- Gambar diubah ke ukuran *64x64* agar lebih ringan dan cepat diproses, cocok untuk CNN kustom


## Cara Menjalankan Notebook

1. Upload dataset dengan struktur sesuai folder dataset/
2. Jalankan semua sel dalam notebook
3. Upload gambar untuk klasifikasi → hasil prediksi akan otomatis dipindahkan ke folder result/<kelas_prediksi>/

---

## Catatan

- Model tidak menggunakan pretrained (misalnya MobileNet), melainkan CNN buatan sendiri
- Dapat dikembangkan lebih lanjut dengan model transfer learning dan GUI prediksi

---

## Sumber

- [Notebook Asli - Dalia Alzubi](https://github.com/DaliaAlzubi/Kidney_Tumor)


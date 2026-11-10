
# Rencana Pengumpulan Data

## 1. Tujuan
Mengumpulkan dataset citra pribadi untuk eksperimen klasifikasi objek menggunakan metode HOG + SVM, CNN Baseline, dan CNN Improved.

## 2. Sumber Data
Dataset dikumpulkan secara mandiri menggunakan kamera HP Samsung Galaxy A51.

## 3. Kelas Dataset

| No | Kelas | Jumlah |
|---|---|---:|
| 1 | Laptop | 40 |
| 2 | Buku Gambar | 40 |
| 3 | Tas | 40 |
| | Total | 120 |

## 4. Kondisi Pengambilan Gambar

Setiap kelas memiliki dua kondisi:

- Ideal: 20 gambar dengan pencahayaan dan fokus yang baik.
- Sulit: 20 gambar dengan kondisi citra kurang ideal, seperti blur.

## 5. Pembagian Dataset

Dataset dibagi dengan perbandingan 70:15:15.

| Data | Jumlah |
|---|---:|
| Training | 84 |
| Validation | 18 |
| Testing | 18 |
| Total | 120 |

Random state: 42.

## 6. Rencana Eksperimen

1. Pemeriksaan struktur dan kualitas dataset.
2. Pembagian dataset.
3. Pembuatan baseline menggunakan HOG + SVM.
4. Pelatihan CNN Baseline.
5. Pengembangan CNN Improved.
6. Evaluasi dan perbandingan hasil ketiga metode.

## 7. Perangkat

- Python
- Google Colab
- Google Drive
- OpenCV
- TensorFlow / Keras
- Scikit-learn
- Samsung Galaxy A51

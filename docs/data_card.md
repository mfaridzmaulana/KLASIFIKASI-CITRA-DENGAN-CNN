
# Data Card – Dataset Klasifikasi Citra

## 1. Informasi Dataset

Nama: Dataset Klasifikasi Citra Objek

Jumlah data: 120 gambar

Sumber: Pengambilan gambar mandiri.

Perangkat: Samsung Galaxy A51.

## 2. Kategori Dataset

| Kelas | Kondisi Ideal | Kondisi Sulit | Total |
|---|---:|---:|---:|
| Laptop | 20 | 20 | 40 |
| Buku Gambar | 20 | 20 | 40 |
| Tas | 20 | 20 | 40 |
| Total | 60 | 60 | 120 |

## 3. Karakteristik Data

Kondisi ideal:
- Objek terlihat jelas.
- Fokus kamera baik.
- Pencahayaan relatif stabil.

Kondisi sulit:
- Gambar mengalami blur.
- Ketajaman gambar berkurang.
- Kondisi pengambilan gambar lebih menantang.

## 4. Preprocessing

- Pemeriksaan gambar.
- Penyesuaian ukuran menjadi 128 x 128 piksel.
- Penyesuaian format gambar.
- Normalisasi nilai piksel untuk CNN.

## 5. Pembagian Dataset

| Pembagian | Jumlah |
|---|---:|
| Training | 84 |
| Validation | 18 |
| Testing | 18 |

## 6. Penggunaan Dataset

Dataset digunakan untuk:
- Eksperimen HOG + SVM.
- Eksperimen CNN Baseline.
- Eksperimen CNN Improved.
- Evaluasi kondisi ideal dan sulit.

## 7. Keterbatasan Dataset

Jumlah dataset masih terbatas, yaitu 120 gambar.
Variasi objek, sudut pengambilan, latar belakang, dan pencahayaan dapat memengaruhi hasil klasifikasi.

## 8. Privasi dan Penggunaan

Dataset dikumpulkan untuk kepentingan akademik dan penelitian Computer Vision.

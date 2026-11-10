
# Checkpoint 2 – Eksperimen dan Evaluasi Model

## 1. Tujuan

Mendokumentasikan pelaksanaan eksperimen klasifikasi citra menggunakan tiga pendekatan.

## 2. Metode Eksperimen

1. HOG + SVM
2. CNN Baseline
3. CNN Improved

## 3. Hasil Pengujian

| Metode | Akurasi |
|---|---:|
| HOG + SVM | 72,22% |
| CNN Baseline | 72,22% |
| CNN Improved | 50,00% |

Jumlah data testing: 18 gambar.

## 4. Perbandingan Kondisi

| Metode | Ideal | Sulit |
|---|---:|---:|
| HOG + SVM | 77,78% | 66,67% |
| CNN Baseline | 66,67% | 77,78% |
| CNN Improved | 44,44% | 55,56% |

## 5. Analisis Awal

HOG + SVM dan CNN Baseline mendapatkan akurasi tertinggi, yaitu 72,22%.

CNN Improved memperoleh akurasi 50,00%. Hasil tersebut menunjukkan bahwa penambahan augmentasi dan perubahan arsitektur belum meningkatkan performa model pada dataset eksperimen ini.

## 6. Status

Eksperimen dan analisis awal telah dilakukan.

## 7. Pekerjaan Selanjutnya

- Melengkapi confusion matrix.
- Mendokumentasikan gambar yang salah diklasifikasikan.
- Menyusun pembahasan hasil.
- Menyelesaikan laporan dan presentasi.



# CHECKPOINT 2 — PERSIAPAN DATASET DAN LINGKUNGAN PENGEMBANGAN

## 1. Perkembangan Proyek
Pada tahap ini, pengumpulan dataset telah selesai dilakukan. Selanjutnya dilakukan persiapan struktur penyimpanan data dan lingkungan pengembangan untuk mendukung proses klasifikasi citra menggunakan CNN.

## 2. Struktur Penyimpanan Dataset
Dataset disimpan di Google Drive dengan pengelompokan berdasarkan tiga kelas objek:
- Laptop
- Buku Gambar
- Tas

Setiap kelas memiliki 40 foto yang dikumpulkan secara mandiri dengan kondisi ideal dan sulit.

## 3. Pengelolaan Proyek di GitHub
Repository GitHub telah dibuat dengan nama:
KLASIFIKASI-CITRA-DENGAN-CNN

Struktur repository saat ini terdiri dari:
- data/ : Penyimpanan dan pengelolaan data.
- docs/ : Dokumentasi proyek.
- notebooks/ : Tempat pengerjaan menggunakan Google Colab.
- src/ : Persiapan penyimpanan kode program.
- README.md : Informasi umum proyek.

## 4. Persiapan Lingkungan Pengembangan
- Google Drive telah dibuat dan disusun untuk penyimpanan dataset.
- Repository GitHub telah dibuat.
- Google Colab telah disiapkan dan dihubungkan dengan GitHub.
- Notebook digunakan sebagai lingkungan pengerjaan program Python.

## 5. Tahapan yang Belum Dilaksanakan
- [ ] Pemeriksaan dan seleksi kualitas seluruh gambar.
- [ ] Preprocessing citra.
- [ ] Resize dan normalisasi gambar.
- [ ] Pembagian data training, validation, dan testing.
- [ ] Pembuatan arsitektur model CNN.
- [ ] Proses training model.
- [ ] Evaluasi hasil klasifikasi.
- [ ] Pengujian model pada kondisi ideal dan sulit.
- [ ] Analisis kesalahan klasifikasi.

## 6. Kendala dan Catatan
Sampai checkpoint ini, pekerjaan masih berfokus pada pengumpulan dataset dan persiapan lingkungan pengembangan. Eksperimen model CNN belum dilaksanakan sehingga belum terdapat hasil akurasi maupun evaluasi model.

## 7. Rencana Selanjutnya
Tahap selanjutnya adalah melakukan pemeriksaan dataset, preprocessing citra, pembagian dataset, kemudian membangun dan melatih model CNN untuk melakukan klasifikasi tiga kelas objek.

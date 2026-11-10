PROJEK MK COMPUTER VISION
“KLARIFIKASI CITRA DENGAN MENGGUNAKAN CONVOLUTION NEURAL NETWORK”










Disusun 
Oleh :


Nama
Nim
Muhammad Faridz Maulana
2355202006
Muhammad Farrid
2355202005
Abdul Aziz
2355202012










Program Studi Teknik Informatika
UNIVERSITAS ISLAM SUMATERA BARAT 2026

1. RINGKASAN EKSEKUTIF (EXECUTIVE SUMMARY)
RINGKASAN ABSTRAK

	Proyek ini bertujuan untuk mengembangkan sistem klasifikasi citra menggunakan metode Convolutional Neural Network (CNN) untuk mengenali dan mengelompokkan objek berdasarkan karakteristik visual pada gambar. Sistem dirancang untuk melakukan proses pengolahan data gambar, pembelajaran fitur, pelatihan model, hingga menghasilkan prediksi terhadap kategori objek yang telah ditentukan.
Fokus utama proyek ini adalah menguji kemampuan model CNN dalam mengenali objek pada dua kondisi kualitas citra, yaitu kondisi ideal dan kondisi sulit. Kondisi ideal menggunakan gambar dengan pencahayaan yang stabil dan fokus objek yang jelas, sedangkan kondisi sulit menggunakan gambar yang mengalami blur atau penurunan ketajaman.
Dataset diperoleh melalui pengambilan gambar secara mandiri menggunakan kamera smartphone. Selanjutnya, data diproses dan digunakan dalam pelatihan serta pengujian model menggunakan Python, Google Colab, TensorFlow/Keras, dan OpenCV. Hasil eksperimen akan dianalisis berdasarkan nilai akurasi, precision, recall, F1-score, serta Confusion Matrix untuk mengetahui pengaruh kualitas citra terhadap hasil klasifikasi.

2. TUJUAN DAN LINGKUP PROYEK (PROJECT OBJECTIVES & SCOPE)
Tujuan Utama Proyek
Pengembangan Sistem Klasifikasi: Mengembangkan model CNN yang mampu mengenali dan mengelompokkan objek ke dalam tiga kategori berdasarkan karakteristik visual gambar.
Pengolahan Dataset: Mempersiapkan kumpulan gambar melalui proses pengubahan ukuran, normalisasi, dan pengelompokan data agar sesuai dengan kebutuhan pelatihan model.
Pengujian Ketahanan Model: Menguji kemampuan CNN dalam mengenali objek pada kondisi gambar ideal maupun gambar yang mengalami blur.
Evaluasi Hasil Klasifikasi: Mengukur performa model menggunakan metrik evaluasi untuk mengetahui tingkat ketepatan prediksi dan kesalahan klasifikasi.
Batasan Proyek (Scope Boundaries)
Data Input: Data masukan berupa gambar digital yang diperoleh melalui pengambilan foto secara mandiri.
Kategori Objek: Klasifikasi dibatasi pada tiga kelas objek, yaitu botol, buku, dan kunci sesuai contoh kategori yang tercantum dalam rancangan PPT.
Jumlah Dataset: Dataset direncanakan sebanyak 120 gambar, dengan pembagian 40 gambar untuk setiap kelas.
Kondisi Citra: Data dibagi menjadi kondisi ideal sebanyak 20 gambar dan kondisi blur sebanyak 20 gambar pada setiap kelas.
Perangkat Akuisisi: Pengambilan gambar menggunakan kamera smartphone dengan bantuan tripod, pencahayaan LED portabel, dan alas latar netral.
Environment: Pengembangan dan eksperimen dilakukan menggunakan Google Colab dengan bahasa pemrograman Python.
Metode Klasifikasi: Algoritma utama yang digunakan adalah Convolutional Neural Network (CNN).


3. DEFINISI DOMAIN CITRA (DATASET CONDITION DEFINITION)
Untuk mengetahui pengaruh kualitas gambar terhadap kemampuan klasifikasi model CNN, dataset dibagi menjadi dua domain kondisi, yaitu kondisi ideal dan kondisi sulit.
1. Citra Kondisi Ideal (Easy Condition)
Citra kondisi ideal merupakan gambar yang diambil dengan pengaturan lingkungan dan kualitas visual yang terjaga sehingga objek dapat terlihat dengan jelas.
Pencahayaan dan Kontras: Intensitas cahaya dibuat merata menggunakan bantuan pencahayaan LED portabel untuk mengurangi bayangan yang mengganggu tampilan objek.
Ketajaman Gambar: Objek berada dalam kondisi fokus sehingga bentuk, tepi, dan detail visual dapat terlihat dengan jelas.
Kestabilan Pengambilan: Kamera ditempatkan pada posisi yang stabil menggunakan tripod untuk mengurangi kemungkinan terjadinya guncangan saat pengambilan gambar.
Kejelasan Objek: Objek tidak tertutup oleh benda lain sehingga karakteristik visual setiap kategori dapat diamati dengan baik.

2. Citra Kondisi Sulit (Hard Condition)
Citra kondisi sulit merupakan gambar yang mengalami penurunan kualitas visual berupa blur sehingga informasi detail objek menjadi berkurang dan proses pengenalan oleh model CNN menjadi lebih menantang.
Motion dan Out-of-Focus Blur: Gambar mengalami keburaman akibat pergerakan kamera atau ketidaktepatan fokus saat pengambilan gambar.
Penurunan Detail Visual: Batas tepi, tekstur, dan bentuk objek menjadi kurang tajam sehingga informasi penting pada gambar berkurang.
Degradasi Fitur: Lapisan konvolusi pada CNN dapat mengalami kesulitan dalam mengenali pola visual yang menjadi pembeda antarobjek.
Variasi Blur: Pengujian dilakukan menggunakan blur alami dan blur sintetis melalui teknik Gaussian Blur dengan bantuan OpenCV.

4. SPESIFIKASI TEKNOLOGI DAN PERANGKAT LUNAK (TECH STACK)
Komponen
Pustaka / Tools
Fungsi Utama & Modul Spesifik
Bahasa Pemrograman
Python 3.x
Bahasa utama untuk pengolahan dataset, manipulasi data, dan pengembangan model CNN.
Pengolahan Citra
OpenCV
Digunakan untuk membaca gambar, melakukan resizing, konversi ruang warna, augmentasi citra, dan penerapan Gaussian Blur.
Komputasi Matriks
NumPy
Membantu operasi numerik, manipulasi array, serta pengolahan data gambar dalam bentuk matriks.
Pengolahan Dataset
Pandas
Membantu pengelolaan label, struktur dataset, dan informasi data yang digunakan dalam eksperimen.
Framework Deep Learning
TensorFlow / Keras
Digunakan untuk membangun arsitektur CNN melalui Conv2D, MaxPooling, Dense, dan Dropout serta mengatur optimizer Adam dan fungsi loss.
Environment
Google Colab
Lingkungan pengembangan berbasis notebook untuk menjalankan kode, melatih model, dan melakukan pengujian dengan dukungan GPU.
Perangkat Akuisisi
Kamera Smartphone
Digunakan untuk mengambil gambar objek secara mandiri sebagai bahan pembentukan dataset.
Perangkat Pendukung
Tripod dan LED Portabel
Membantu menjaga kestabilan posisi kamera dan mengatur pencahayaan saat pengambilan gambar.


5. PEMBAGIAN TUGAS DAN TANGGUNG JAWAB TIM (DIVISION OF 
RESPONSIBILITIES)  PERAN + NAMA ANGGOTA

Muhammad Faridz Maulana (NIM: 2355202006)
Peran Utama: Project Leader & CNN Model Developer
1. Fokus Utama: Bertanggung jawab terhadap pengembangan model klasifikasi CNN, integrasi sistem, dan koordinasi pengerjaan proyek kelompok.
2. Tanggung Jawab Teknis:
CNN Architecture Development: Merancang dan mengembangkan arsitektur CNN menggunakan TensorFlow/Keras, termasuk lapisan Conv2D, MaxPooling, Dense, dan Dropout.
Model Training: Mengatur proses pelatihan model menggunakan dataset yang telah melalui tahap preprocessing.
Model Optimization: Mengatur parameter pelatihan, optimizer Adam, serta fungsi loss untuk memperoleh hasil pembelajaran model yang optimal.
System Integration: Menggabungkan proses pengolahan dataset, pelatihan model, dan klasifikasi ke dalam satu alur eksperimen di Google Colab.
3. Tanggung Jawab Non-Teknis:
Mengatur koordinasi dan pembagian pekerjaan antaranggota kelompok.
Memantau perkembangan proyek serta memastikan setiap tahapan berjalan sesuai rencana.

Muhammad Farrid (NIM: 2355202005)
Peran Utama: Data Engineer & Image Preprocessing Specialist
1. Fokus Utama: Bertanggung jawab terhadap pengumpulan dataset, pengelompokan gambar, dan pengolahan awal citra sebelum digunakan dalam proses pelatihan CNN.
2. Tanggung Jawab Teknis:
Data Acquisition: Melakukan pengambilan gambar secara mandiri terhadap tiga kategori objek menggunakan kamera smartphone.
Dataset Curation: Mengumpulkan dan mengelompokkan 120 gambar berdasarkan kategori objek dan kondisi citra ideal maupun blur.
Image Preprocessing: Melakukan pengolahan awal gambar menggunakan OpenCV, seperti pengubahan ukuran dimensi gambar (resizing) dan penyesuaian format warna.
Image Degradation: Menyiapkan variasi gambar blur alami dan blur sintetis menggunakan teknik Gaussian Blur untuk kebutuhan eksperimen.
Dataset Preparation: Membantu melakukan normalisasi nilai piksel dan menyiapkan pembagian data latih serta data uji.
3. Tanggung Jawab Non-Teknis:
Mengelola penyimpanan dataset agar tersusun berdasarkan kategori dan kondisi gambar.
Melakukan pemeriksaan kualitas gambar sebelum dataset digunakan dalam eksperimen.

Abdul Aziz (NIM: 2355202012)
Peran Utama: Model Evaluation & Quality Assurance Specialist
1. Fokus Utama: Bertanggung jawab terhadap pengujian performa model, evaluasi hasil klasifikasi, dan analisis kesalahan prediksi pada kondisi citra yang berbeda.
2. Tanggung Jawab Teknis:
Model Testing: Melakukan pengujian terhadap model CNN menggunakan gambar dari masing-masing kategori objek.
Performance Evaluation: Mengukur hasil klasifikasi menggunakan metrik Accuracy, Precision, Recall, dan F1-Score.
Confusion Matrix Analysis: Menganalisis hasil prediksi untuk mengetahui kategori objek yang berhasil dikenali maupun yang mengalami kesalahan klasifikasi.
Robustness Testing: Membandingkan performa model pada gambar kondisi ideal dan kondisi blur untuk mengetahui pengaruh penurunan kualitas citra.
Error Analysis: Mengidentifikasi kemungkinan penyebab kesalahan prediksi berdasarkan karakteristik gambar dan hasil pengujian.
3. Tanggung Jawab Non-Teknis:
Mendokumentasikan hasil pengujian dan evaluasi model.
Membantu menyusun hasil analisis, laporan akhir, dan materi presentasi proyek.





6. SPESIFIKASI DATASET DAN KRITERIA KEBERHASILAN
1. Spesifikasi Dataset Pengujian
Dataset yang digunakan dalam proyek ini merupakan kumpulan gambar yang diperoleh melalui pengambilan data secara mandiri. Dataset disusun berdasarkan kategori objek dan kondisi kualitas citra untuk mendukung proses pelatihan serta pengujian model CNN.
Jumlah Sampel: Sebanyak 120 gambar digital yang dibagi ke dalam tiga kategori objek.
Kategori Objek: Tiga kelas objek spesifik, dengan contoh kategori berupa botol, buku, dan kunci.
Pembagian Sampel: Setiap kategori memiliki 40 gambar, terdiri dari 20 gambar kondisi ideal dan 20 gambar kondisi blur.
Kondisi Pengambilan: Pengambilan gambar dilakukan dengan variasi kondisi fokus dan kualitas ketajaman objek.
Perangkat Akuisisi: Kamera smartphone sebagai perangkat utama untuk mengambil gambar.
Perangkat Pendukung: Tripod, pencahayaan LED portabel, serta alas dengan latar netral untuk membantu menjaga konsistensi pengambilan data.
Format Data: Gambar digital yang diproses menggunakan OpenCV dan Python sebelum digunakan dalam pelatihan model.
Pembagian Dataset: Data disiapkan untuk kebutuhan pelatihan (training) dan pengujian (testing) model CNN.
2. Kriteria Keberhasilan (Acceptance Criteria)
Keberhasilan Klasifikasi: Model CNN mampu melakukan pengenalan dan pengelompokan gambar ke dalam tiga kategori objek yang telah ditentukan.
Pengolahan Dataset: Seluruh gambar dapat diproses dan digunakan sesuai format serta ukuran yang dibutuhkan oleh model.
Pengujian Kondisi Ideal: Model mampu melakukan klasifikasi terhadap gambar dengan pencahayaan stabil dan fokus yang jelas.
Pengujian Kondisi Sulit: Model dapat diuji pada gambar yang mengalami blur untuk mengetahui tingkat ketahanan dalam mengenali objek.
Pengukuran Performa: Sistem menghasilkan nilai Accuracy, Precision, Recall, dan F1-Score berdasarkan hasil pengujian.
Analisis Kesalahan: Confusion Matrix dapat digunakan untuk mengidentifikasi kesalahan prediksi pada masing-masing kategori objek.
Perbandingan Hasil: Tersedia hasil perbandingan performa model antara kondisi ideal dan kondisi blur sebagai dasar evaluasi pengaruh kualitas citra terhadap kemampuan klasifikasi CNN.


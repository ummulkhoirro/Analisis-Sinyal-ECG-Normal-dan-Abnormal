# Analisis-Sinyal-ECG-Normal-dan-Abnormal
Proyek ini bertujuan untuk menganalisis sinyal elektrokardiogram (ECG) dari dua sumber data utama, yaitu MIT-BIH Arrhythmia Dataset dan PTB Diagnostic ECG Database, untuk mendeteksi dan membedakan kondisi jantung normal dan abnormal. Data yang digunakan berasal dari rekaman aktivitas listrik jantung yang mencatat variasi potensial listrik yang dihasilkan oleh kontraksi dan relaksasi otot jantung.

# Tujuan Proyek:
1. Visualisasi Sinyal ECG: Menampilkan sinyal EKG dalam domain waktu untuk kedua kategori data (normal dan abnormal) untuk mendapatkan gambaran umum tentang pola aktivitas listrik jantung.
2. Transformasi Fourier: Menggunakan transformasi Fourier untuk menganalisis komponen frekuensi dalam sinyal ECG dan memberikan wawasan tentang spektrum frekuensi yang membentuk sinyal tersebut.
3. Analisis Sinyal Normal dan Abnormal: Membandingkan perbedaan antara sinyal ECG dalam kondisi normal dan kondisi abnormal, seperti aritmia atau gangguan jantung lainnya.
4. Deteksi Gangguan Jantung: Menyediakan metode untuk mendeteksi gangguan irama jantung melalui analisis sinyal dalam domain waktu dan frekuensi, serta untuk mengidentifikasi potensi masalah kesehatan jantung.

# Manfaat Proyek:
1. Peningkatan Pemahaman: Memberikan pemahaman yang lebih baik tentang bagaimana gangguan jantung mempengaruhi sinyal ECG, baik dalam domain waktu maupun frekuensi.
2. Deteksi Penyakit Jantung: Membantu dalam mendeteksi penyakit jantung lebih cepat dan lebih akurat melalui analisis sinyal ECG.

# Dataset
sumber : https://www.kaggle.com/datasets/shayanfazeli/heartbeat?resource=download 

Sinyal yang dianalisis adalah sinyal Elektrokardiogram (ECG), yang merupakan representasi grafis aktivitas listrik jantung selama siklus
detak jantung sehingga mencerminkan pola depolarisasi dan repolarisasi otot jantung, yang penting untuk mendiagnosis kondisi kesehatan jantung.
Yang berasal dari dataset MIT-BIH Arrhythmia dan PTB Diagnostic ECG Database.
- MIT-BIH: Merekam sinyal EKG pasien dengan berbagai jenis aritmia.
- PTBDB: Mengandung data normal dan abnormal, termasuk pasien dengan kondisi seperti infark miokard (serangan jantung).

# Metodologi:
1. Pengolahan Data: Menggunakan file CSV yang berisi sinyal EKG yang dipotong dan disegmentasi untuk setiap detak jantung. Setiap baris dalam file CSV mewakili data sinyal untuk detak jantung tertentu.
2. Analisis Sinyal dalam Domain Waktu: Menampilkan sinyal dalam domain waktu menggunakan Matplotlib untuk visualisasi pola detak jantung baik dalam kondisi normal maupun abnormal.
3. Transformasi Fourier: Menggunakan Scipy.fft untuk melakukan transformasi Fourier dan memperoleh informasi frekuensi dari sinyal ECG. Transformasi ini memungkinkan kita untuk mengidentifikasi komponen-komponen frekuensi yang membentuk sinyal jantung.
4. Perbandingan Kondisi Normal dan Abnormal: Membandingkan sinyal ECG yang diperoleh dari pasien yang sehat (normal) dengan pasien yang mengalami gangguan jantung (abnormal) dan mengidentifikasi pola yang berbeda dalam spektrum frekuensi.

# Hasil yang Diharapkan:
1. Visualisasi sinyal EKG yang memudahkan untuk membedakan pola normal dan abnormal.
2. Analisis domain frekuensi yang memberikan gambaran lebih jelas tentang gangguan atau perubahan irama jantung.
3. Deteksi dini gangguan irama jantung yang dapat digunakan untuk membantu dalam diagnosis medis dan pemantauan kondisi jantung.


# Bagaimana sinyal itu diperoleh dan Sinyal kondisi sinyal

1. Sinyal MIT-BIH:
   
Direkam pada frekuensi sampling 125 Hz dengan durasi panjang untuk setiap sesi.
Menggambarkan kondisi pasien dengan aritmia seperti PVC (Premature Ventricular Contractions), Bigeminy, dan lainnya.

2. Sinyal PTBDB:
   
Juga direkam pada frekuensi sampling 125 Hz.

- Dataset ini mengelompokkan sinyal menjadi Normal dan Abnormal, termasuk gangguan seperti iskemia dan infark miokard.
Dataset tersebut menyediakan label yang mengindikasikan jenis sinyal, antaralain :
   - MIT-BIH: Kelas ['N' (Normal), 'S', 'V', 'F', 'Q']
   - PTBDB: Kategori 0 (Normal) dan 1 (Abnormal).

# Informasi yang tersimpan pada sinyal tersebut
Dari data EKG, memperoleh: 

1. Gelombang P, QRS, dan T:
- Digunakan untuk memahami aktivitas listrik atrium dan ventrikel.
- Abnormalitas bentuk atau intervalnya dapat menunjukkan masalah seperti AV Block atau Bundle Branch Block.

2. Interval RR (Puncak R ke R):
- Memberikan informasi tentang irama jantung (reguler atau tidak).
- Variabilitas interval RR membantu mendeteksi aritmia seperti Fibrilasi Atrium.

3. Amplitudo Gelombang:
- Mengindikasikan kekuatan aktivitas listrik jantung.
- Amplitudo rendah bisa menunjukkan iskemia atau masalah konduksi.

4. Frekuensi:
- Membantu mengidentifikasi noise atau artefak.
- Rentang normal komponen frekuensi adalah sekitar 0.5 Hz hingga 50 Hz.

# Perbedaan sinyal dalam kondisi normal dan abnormal
- Kondisi Normal:
    1. Gelombang P, QRS, dan T memiliki bentuk standar.
    2. Interval RR seragam.
    3. Tidak ada gangguan amplitudo atau pola yang tidak lazim.

- Kondisi Abnormal:
    1. Pola gelombang tidak beraturan (misalnya, gelombang QRS melebar pada Ventricular Tachycardia).
    2. Interval RR tidak seragam (terlalu pendek atau terlalu panjang).
    3. Abnormalitas amplitudo (tinggi pada hipertrofi ventrikel atau rendah pada serangan jantung).

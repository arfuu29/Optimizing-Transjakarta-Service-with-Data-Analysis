**Analisis Data Perjalanan dan Perilaku Pengguna Transjakarta**
===============================================================

Proyek ini merupakan studi analisis data mendalam terhadap pola perjalanan dan perilaku pengguna layanan Bus Rapid Transit (BRT) TransJakarta. Dengan memanfaatkan data historis transaksi tap-in dan tap-out, analisis ini bertujuan untuk menggali insight yang dapat digunakan sebagai dasar pengambilan keputusan strategis untuk meningkatkan efisiensi operasional dan kualitas layanan transportasi publik di Jakarta.

**Latar Belakang**
------------------

Sebagai ibu kota Indonesia, Jakarta menghadapi tantangan mobilitas yang kompleks. TransJakarta, sebagai sistem BRT pertama di Asia Tenggara, menjadi tulang punggung transportasi umum bagi ratusan ribu warga setiap harinya. Namun, tantangan seperti ketimpangan volume penumpang, waktu tunggu yang tidak merata, dan tingginya angka kegagalan tap-out masih menjadi isu yang perlu diatasi. Analisis data ini hadir untuk memberikan solusi berbasis bukti (data-driven) terhadap permasalahan tersebut.

**❗️ Pernyataan Masalah**
-------------------------

Bagaimana TransJakarta dapat meningkatkan efisiensi dan keadilan layanan melalui pemahaman mendalam terhadap perilaku pengguna, optimalisasi rute dan koridor, serta pencegahan pelanggaran sistem tap-out?

**📖 Sintesis Cerita Utama: Efek "Pressure Cooker"**
----------------------------------------------------

Analisis menunjukkan sebuah narasi utama yang dapat disebut **Efek "Pressure Cooker"**: Volume penumpang yang sangat terkonsentrasi di **koridor-koridor tulang punggung** pada **waktu-waktu puncak** menciptakan sebuah "panci bertekanan tinggi". Tekanan ini bermanifestasi dalam bentuk efisiensi yang menurun (durasi perjalanan lebih lama) dan perubahan perilaku pengguna (tingginya gagal tap-out akibat kepadatan dan ketergesa-gesaan). Ini berarti, masalah terbesar TransJakarta bukanlah masalah yang tersebar, melainkan sangat **terpusat dan dapat diprediksi**, sehingga solusi dapat difokuskan pada titik-titik kritis ini untuk dampak maksimal.

**🔍 Pertanyaan Kunci Analisis**
--------------------------------

Proyek ini berfokus untuk menjawab pertanyaan-pertanyaan berikut:

1.  **Analisis Pola Tren Waktu:** Kapan jam sibuk terjadi dan bagaimana perbedaannya antara hari kerja dan akhir pekan?
    
2.  **Analisis Rute dan Koridor:** Koridor mana yang paling padat dan mana yang paling sepi? Pola komuter apa yang terlihat?
    
3.  **Analisis Kegagalan Tap-Out:** Siapa, kapan, dan di mana kegagalan tap-out paling sering terjadi?
    

**📊 Dataset**
--------------

Dataset yang digunakan adalah data transaksi historis TransJakarta yang mencakup informasi perjalanan seperti ID pengguna, koridor, waktu tap-in/tap-out, dan demografi dasar.

_Catatan: Dataset ini merepresentasikan perjalanan tunggal dan tidak mencakup data transit antar koridor._

**🛠️ Metodologi**
------------------

Analisis dilakukan melalui beberapa tahapan utama yang terdokumentasi dalam notebook Jupyter (Transjakarta Data Analysis.ipynb):

1.  **Eksplorasi Data (Data Exploration):** Memahami karakteristik dasar dataset.
    
2.  **Pembersihan dan Pra-pemrosesan Data (Data Cleaning & Preprocessing):** Menangani nilai yang hilang dan melakukan _feature engineering_ (misalnya, menghitung usia dan durasi perjalanan).
    
3.  **Analisis Data Eksploratif (Exploratory Data Analysis - EDA):** Menganalisis tren dan pola berdasarkan waktu, lokasi, dan demografi.
    
4.  **Visualisasi Data:** Menggunakan Matplotlib dan Seaborn untuk membuat visualisasi yang informatif.
    

**💡 Temuan Utama & Rekomendasi**
---------------------------------

#### **1\. Temuan: Pola Jam Sibuk Ganda**

*   **Deskripsi:** Terdapat dua puncak kepadatan di hari kerja (pagi: 07.00-08.00, sore: 17.00-18.00) yang berbeda drastis dengan pola akhir pekan yang lebih landai.
    
*   **Rekomendasi:** Tingkatkan frekuensi dan kapasitas bus pada jam-jam puncak di koridor utama.
    
*   **Dampak Bisnis:** Meningkatkan kepuasan pelanggan dengan mengurangi waktu tunggu dan kepadatan.
    

#### **2\. Temuan: Kesenjangan Performa Koridor**

*   **Deskripsi:** Terdapat kesenjangan ekstrem antara koridor teramai (misalnya, Cibubur-Balaikota) dan tersepi (misalnya, Kp. Rambutan-Blok M).
    
*   **Rekomendasi:** Prioritaskan investasi (perluasan halte, penambahan armada) pada koridor teramai dan lakukan evaluasi rasionalisasi (penggabungan rute, penyesuaian armada) pada koridor tersepi.
    
*   **Dampak Bisnis:** Alokasi sumber daya yang lebih efisien dan optimalisasi biaya operasional.
    

#### **3\. Temuan: Gagal Tap-Out Terpusat**

*   **Deskripsi:** Kegagalan tap-out tertinggi terjadi pada jam pulang kerja (16.00-19.00), terutama oleh pengguna usia muda (17-25 tahun) di koridor-koridor padat.
    
*   **Rekomendasi:** Tambahkan pengingat visual/audio di halte padat dan luncurkan kampanye edukasi berbasis media sosial yang menargetkan segmen usia pelajar/mahasiswa.
    
*   **Dampak Bisnis:** Meningkatkan akurasi data perjalanan (Origin-Destination) yang krusial untuk perencanaan jangka panjang.
    

**🗺️ Peta Jalan Implementasi (Roadmap)**
-----------------------------------------

| **Horizon Waktu**         | **Fokus**                          | **Contoh Aksi**                                                                                   |
|---------------------------|------------------------------------|----------------------------------------------------------------------------------------------------|
| **Jangka Pendek (< 6 bulan)** | Quick Wins & Atasi Keluhan Mendesak | • Optimalisasi jadwal bus paling pagi (05.00)  <br>• Kampanye edukasi tap-out di media sosial  <br>• Pengingat audio/visual di halte utama |
| **Jangka Menengah (6–18 bulan)** | Pembangunan Fondasi Sistem         | • Bangun dashboard monitoring real-time  <br>• Uji coba notifikasi tap-out via aplikasi  <br>• Evaluasi dan rasionalisasi rute sepi         |
| **Jangka Panjang (> 18 bulan)**  | Inovasi & Transformasi Layanan     | • Studi kelayakan skema tarif dinamis (misal: tarif lebih murah di luar jam sibuk)  <br>• R&D sistem tap-out otomatis  <br>• Integrasi data penuh dengan MRT/LRT |


**🚀 Teknologi yang Digunakan**
-------------------------------

*   **Bahasa:** Python 3
    

**Library:** pandas, numpy, matplotlib, seaborn

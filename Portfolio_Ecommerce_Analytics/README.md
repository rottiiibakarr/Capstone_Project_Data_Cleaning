# 🛒 E-Commerce Data Analytics: From Messy Data to Business Insights

## 📌 Latar Belakang & Tujuan Bisnis (Business Context)
Di era digital, data transaksi e-commerce sering kali diinput secara manual atau berasal dari berbagai sistem yang tidak terintegrasi, menghasilkan data yang sangat kotor (*messy data*). Proyek ini bertujuan untuk membersihkan data transaksi mentah yang penuh anomali dan mengekstrak *insight* bisnis yang dapat diproses untuk strategi penjualan dan promosi di bulan berikutnya.

## 🗄️ Sumber Data (Data Source)
- **Sumber:** Dataset simulasi e-commerce (Atau tuliskan tautan sumber asli jika menggunakan data publik seperti Kaggle / BPS semacamnya).
- **Deskripsi Data:** Memuat metrik transaksi seperti ID Order, Nama Kategori, Harga per Unit, Kuantitas, Tanggal Order, Kode Diskon, dan Biaya Pengiriman.

## 🛠️ Tech Stack
- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

## 📂 Struktur Proyek
Proyek ini menggunakan struktur *modular* yang memisahkan proses transformasi data dan analisis visual:
1. `01_Data_Cleaning.ipynb` : Skrip pemrosesan data.
2. `02_Data_Visualization.ipynb` : Skrip untuk *Exploratory Data Analysis* (EDA) dan visualisasi.
3. `/data_raw/` : Direktori penyimpanan data mentah yang belum diproses.
4. `/data_clean/` : Direktori penyimpanan data yang telah dibersihkan dan siap untuk dianalisis.

---

## 🧹 Bagian 1: Pembersihan Data (Data Cleaning)
Dataset awal memiliki berbagai masalah kualitas data. Penanganan yang dilakukan meliputi:
- **Complex Currency Parsing:** Pembuatan fungsi kustom (`.apply()`) untuk mendeteksi dan mengonversi format mata uang yang tidak konsisten ("3.5 Juta", "100K", "Gratis", "Rp", "IDR") menjadi *float* numerik.
- **Text Standardization:** Pembersihan *whitespaces*/*spasi* gaib, penyeragaman huruf kapital, dan standarisasi nama kategori produk.
- **Imputation & Logical Constraints:** Mengoreksi kuantitas bernilai negatif, menghilangkan teks "pcs", dan mengisi *missing values* (NaN) pada kolom `Quantity` menggunakan nilai *Median*.
- **Feature Engineering:** Menciptakan metrik bisnis penting: `Total_Sales` (Harga * Kuantitas) dan `Final_Amount` (Total Sales + Biaya Pengiriman).

---

## 🖼️ Dashboard Visualisasi (Visualization Dashboard)

![Tren Penjualan](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_Ecommerce_Analytics/Total_Pendapatan.png?raw=true)
*Gambar 1: Tren total pendapatan harian selama bulan Februari 2024.*

![Kategori Produk](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_Ecommerce_Analytics/Keuntungan_Produk.png?raw=true)
*Gambar 2: Perbandingan total pendapatan berdasarkan kategori produk.*

![Kuantitas Pembelian](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_Ecommerce_Analytics/Keuntungan_Produk.png?raw=true)
*Gambar 3: Perbandingan kuantitas pembelian produk berdasarkan jumlah transaksi.*

![Penggunaan Diskon](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_Ecommerce_Analytics/Penggunaan_Diskon.png?raw=true)
*Gambar 4: Perbandingan penggunaan diskon berdasarkan pengguna.*

---

## 📊 Bagian 2: Hasil Analisis & Temuan Utama (Key Insights)
Berdasarkan analisis visualisasi data yang telah dilakukan, berikut adalah temuan utama dari transaksi bulan Februari 2024:
1. **Tren Pendapatan Harian:** Pendapatan menunjukkan tren yang fluktuatif, dengan lonjakan transaksi tertinggi terjadi pada tanggal 11.
2. **Kategori Produk Paling Menguntungkan:** **Electronics** adalah penyumbang pendapatan terbesar, diikuti oleh Fashion. 
3. **Analisis Penggunaan Diskon:** Sebanyak **50%** pelanggan menggunakan kode diskon saat *checkout*. Tingkat penerapan promo ini tergolong Sedang.
4. **Distribusi Kuantitas Pembelian:** Mayoritas pelanggan membeli **1 hingga 2** barang dalam satu kali transaksi. 

---

## 💡 Rekomendasi Bisnis (Actionable Insights)
Berdasarkan temuan di atas, rekomendasi strategi untuk bulan depan adalah:
1. **Fokus Inventaris:** Memperbanyak stok dan variasi produk pada kategori **Electronics** karena terbukti memberikan *Revenue* terbesar.
2. **Optimalisasi Promo:** Mengingat penggunaan diskon berada di angka 50%, perusahaan bisa mempertimbangkan strategi *bundling* produk untuk mendorong pelanggan membeli lebih banyak barang per transaksi.

---

## 🚀 Cara Menjalankan Proyek (How to Run)
1. *Clone* repositori ini ke lokal *machine* Anda.
2. Pastikan file data kotor berada di `data_raw/data_capstone_ecommerce.csv`.
3. Jalankan `Data_Cleaning.ipynb` terlebih dahulu untuk menghasilkan data bersih.
4. Jalankan `Data_Visualization.ipynb` untuk merender grafik analisis.

---

## 📬 Let's Connect!
Jika Anda memiliki pertanyaan, masukan, atau tawaran kolaborasi, jangan ragu untuk menghubungi saya:
- **Email:** diki.naufal29dev@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/dikinaufal/
- **Portfolio:** Menyusul! 😁🙏


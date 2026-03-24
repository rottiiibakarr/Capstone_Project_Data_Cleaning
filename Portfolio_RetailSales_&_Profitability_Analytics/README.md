# ⚽ Retail Sales & Profitability Analysis: From Messy Data to Business Insights

## 📌 Latar Belakang & Tujuan Bisnis (Business Context)
Data transaksi dari sistem kasir (*Point of Sales*) di industri ritel sering kali kotor dan tidak konsisten akibat proses input manual. Proyek ini bertujuan untuk membersihkan data mentah tersebut dan mengubahnya menjadi *insight* bisnis yang berguna untuk mengevaluasi performa penjualan, profitabilitas produk, dan tren keuntungan.

## 🗄️ Sumber Data & Kamus Data(Data Sources and Data Dictionary)
- **Sumber:** Dataset simulasi e-commerce (Atau tuliskan tautan sumber asli jika menggunakan data publik seperti Kaggle / BPS semacamnya).
- **Kamus Data Utama:**
  - `Invoice_ID`: Nomor unik bukti transaksi.
  - `Salesperson`: Nama staf yang melayani transaksi.
  - `Store_Location`: Cabang toko fisik (Jakarta, Bandung, Surabaya).
  - `Product_Name`: Nama jersey klub sepak bola yang terjual.
  - `Units_Sold`: Jumlah barang yang dibeli.
  - `Revenue`: Pendapatan kotor dari transaksi.
  - `Cost_per_Unit`: Harga modal dari satu buah jersey.
  - `Total_Cost`: Total harga modal.
  - `Total_Profit`: Keuntungan bersih.
  - `Profit_Margin_%`: Persentase margin keuntungan.

## 🛠️ Tech Stack
- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

## 📂 Struktur Proyek
1. `01_Data_Cleaning.ipynb` : Skrip pembersihan data mentah.
2. `02_Data_Visualization.ipynb` : Skrip *Exploratory Data Analysis* (EDA) dan visualisasi.
3. `/data_raw/` : Direktori penyimpanan data mentah.
4. `/data_clean/` : Direktori penyimpanan data bersih.

---

## 🧹 Bagian 1: Pembersihan Data (Data Cleaning)
Dataset awal memiliki berbagai anomali. Penanganan tingkat lanjut yang dilakukan meliputi:
- **Advanced Text Mapping:** Menggunakan fungsi *custom* bersarang (*nested if-elif-else*) untuk mendeteksi dan menyamakan berbagai variasi input nama produk yang berantakan menjadi nama klub standar (yang bersih).
- **Complex Regex & Currency Parsing:** Menggunakan *Regular Expression* (`regex=True`) untuk menghapus satuan teks ("pcs", "unit"), serta fungsi `.apply()` untuk mengonversi format mata uang Indonesia ("Juta", "K", "Rp", "IDR") menjadi numerik.
- **Imputation:** Mengisi data kuantitas penjualan yang kosong (*NaN*) dengan nilai *Median*.

---

## 🖼️ Dashboard Visualisasi (Dashboard Visualization)
![Performa Salesperson](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_RetailSales_&_Profitability_Analytics/performa_penjual.png?raw=true)
*Gambar 1: Perbandingan total pendapatan (Revenue) berdasarkan tenaga penjual.*

![Profitabilitas Produk](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_RetailSales_&_Profitability_Analytics/profibilitas_produk.png?raw=true)
*Gambar 2: Peringkat jersey klub yang memberikan total keuntungan (Total Profit) tertinggi.*

![Distribusi Penjualan](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_RetailSales_&_Profitability_Analytics/distribusi_penjualan.png?raw=true)
*Gambar 3: Perbandingan distribusi penjualan berdasarkan kota.*

![Tren Profit](https://github.com/rottiiibakarr/Capstone_Project_Data_Cleaning/blob/main/Portfolio_RetailSales_&_Profitability_Analytics/profit_harian.png?raw=true)
*Gambar 4: Tren profit harian selama bulan Maret 2024.*

---

## 📊 Bagian 2: Hasil Analisis & Temuan Utama (Key Insights)
Berdasarkan visualisasi data yang telah dilakukan, berikut adalah temuan bisnis utama selama bulan Maret 2024:
1. **Performa Tenaga Penjual:** **Andi T.** adalah tenaga penjual dengan performa terbaik, menyumbang total pendapatan paling besar bagi perusahaan.
2. **Profitabilitas Produk Utama:** Jersey **Paris Saint-Germain** menjadi produk yang paling menguntungkan.
3. **Distribusi Penjualan Kota:** Cabang **Jakarta** mendominasi kontribusi pendapatan total sebesar **55.8%**.
4. **Tren Profit Harian:** Tren pergerakan profit harian menunjukkan angka yang fluktuatif dengan puncak keuntungan tertinggi tercatat pada tanggal **1 dan 21**.

---

## 💡 Rekomendasi Bisnis (Actionable Insights)
Berdasarkan temuan di atas, rekomendasi untuk kuartal berikutnya adalah:
1. **Strategi Restock:** Memprioritaskan pengadaan stok untuk jersey **Paris Saint-Germain** guna menghindari *stock-out* pada produk dengan margin keuntungan terbaik.
2. **Apresiasi & Evaluasi SDM:** Memberikan insentif kepada **Andi T.** untuk menjaga performa, serta mengadakan *knowledge sharing* ke setiap cabang yang kontribusi penjualannya masih paling rendah, yaitu **Surabaya**.

---

## 🚀 Cara Menjalankan Proyek (How to Run)
1. *Clone* repositori ini.
2. Pastikan file `data_capstone_RetailSales.csv` berada di folder `data_raw/`.
3. Jalankan `01_Data_Cleaning.ipynb` terlebih dahulu untuk memproses data.
4. Jalankan `02_Data_Visualization.ipynb` untuk merender grafik EDA.

---
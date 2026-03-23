# ⚽ Retail Sales & Profitability Analysis: Unlocking Business Value from Messy POS Data

## 📌 Latar Belakang & Tujuan Bisnis
Data transaksi dari sistem kasir (*Point of Sales*) di industri ritel sering kali kotor dan tidak konsisten akibat proses input manual. Proyek ini bertujuan untuk membersihkan data mentah tersebut dan mengubahnya menjadi *insight* bisnis yang berharga untuk mengevaluasi performa penjualan, profitabilitas produk, dan tren keuntungan.

## 🗄️ Sumber Data & Kamus Data
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

## 🧹 Part 1: Pembersihan Data (Data Cleaning)
Dataset awal memiliki berbagai anomali. Penanganan tingkat lanjut yang dilakukan meliputi:
- **Advanced Text Mapping:** Menggunakan fungsi *custom* bersarang (*nested if-elif-else*) untuk mendeteksi dan menyamakan berbagai variasi input nama produk yang berantakan menjadi nama klub standar (yang bersih).
- **Complex Regex & Currency Parsing:** Menggunakan *Regular Expression* (`regex=True`) untuk menghapus satuan teks ("pcs", "unit"), serta fungsi `.apply()` untuk mengonversi format mata uang Indonesia ("Juta", "K", "Rp", "IDR") menjadi numerik.
- **Imputation:** Mengisi data kuantitas penjualan yang kosong (*NaN*) dengan nilai *Median*.

---

## 🖼️ Dashboard Visualisasi (Dashboard Visualization)

---

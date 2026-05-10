# Delivery Business Intelligence Project 🚚📊

## 📌 Project Overview
Project ini merupakan implementasi **Business Intelligence (BI)** dan **Data Warehouse** menggunakan dataset delivery dari Kaggle.  
Tujuan utama project adalah menganalisis performa layanan delivery berdasarkan berbagai faktor seperti kota, cuaca, traffic, dan waktu pengiriman.

Project ini mencakup proses:
- Extract, Transform, Load (ETL)
- Data Cleaning
- Data Warehouse Design
- SQL Analysis
- Data Visualization
- Business Insight

---

# 🎯 Project Objectives

- Mengimplementasikan proses ETL (Extract, Transform, Load) pada dataset food delivery.
- Melakukan data cleaning dan transformasi data menggunakan Python dan Google Colab.
- Membangun Data Warehouse sederhana menggunakan MySQL.
- Melakukan analisis data untuk mendapatkan insight terkait performa layanan delivery.
- Menggunakan query SQL untuk mendukung proses analisis data.
- Menyajikan hasil analisis dalam bentuk visualisasi data.
- Mengelola dan mendokumentasikan project menggunakan GitHub.

---

# 🔗 Important Links

### 📓 Notebook: https://colab.research.google.com/drive/1AZC9EbT7TIynGbE3Dleai4UOA1eXClnG?usp=sharing

### 📂 Dataset Source: https://www.kaggle.com/datasets/vananhtong/food-delivery-dataset/data

### 🌐 GitHub Repository: https://github.com/USERNAME/REPOSITORY-NAME

---

# 📂 Dataset
Dataset yang digunakan berasal dari Kaggle:


Dataset berisi informasi mengenai:
- Driver delivery
- Waktu pengiriman
- Kondisi cuaca
- Kepadatan lalu lintas
- Lokasi delivery
- Rating driver
- Jenis kendaraan
- Tipe order

---

# 🛠 Tools & Technologies

| Tools | Fungsi |
|---|---|
| Python (Pandas) | Data Cleaning & ETL |
| Google Colab | Data Processing |
| MySQL | Data Warehouse |
| GitHub | Version Control |

---

# 🔄 ETL Process

## 1. Extract
Dataset diambil dari Kaggle dalam format CSV.

## 2. Transform
Tahap transformasi meliputi:
- Menghapus missing value
- Mengubah format tanggal
- Menambahkan kolom Month dan Hour
- Membersihkan tipe data
- Mengelompokkan data berdasarkan kebutuhan analisis

## 3. Load
Data hasil cleaning dimasukkan ke dalam Data Warehouse menggunakan pendekatan **Star Schema**.

---

# ⭐ Data Warehouse Design

## Fact Table
### fact_delivery
Menyimpan data utama transaksi delivery:
- delivery_id
- customer_id
- location_id
- time_id
- delivery_time
- total_order

---

## Dimension Tables

### dim_customer
Informasi customer.

### dim_location
Informasi kota dan lokasi delivery.

### dim_time
Informasi waktu seperti hari, bulan, tahun, dan jam.

---

# 📊 Data Analysis

## 🌆 Kota dengan Order Terbanyak
Menganalisis kota dengan jumlah order delivery tertinggi.

### Insight
Kota dengan jumlah order tertinggi menunjukkan tingkat permintaan layanan delivery yang lebih besar dibanding kota lainnya.

---

## ⏰ Peak Hour Delivery
Menganalisis jam tersibuk dalam layanan delivery.

### Insight
Order paling banyak terjadi pada jam makan siang dan malam.

---

## 🚚 Average Delivery Time

### Result
Rata-rata delivery time:
26.63 menit

### Insight
Waktu pengiriman menunjukkan performa layanan delivery yang cukup efisien.

---

## 🌧️ Weather vs Delivery Time

### Insight
Cuaca buruk cenderung meningkatkan waktu delivery.

---

## 🚦 Traffic Density vs Delivery Time

### Insight
Semakin tinggi traffic density, semakin lama waktu pengiriman.

---

## ⭐ Driver Rating vs Delivery Time

### Insight
Driver dengan rating tinggi cenderung memiliki waktu pengiriman yang lebih stabil.

---

# 📈 Visualization
Visualisasi data dibuat menggunakan:
- Bar Chart
- Line Chart
- Scatter Plot
- Histogram

Dashboard digunakan untuk membantu proses pengambilan keputusan bisnis.

---

# 🗂 Project Structure

```bash
delivery-business-intelligence/
│
├── dataset/
│   └── clean_delivery_data.csv
│
├── notebook/
│   └── delivery_analysis.ipynb
│
├── sql/
│   └── delivery_dw.sql
│
└── README.md
```

---

# 💾 SQL Analysis Example

## Total Order per City

```sql
SELECT city, COUNT(*) AS total_order
FROM delivery_data
GROUP BY city
ORDER BY total_order DESC;
```

---

## Average Delivery Time

```sql
SELECT AVG(delivery_time) AS avg_delivery
FROM delivery_data;
```

---

# 🚀 Business Insight
Berdasarkan hasil analisis, faktor seperti cuaca dan kepadatan lalu lintas memiliki pengaruh terhadap efisiensi delivery. Selain itu, jam makan siang dan malam menjadi waktu dengan jumlah order tertinggi sehingga perusahaan perlu melakukan optimalisasi distribusi driver pada jam-jam tersebut.

---

# 👥 Team Members
1. Dafa Firdaus
2. Muhamamd Romadhoni Alfatih  
3. Muhammad Rifqi Jastiartha


---

# 📌 Conclusion
Implementasi Business Intelligence dan Data Warehouse membantu proses analisis data delivery menjadi lebih terstruktur, cepat, dan informatif sehingga dapat mendukung pengambilan keputusan bisnis secara lebih efektif.

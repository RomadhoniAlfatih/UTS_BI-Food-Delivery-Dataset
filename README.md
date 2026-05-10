# UTS_BI-Food-Delivery-Dataset

Delivery Business Intelligence Project 🚚📊
📌 Project Overview
Project ini merupakan implementasi Business Intelligence (BI) dan Data Warehouse menggunakan dataset delivery dari Kaggle.
Tujuan utama project adalah menganalisis performa layanan delivery berdasarkan berbagai faktor seperti kota, cuaca, traffic, dan waktu pengiriman.
Project ini mencakup proses:


Extract, Transform, Load (ETL)


Data Cleaning


Data Warehouse Design


SQL Analysis


Data Visualization


Business Insight



📂 Dataset
Dataset yang digunakan berasal dari Kaggle:
Food Delivery Dataset Kaggle
Dataset berisi informasi mengenai:


Driver delivery


Waktu pengiriman


Kondisi cuaca


Kepadatan lalu lintas


Lokasi delivery


Rating driver


Jenis kendaraan


Tipe order



🛠 Tools & Technologies
Project ini menggunakan beberapa tools berikut:
ToolsFungsiPython (Pandas)Data Cleaning & ETLGoogle ColabData ProcessingMySQLData WarehousePower BIDashboard VisualizationGitHubVersion Control

🔄 ETL Process
1. Extract
Dataset diambil dari Kaggle dalam format CSV.
2. Transform
Tahap transformasi meliputi:


Menghapus missing value


Mengubah format tanggal


Menambahkan kolom Month dan Hour


Membersihkan tipe data


Mengelompokkan data berdasarkan kebutuhan analisis


3. Load
Data hasil cleaning dimasukkan ke dalam Data Warehouse menggunakan pendekatan Star Schema.

⭐ Data Warehouse Design
Fact Table
fact_delivery
Menyimpan data utama transaksi delivery:


delivery_id


customer_id


location_id


time_id


delivery_time


total_order



Dimension Tables
dim_customer
Informasi customer.
dim_location
Informasi kota dan lokasi delivery.
dim_time
Informasi waktu seperti hari, bulan, tahun, dan jam.

📊 Data Analysis
Beberapa analisis yang dilakukan:
🌆 Kota dengan Order Terbanyak
Menganalisis kota dengan jumlah order delivery tertinggi.
Insight
Kota dengan jumlah order tertinggi menunjukkan tingkat permintaan layanan delivery yang lebih besar dibanding kota lainnya.

⏰ Peak Hour Delivery
Menganalisis jam tersibuk dalam layanan delivery.
Insight
Order paling banyak terjadi pada jam makan siang dan malam.

🚚 Average Delivery Time
Menghitung rata-rata waktu pengiriman.
Result
Rata-rata delivery time:
26.63 menit
Insight
Waktu pengiriman menunjukkan performa layanan delivery yang cukup efisien.

🌧️ Weather vs Delivery Time
Menganalisis pengaruh cuaca terhadap waktu pengiriman.
Insight
Cuaca buruk cenderung meningkatkan waktu delivery.

🚦 Traffic Density vs Delivery Time
Menganalisis pengaruh kepadatan lalu lintas terhadap delivery.
Insight
Semakin tinggi traffic density, semakin lama waktu pengiriman.

⭐ Driver Rating vs Delivery Time
Menganalisis hubungan rating driver dengan performa delivery.
Insight
Driver dengan rating tinggi cenderung memiliki waktu pengiriman yang lebih stabil.

📈 Visualization
Visualisasi data dibuat menggunakan:


Bar Chart


Line Chart


Scatter Plot


Histogram


Dashboard digunakan untuk membantu proses pengambilan keputusan bisnis.

🗂 Project Structure
delivery-business-intelligence/│├── dataset/│   └── clean_delivery_data.csv│├── notebook/│   └── delivery_analysis.ipynb│├── sql/│   └── delivery_dw.sql│├── dashboard/│   └── powerbi_dashboard.png│├── laporan/│   └── laporan_project.pdf│└── README.md

💾 SQL Analysis Example
Total Order per City
SELECT city, COUNT(*) AS total_orderFROM delivery_dataGROUP BY cityORDER BY total_order DESC;

Average Delivery Time
SELECT AVG(delivery_time) AS avg_deliveryFROM delivery_data;

🚀 Business Insight
Berdasarkan hasil analisis, faktor seperti cuaca dan kepadatan lalu lintas memiliki pengaruh terhadap efisiensi delivery. Selain itu, jam makan siang dan malam menjadi waktu dengan jumlah order tertinggi sehingga perusahaan perlu melakukan optimalisasi distribusi driver pada jam-jam tersebut.

👥 Team Members


Dafa Firdaus


Muhammad Romadhoni Alfatih


Muhammad Rifqi Jastiartha



📌 Conclusion
Implementasi Business Intelligence dan Data Warehouse membantu proses analisis data delivery menjadi lebih terstruktur, cepat, dan informatif sehingga dapat mendukung pengambilan keputusan bisnis secara lebih efektif.

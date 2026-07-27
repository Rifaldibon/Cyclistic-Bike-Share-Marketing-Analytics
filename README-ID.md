# Analitik Marketing Cyclistic Bike-Share: Menganalisis Perilaku Pengguna untuk Meningkatkan Membership

---
## Ringkasan Proyek
### Skenario

Anda adalah analis data junior yang bekerja di tim analis marketing Cyclistic, sebuah perusahaan bike-share di Chicago. Direktur pemasaran percaya bahwa kesuksesan masa depan perusahaan tergantung pada memaksimalkan jumlah membership. Oleh karena itu, tim Anda ingin memahami perbedaan antara pengguna kasual dan pengguna membership dalam menggunakan sepeda Cyclistic. Dari wawasan ini, tim Anda akan merancang strategi pemasaran baru untuk mengonversi pengguna kasual menjadi member. Namun, eksekutif dari Cyclistic harus menyetujui rekomendasi anda terlebih dahulu, sehingga rekomendasi anda harus didukung dengan wawasan yang menarik dan visualisasi data yang profesional.

### Tim

| Tim | Deskripsi |
| :--- | :---|
| **Cyclistic** | Program bike-share yang menampilkan lebih dari 5.800 sepeda dan 600 stasiun docking. |
| **Lily Moreno** | Direktur pemasaran dan manajer kami. Moreno bertanggung jawab atas pengembangan kampanye dan inisiatif untuk mempromosikan program bike-share. |
| **Tim analitik pemasaran Cyclistic** | Tim analis data yang bertanggung jawab atas pengumpulan, analisis, dan pelaporan data yang membantu memandu strategi pemasaran Cyclistic. (Tim saya) |
| **Tim eksekutif Cyclistic** | Tim eksekutif yang terkenal detail-oriented akan memutuskan apakah mereka akan menyetujui program pemasaran yang direkomendasikan. |

### Durasi Proyek

Proyek dikerjakan dari tanggal **20 Juli 2026** hingga **26 Juli 2026**. <br>
Proyek selesai dalam **6 hari**.

---

![Dashboard Tableau](dashboard/dashboard_overview.png)

## 📌 Executive Summary
Cyclistic adalah program bike-share di Chicago yang menampilkan lebih dari 5.800 sepeda dan 600 stasiun docking. Proyek ini menganalisis **lebih dari 5,24 juta catatan perjalanan** yang mencakup periode **Juli 2025 hingga Juni 2026** untuk memahami perbedaan antara **Member** dan **Pengguna Kasual** dalam menggunakan sepeda. Tujuan bisnis utama dari proyek ini adalah merancang strategi pemasaran berbasis data untuk mengonversi Pengguna Kasual menjadi Member.

## 📊 Interactive Dashboard Showcase

### 1. Full Dashboard Overview
![Ikhtisar Dashboard Cyclistic](dashboard/dashboard_overview.png)

### 2. Interactive Filtering Demo
![Demo Interaktivitas Dashboard](dashboard/visualization.gif)

> 💡 **Catatan:** Anda dapat mengunduh file Tableau Packaged Workbook [`visualization.twbx`](dashboard/visualization.twbx) dari repositori ini untuk menjelajahi semua grafik yang dikerjakan dan elemen interaktif secara native di Tableau Reader atau Tableau Desktop.

---

## 🛠️Tech Stack & Metode

* **Data Processing & Cleaning:** Python (`Pandas`, `NumPy`)
* **Spatial Imputation (Machine Learning):** Scikit-Learn (`BallTree` menggunakan Haversine distance)
* **Statistical Filtering:** Interquartile Range (IQR) untuk deteksi outlier di durasi perjalanan
* **Data Visualization:** Tableau Desktop
---

## 📊 Temuan Utama & Wawasan

### 1. User Volume & Duration Trade-off
* **Pengguna Membership** mendominasi penggunaan sepeda secara keseluruhan, menyumbang **66,6% (3,49 juta perjalanan)** dari total perjalanan.
* **Pengguna Kasual** menyumbang **33,4% (1,75 juta perjalanan)**, tetapi menghabiskan waktu **16,6% lebih lama** per perjalanan (rata-rata 12,29 menit) dibandingkan dengan pengguna membership (rata-rata 10,54 menit).

### 2. Pola Perilaku (Komuter vs. Rekreasi)
* **Peak Days:** Pengguna membership mencapai puncaknya pada hari kerja (**Selasa - Kamis**), sedangkan perjalanan kasual melonjak **+75% pada akhir pekan** (puncak pada Sabtu dengan 354,8 ribu perjalanan).
* **Peak Hours:** Pengguna membership menunjukkan **pola komuter bimodal** yang mencapai puncak pada jam **08:00 AM** dan **05:00 PM**. Sedangkan pengguna kasual menampilkan **tren unimodal** yang halus dimana mencapai puncak antara jam **12:00 PM - 05:00 PM**.

### 3. Musim & Preferensi Sepeda
* **Musim:** Perjalanan kasual sangat sensitif terhadap cuaca, menurun drastis sebanyak **-91,7%** selama musim dingin (Januari 2026) dibandingkan dengan puncak musim panas (Juli/Agustus 2025).
* **Permintaan E-Bike:** Pengguna kasual menunjukkan preferensi yang lebih kuat untuk penggunaan **Sepeda Listrik (72,5%)** dibanding Sepeda Klasik.
* **Hotspot:** Perjalanan pengguna kasual sangat terkonsentrasi di area wisata dan pantai, dengan **Navy Pier** dan **DuSable Lake Shore Drive** sebagai stasiun teratas.

---

## 💡 Rekomendasi Strategis (Tahap Bertindak)

1. **Pengiklanan di Akhir Pekan saat Musim Panas:**
   * Terapkan iklan digital dan booth promosi fisik di hotspot teratas atau stasiun dimana pengguna Kasual paling banyak menyewa sepeda (**Navy Pier**, **DuSable Lake Shore Drive**) setiap akhir pekan di puncak musim panas (**Mei - Agustus**), menekankan dengan menjadi member dapat menghemat biaya.

2. **Tingkat Keanggotaan Musiman:**
   * Perkenalkan **"Summer Pass"** atau **"Weekend Pass"** yang disesuaikan untuk pengguna untuk kebutuhan rekreasi, menampilkan juga opsi untuk dapat upgrade secara otomatis ke pengguna member utama.

3. **Insentif Loyalitas Penggunaan E-Bike:**
   * Manfaatkan preferensi kasual yang tinggi untuk penggunaan e-bike (72,5%) dengan menawarkan penghapusan biaya untuk buka kunci e-bike dan diskon tarif penggunaan e-bike per menit jika menjadi member.

---

## ⚙️ How to Reproduce

1. Clone repositori ini: `git clone https://github.com/Rifaldibon/Cyclistic-Bike-Share-Marketing-Analytics.git`
2. Jalankan skrip data preparation: `notebooks/prepare.ipynb`
3. Jalankan pipeline ML imputation dan pembersihan data: `notebooks/process.ipynb`
4. Load file `bike_trip_data_clean(July 2025-June 2026).csv` yang dihasilkan ke dalam Tableau.

---

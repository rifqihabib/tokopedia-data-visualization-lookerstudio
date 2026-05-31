# tokopedia-data-visualization-lookerstudio
Dokumentasi dan analisis visualisasi data e-commerce Tokopedia (2021-2022) menggunakan Google Looker Studio untuk memantau Marketing Campaign, Performa Produk, dan Distribusi Pembayaran.
# 📊 Tokopedia Data Visualization — Looker Studio Final Project

Repository ini berisi portofolio proyek akhir (*Final Project*) visualisasi data menggunakan **Google Looker Studio**, sebagai bagian dari program Data Analyst di MySkill. Analisis dilakukan pada dataset transaksi e-commerce **Tokopedia** periode tahun 2021 s.d. 2022 untuk menyajikan laporan interaktif bisnis bagi pihak manajemen.

---

## 👥 Anggota Kelompok 4B
* Muhammad Fathi Rizqi
* Rifqi Habib
* Farid Ilham Nugrahatta
* Brigita Adven Novani
* Siti Aisyah Bintang Larasati
* Godefriedo Dimas Putra Brata
* Yohanes Dimas Pratama
* Dini Desita
* Ajeng Listya Devani
* Imam Afdol Hakiki Bakri
* Mohamad Nizar Ajiyansya
* Anugerah Putra Pratama
* Naura Fatin
* Muhammad Hibban

---

## 🛠️ Penyiapan Data & Indikator Kalkulasi (Calculated Field)

Sebelum visualisasi dirancang, seluruh berkas data mentah (*Order, Customer, Payment,* dan *SKU Details*) dihubungkan ke Looker Studio. Untuk memenuhi kebutuhan metrik pemantauan manajemen, dibuat 2 indikator kalkulasi baru (*Calculated Field*):

1. **Net Profit** (Mengukur laba bersih perusahaan):
   $$\text{Net Profit} = \text{SUM}(before\_discount) - \text{SUM}(cogs \times qty\_ordered)$$

2. **AOV (Average Order Value)** (Mengetahui rata-rata nilai belanja per transaksi):
   $$\text{AOV} = \frac{\text{SUM}(before\_discount)}{\text{COUNT\_DISTINCT}(id)}$$

---

## 📉 Dashboard Halaman 1: Performa Kampanye Pemasaran (Marketing Campaign)

Halaman pertama berfokus untuk memantau hubungan antara total penjualan harian (*Value Sales*), keuntungan bersih (*Net Profit*), dan rata-rata nilai transaksi (*AOV*) sepanjang tahun 2022.

* **Ringkasan Angka Kunci (Scorecard 2022):**
    * **Value Sales (Before Discount):** 5.1 M
    * **Net Profit:** 1.1 M
    * **Average Order Value (AOV):** 1.6 M
* **Analisis Grafik Kontrol Harian:** Penjualan melonjak sangat tajam pada bulan **April, Agustus, dan September**. Bulan September mencatatkan nilai AOV tertinggi, menandakan transaksi didominasi oleh produk bernilai tinggi. Namun, performa mengalami penurunan drastis di kuartal akhir (Q4: Oktober - Desember).

> 🔗 **Tautan Akses Dashboard:** https://datastudio.google.com/reporting/a79bd5b0-424b-4f91-a314-d2f1fdf9fc63

---

## 🛍️ Dashboard Halaman 2: Performa Produk & Distribusi Pembayaran

Halaman kedua menyajikan papan peringkat performa produk secara mendetail serta pemetaan perilaku transaksi konsumen.

* **Papan Peringkat Produk (Leaderboard):** Kategori *Mobiles & Tablets* menjadi penggerak utama bisnis dengan total kuantitas produk terjual mencapai **2,4 ribu unit**, disusul oleh kategori *Soghaat* sebesar 1,2 ribu unit. Produk **IDROID BALRXT-Gold** tercatat sebagai penyumbang keuntungan bersih tertinggi.
* **Metode Pembayaran (Distribution):** Metode **COD (Cash on Delivery)** masih mendominasi mutlak dengan proporsi sebesar **48.2%** dari total preferensi transaksi pelanggan, diikuti oleh metode pembayaran lainnya sebesar 24.8%.

> 🔗 **Tautan Akses Dashboard:** https://datastudio.google.com/reporting/a79bd5b0-424b-4f91-a314-d2f1fdf9fc63

---

## 💡 Temuan Utama (Insights) & Rekomendasi Strategis Bisnis

1. **Edukasi Keamanan Pembayaran Digital:** Mengingat tingginya ketergantungan pelanggan pada metode COD (48.2%), perusahaan perlu mengedukasi konsumen mengenai kemudahan transaksi nontunai serta memberikan promo/diskon khusus pengguna e-wallet/bank transfer.
2. **Program Bundling Antar-Kategori:** Performa volume penjualan sangat didominasi oleh kategori *Mobiles & Tablets* (2,4 ribu unit). Disarankan membuat program bundling paket hemat (misal: menyilangkan produk gadget dengan kategori *Fashion* atau *Kids*) untuk mendongkrak kategori yang kurang diminati.
3. **Strategi Up-selling & Cross-selling:** Menerapkan taktik rekomendasi produk pelengkap saat checkout guna meningkatkan nilai transaksi per pelanggan (*Average Order Value*).
4. **Strategi Retargeting untuk Pelanggan Lama:** Menjalankan iklan terarah (*retargeting*) lewat email promo, notifikasi diskon keranjang, atau voucer khusus pelanggan lama untuk mendorong terjadinya pembelian berulang (*repeat purchase*).

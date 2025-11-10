# ⚽ Sistem Penyewaan Lapangan Futsal

<p align="center">
  <b>🧩 Framework:</b> Laravel + Livewire + Alpine.js  
</p>

---

## 🧑‍🤝‍🧑 1. Aktor & Peran dalam Sistem Informasi Penyewaan Lapangan Futsal

### 👨‍💼 A. Admin (Pemilik/Pengelola)
**Peran Utama:** Mengelola seluruh operasional sistem  

**Tanggung Jawab:**
- Mengelola data lapangan dan jadwal  
- Mengkonfirmasi pesanan penyewaan  
- Memproses pembayaran  
- Menghasilkan laporan transaksi  
- Memelihara sistem dan data  

---

### 🧍‍♂️ B. User (Pelanggan/Penyewa)
**Peran Utama:** Menggunakan sistem untuk menyewa lapangan  

**Tanggung Jawab:**
- Melakukan registrasi dan login  
- Memesan lapangan sesuai jadwal yang diinginkan  
- Melakukan pembayaran  
- Mengelola reservasi pribadi  

**Interaksi Antar Aktor:**
- Admin berinteraksi dengan sistem untuk mengelola data dan mengkonfirmasi pesanan  
- User berinteraksi dengan sistem untuk booking dan pembayaran  
- Admin memverifikasi dan memproses permintaan dari user  

---

## 🔄 2. Alur Proses Sistem Penyewaan Lapangan Futsal

### 🧍 Alur Proses untuk User (Pelanggan)

#### 🪪 Tahap 1: Akses Sistem
1. User membuka halaman web sistem penyewaan  
2. Melakukan login dengan username dan password  
3. Sistem memverifikasi kredensial user  

#### 📅 Tahap 2: Pemesanan Lapangan
1. User memilih halaman booking/pemesanan  
2. Mengisi form pemesanan dengan data:
   - Nama pemesan  
   - Nomor telepon  
   - Tanggal bermain  
   - Jam mulai  
   - Jam selesai  
3. Sistem mengecek ketersediaan lapangan  

#### 💳 Tahap 3: Konfirmasi dan Pembayaran
1. Sistem menampilkan detail pesanan dan total biaya  
2. User melakukan pembayaran via transfer (DP atau lunas)  
3. Sistem memproses transaksi pembayaran  

#### ✅ Tahap 4: Konfirmasi Pesanan
1. Sistem mengirim konfirmasi pesanan  
2. Data pesanan tersimpan dalam database  

---

### 🧑‍💼 Alur Proses untuk Admin

#### 🔐 Tahap 1: Login Admin
1. Admin login ke sistem dengan kredensial khusus  
2. Mengakses dashboard admin  

#### 🗂️ Tahap 2: Pengelolaan Data
- Mengelola data lapangan dan jadwal  
- Mengatur tarif penyewaan  
- Memelihara master data sistem  

#### 📬 Tahap 3: Konfirmasi Pesanan
- Menerima notifikasi pesanan baru  
- Memverifikasi ketersediaan lapangan  
- Mengkonfirmasi atau menolak pesanan  

#### 📊 Tahap 4: Laporan dan Monitoring
- Menghasilkan laporan transaksi  
- Monitoring penggunaan lapangan  
- Rekap pendapatan  

---

## 💾 3. Data Input-Output Sistem

### 📥 Data Input

#### 🧍 A. Input dari User/Pelanggan
- **Data Registrasi:** Username, password, nama lengkap, email, nomor telepon  
- **Data Pemesanan:**
  - Nama pemesan  
  - Nomor telepon kontak  
  - Tanggal penyewaan  
  - Jam mulai bermain  
  - Jam selesai bermain  
  - Pilihan lapangan (jika ada beberapa)  
- **Data Pembayaran:** Informasi pembayaran dan konfirmasi transfer  

#### 🧑‍💼 B. Input dari Admin
- **Data Lapangan:** Nama lapangan, fasilitas, tarif per jam  
- **Data Jadwal:** Pengaturan jam operasional, hari libur  
- **Konfirmasi Pesanan:** Persetujuan atau penolakan booking  
- **Data Tarif:** Penetapan harga sewa per jam atau paket  
- **Data Event (jika ada)**  

---

### 📤 Data Output

#### 🧍 A. Output untuk User/Pelanggan
- **Halaman Booking:** Tampilan form pemesanan dengan validasi  
- **Konfirmasi Pesanan:** Detail pemesanan, total biaya, dan instruksi pembayaran  
- **Status Pesanan:** Informasi apakah pesanan dikonfirmasi atau ditolak  
- **Riwayat Transaksi:** History pemesanan sebelumnya  

#### 🧑‍💼 B. Output untuk Admin
- **Dashboard Admin:** Ringkasan aktivitas harian, mingguan, bulanan  
- **Laporan Transaksi:**
  - Data pelanggan yang menyewa  
  - Jadwal penggunaan lapangan  
  - Total pendapatan per periode  
  - Statistik penggunaan lapangan  
- **Daftar Pesanan:** List semua pesanan (pending, confirmed, completed)  
- **Laporan Keuangan:** Summary income dari penyewaan  

---

### 🧠 Karakteristik Data Input-Output

**Input Requirements:**
- ✅ **Validasi Data:** Form input dilengkapi validasi untuk memastikan akurasi  
- ⏰ **Format Waktu:** Standardisasi format tanggal dan jam  
- 🔄 **Ketersediaan Real-time:** Pengecekan langsung ketersediaan jadwal  

---

## 🧩 Diagram & Flowchart

### 🧱 Class Diagram
<p align="center">
  <img src="doc-img/class-diagram.svg" alt="Class Diagram" height="700">
</p>

---

### 🔗 Relasi Antar Tabel
<p align="center">
  <img src="doc-img/relasi-tabel.png" alt="Relasi Antar Tabel" height="700">
</p>

---

### 🧭 Admin Flowchart
<p align="center">
  <img src="doc-img/admin_flow.png" alt="Admin Flowchart" height="700">
</p>

---

### 👥 User Flowchart
<p align="center">
  <img src="doc-img/user_flow.png" alt="User Flowchart" height="700">
</p>

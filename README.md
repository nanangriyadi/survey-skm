# Sistem Survei Kepuasan Masyarakat (SKM) Digital 
**SLB Negeri Badegan Ponorogo**

Sistem web responsif berbasis klien (*client-side*) untuk mengumpulkan, menghitung, dan melaporkan Indeks Kepuasan Masyarakat (IKM) berdasarkan 9 Unsur Pelayanan Publik standar PermenPANRB.

## 🚀 Fitur Utama
- **Kalkulasi SKM Otomatis:** Menghitung Nilai Rata-Rata (NRR) per unsur dan total IKM secara otomatis sesuai bobot tertimbang (0.111).
- **Dashboard Real-time:** Visualisasi data menggunakan grafik batang dan *doughnut chart* interaktif.
- **Ekspor Data:** Kemampuan untuk mengunduh seluruh data responden ke dalam format `.csv` (Microsoft Excel).
- **Laporan Siap Cetak (Print-Ready):** Halaman laporan khusus yang dioptimalkan untuk dicetak menjadi dokumen fisik atau PDF tanpa elemen UI yang mengganggu (Kop Surat otomatis).
- **Keamanan Sesi Sederhana:** Panel Admin dilindungi dengan sistem login berbasis *Local Storage Session*.
- **Mode Gelap/Terang (Dark Mode):** Antarmuka modern yang mendukung penyesuaian tema warna.
- **Database Kiosk Mode:** Menggunakan `localStorage` browser sehingga tidak memerlukan setup server/database backend (Sangat cocok untuk penggunaan *Kiosk* / Tablet di ruang tunggu sekolah).

## 🛠️ Teknologi yang Digunakan
- **HTML5 & CSS3**
- **Tailwind CSS** (via CDN) - *Styling & Layouting*
- **Vanilla JavaScript (ES6)** - *Logic & DOM Manipulation*
- **Chart.js** (via CDN) - *Data Visualization*
- **Web LocalStorage API** - *Data Persistence*

## 📂 Struktur File (Navigasi Halaman)
| Nama File | Deskripsi Fungsi |
| :--- | :--- |
| `index.html` | **Beranda Publik.** Menampilkan informasi SKM, cara pengisian, dan skor transparansi IKM secara *real-time*. |
| `survey.html` | **Formulir Survei.** Halaman tempat responden mengisi identitas, nilai 9 unsur layanan, dan kotak saran. |
| `thankyou.html` | **Halaman Apresiasi.** Tampil setelah responden berhasil mengirimkan survei (dilengkapi animasi *confetti*). |
| `admin-login.html` | **Gerbang Admin.** Halaman login untuk melindungi data panel. |
| `admin-dashboard.html` | **Ringkasan Admin.** Visualisasi IKM, jumlah responden, mutu layanan, dan grafik per unsur. |
| `admin-results.html` | **Tabel Data & Analisis.** Menampilkan tabel detail setiap responden, fitur pencarian, filter mutu, dan tombol Ekspor CSV. |
| `admin-reports.html` | **Pusat Laporan.** Rekapan lengkap data NRR & Saran untuk keperluan cetak/pelaporan resmi dinas. |

## 💻 Cara Instalasi & Penggunaan

Proyek ini murni berbasis Front-End. Anda tidak perlu menginstal Node.js, PHP, atau MySQL.

1. **Unduh/Clone** seluruh file proyek ke dalam satu folder di komputer Anda.
2. Buka folder tersebut.
3. Klik ganda pada file `index.html` untuk membukanya langsung di Browser (Google Chrome / Microsoft Edge / Safari).
4. *Opsional:* Untuk pengalaman terbaik, buka folder menggunakan VS Code dan jalankan ekstensi **Live Server**.

## 🔐 Akses Panel Admin

Untuk masuk ke dalam Dashboard Admin, akses halaman `admin-login.html` atau klik menu "Admin" di pojok kanan atas beranda, lalu gunakan kredensial berikut:

- **Username:** `admin`
- **Password:** `admin123`

## ⚠️ Catatan Penting Tentang Database (LocalStorage)

Aplikasi saat ini menggunakan **`localStorage`** dari browser sebagai tempat penyimpanan data (Database). Ini berarti:
1. **Penyimpanan Lokal:** Data survei disimpan secara eksklusif di browser pada perangkat yang digunakan untuk mengisi. Jika Anda mengisi survei di Laptop A, datanya tidak akan muncul di Laptop B.
2. **Mode Kiosk Ideal:** Sistem ini paling cocok digunakan dengan meletakkan 1 perangkat (misal: iPad / Laptop) di meja resepsionis/ruang tunggu SLB Negeri Badegan. Responden mengisi di alat tersebut, dan Admin mengecek hasilnya di alat yang sama.
3. **Pembersihan Cache:** Hati-hati saat membersihkan *History/Cache* browser, karena opsi *Clear Site Data* dapat ikut menghapus data survei. Lakukan "Ekspor CSV" secara berkala sebagai *backup* (cadangan).

## 🚀 Rencana Pengembangan Lanjutan (Bila Dibutuhkan)
Jika ke depannya SLB Negeri Badegan ingin survei ini bisa diakses secara publik dari HP masing-masing wali murid di rumah (dan data masuk ke komputer Admin di sekolah), kode JavaScript (pada bagian penyimpanan) harus disambungkan dengan layanan *Backend/Database Cloud* seperti:
- **Google Sheets API / Google Forms Backend**
- **Firebase Realtime Database / Firestore**
- **Supabase**

---
*Dikembangkan untuk SLB Negeri Badegan Ponorogo © 2024*

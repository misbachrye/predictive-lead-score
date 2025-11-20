# 🚀 Predictive Lead Scoring Portal (Front-End)

![Project Status](https://img.shields.io/badge/Status-Capstone%20Project-blue)
![Role](https://img.shields.io/badge/Role-Front--End%20Developer-green)
![Tech](https://img.shields.io/badge/Tech-React%20|%20Vite%20|%20Tailwind-06B6D4)

Repository ini berisi kode sumber Front-End untuk **Predictive Lead Scoring Portal**, sebuah aplikasi dashboard yang dirancang untuk membantu tim penjualan (sales) memprioritaskan nasabah potensial berdasarkan skor probabilitas yang diprediksi oleh sistem.

Proyek ini merupakan bagian dari **Capstone Project** tim kami, di mana saya bertanggung jawab penuh atas pengembangan antarmuka pengguna (User Interface) dan integrasi sisi klien.

## 📋 Tentang Proyek

Aplikasi ini berfungsi sebagai portal bagi tim sales untuk:
1.  Melihat daftar prospek (leads) yang sudah diurutkan berdasarkan prioritas.
2.  Menganalisis profil nasabah secara mendetail (demografi, finansial, dll).
3.  Mencatat interaksi harian dengan nasabah.

Tujuan utamanya adalah meningkatkan efisiensi penjualan dengan memfokuskan upaya pada nasabah dengan probabilitas konversi tertinggi.

### 🛠️ Tech Stack

Teknologi yang saya gunakan dalam pengembangan Front-End ini meliputi:

* **Core:** [React.js](https://react.dev/) (v19) dengan [Vite](https://vitejs.dev/) untuk performa build yang cepat.
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) untuk desain antarmuka yang responsif dan modern.
* **Routing:** [React Router DOM](https://reactrouter.com/) (v7) untuk manajemen navigasi halaman spa (Single Page Application).
* **HTTP Client:** [Axios](https://axios-http.com/) untuk komunikasi API dan manajemen token.
* **Mock Backend:** [JSON Server](https://github.com/typicode/json-server) untuk simulasi REST API, database, dan autentikasi selama masa pengembangan.

## ✨ Fitur Utama (Kontribusi Saya)

Sebagai Front-End Developer, saya mengimplementasikan fitur-fitur berikut:

### 1. Otentikasi & Keamanan
* **Halaman Login:** Validasi input username dan password.
* **Proteksi Rute:** Menggunakan `AuthGuard` (logika di `App.jsx`) untuk mencegah akses dashboard tanpa login.
* **Manajemen Sesi:** Penyimpanan token simulasi dan data user di `localStorage`.

### 2. Dashboard Interaktif
* **Data Visualization:** Menampilkan daftar leads dalam tabel yang bersih dan informatif.
* **Pencarian Real-time:** Mencari nasabah berdasarkan nama secara langsung.
* **Sorting Cerdas:** Fitur untuk mengurutkan data berdasarkan:
    * Probability Score (Tertinggi ke Terendah / Sebaliknya).
    * Pekerjaan (Job) secara alfabetis.

### 3. Detail Nasabah & Manajemen Catatan
* **Profil Lengkap:** Menampilkan data nasabah yang terbagi dalam kartu informasi (*Key Info, Demographic, Financial, Campaign*).
* **Sistem Catatan (Notes):** Fitur interaktif untuk sales menambahkan catatan follow-up yang tersimpan langsung ke database mock.

## 📂 Struktur Folder

Berikut adalah struktur folder utama yang saya kerjakan:

```
frontend/
├── mock-server/               # Simulasi Backend API
│   ├── db.json                # Database mock (Leads & Notes)
│   └── server.js              # Custom server (auth routes)
│
├── predictive-lead-score/
│   ├── src/
│   │   ├── api/               # API Services (authService.js, leadService.js)
│   │   ├── components/        # UI Components (InfoCard, LeadTable, TopBar)
│   │   ├── pages/             # Pages (LoginPage, DashboardPage, CustomerDetail)
│   │   └── App.jsx            # Routing configuration
│   └── ...config files        # Vite, ESLint, Tailwind, etc.

```
## 🚀 Cara Menjalankan Proyek

Karena proyek ini menggunakan **Mock Server** terpisah untuk mensimulasikan backend, Anda perlu menjalankan **dua terminal** secara bersamaan.

### Prasyarat
Pastikan **Node.js** telah terinstal di komputer Anda.

### 1. Clone Repository
```bash
git clone https://github.com/misbachrye/predictive-lead-score.git
```

### 2. Jalankan Mock Server (Terminal 1)
Server ini berjalan di port 5000 dan menangani data JSON serta login.

```bash

cd mock-server
npm install
npm start
Output: "JSON Server with custom login is running on port 5000".
```

### 3. Jalankan Aplikasi React (Terminal 2)
Aplikasi Front-End akan berjalan (biasanya di port 5173).

```bash

cd predictive-lead-score
npm install
npm run dev
```

### 4. Akses Aplikasi
Buka browser dan akses URL yang muncul di terminal (biasanya http://localhost:5173).

Gunakan kredensial berikut untuk login:

Username: sales_user_01

Password: password123

(Kredensial ini dikonfigurasi dalam mock-server/server.js).
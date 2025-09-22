# Panduan Proyek PKL-App

Proyek ini dibuat menggunakan **React** dengan struktur modular agar mudah dikembangkan beberapa orang secara bersamaan.  

---

## 1️⃣ Clone Repository

1. Pastikan Git sudah terinstall di komputer:
```bash
git --version

2. Clone repository:
git clone https://github.com/username/nama-repo.git
cd nama-repo

3. Install semua dependencies:
npm install

4. Jalankan proyek:
npm start

## 2️⃣ Panduan Berkolaborasi

1.Membuat Branch Baru
Sebelum mengubah kode, buat branch baru untuk fitur yang akan dikerjakan: git checkout -b nama-fitur
Contoh : git checkout -b tambah-login

2. Melakukan Perubahan dan Commit
 - Edit atau tambah file di proyek (misal Login.jsx).
 - Stage file yang diubah:
   git add .
 - Commit perubahan dengan pesan jelas:
   git commit -m "Tambah validasi login"

3. Push Branch ke GitHub
git push -u origin nama-fitur

4. Setelah di review (SKIP bagian ini jika belum di review) 
Pull Request (PR)
- Buka GitHub → repo → akan muncul tombol Compare & pull request
- Buat PR untuk menggabungkan branch ke main
- Setelah review dan merge, branch bisa dihapus:
  git branch -d nama-fitur         # hapus lokal
  git push origin --delete nama-fitur  # hapus di GitHub

## 3️⃣ Struktur Folder Modular
src/
├─ admin/            # Buat folder masing-masing role seperti ini
│  ├─ components/     # untuk tempat menyimpan code fitur yang nantinya bisa dipakai di semua page
│  │  ├─ DashboardCard.jsx
│  │  ├─ Sidebar.jsx
│  │  └─ Header.jsx
│  └─ dashboard_admin_jurusan.jsx      # halaman CRUD jurusan
|  └─ dashboard_admin.jsx     # halaman utama admin
│
├─ login/              
│  ├─ components/
│  │  ├─ MouseRippleButton.jsx
│  │  └─ Sidebar.jsx
│  └─ Login.jsx    
│
├─ utils/
│  └─ authHelper.js          # Fungsi login, logout, refresh token, token
│  └─ axiosInstance.js       # konfigurasi request API
|  └─ crypto.js              # Enkripsi & deskripsi token
│


## 4️⃣ Aturan Penambahan Fitur
1. Jika fitur spesifik role, taruh di folder roles/<role>/components/.
2. Jika komponen reusable bisa taruh di folder src/components/ agar bisa dipakai semua role.
3. Jangan buat fitur yang sama di beberapa folder role → cukup panggil dari components yang sudah ada.
4. Halaman utama tiap role tinggal import components yang dibutuhkan:
import Sidebar from './components/Sidebar';
import DashboardCard from './components/DashboardCard';

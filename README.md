# 🐳 KEL3_SBTA 

Proyek ini merupakan arsitektur aplikasi berbasis Docker yang terdiri dari tiga bagian utama:
- **Frontend**
- **Backend**
- **Service pendukung** (PHP, MySQL, Nginx) melalui Docker

---

## 📦 Struktur Folder

KEL3_SBTA/
├── backend/ # Kode backend (API)
├── frontend/ # Kode frontend (UI)
├── docker/ # Konfigurasi service docker (php, nginx, mysql)
├── docker-compose.yml # File utama untuk orkestrasi container
├── Dockerfile # Instruksi build image
└── README.md # Dokumentasi proyek

---

## 🚀 Cara Menjalankan Proyek

Pastikan Anda sudah menginstall:
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### 1. Clone repositori (jika belum)
```bash
git clone <url-repo> frontend
git clone <url-repo> backend
cd KEL3_SBTA

### 2. Jalankan dengan Docker Compose
```bash
docker-compose up --build

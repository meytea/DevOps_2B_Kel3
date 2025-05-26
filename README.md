# 🐳 KEL3_SBTA 

Proyek ini merupakan arsitektur aplikasi berbasis Docker yang terdiri dari tiga bagian utama:
- **Frontend**
- **Backend**
- **Service pendukung** (PHP, MySQL, Nginx) melalui Docker

---

## 📦 Struktur Folder
```bash
KEL3_SBTA/
│
├── backend/
│   └── ...                # Kode backend \
│
├── frontend/
│   └── ...                # Kode frontend 
│
├── docker/
│   ├── mysql/
│   │   ├── init.sql       # SQL untuk inisialisasi database (opsional)
│   │   └── Dockerfile     # Optional: jika ingin kustomisasi image MySQL
│   │
│   ├── nginx/
│   │   └── default.conf   # Konfigurasi reverse proxy Nginx
│   │
│   └── php/
│       └── Dockerfile     # Image PHP, biasanya berisi Apache + PHP
│
├── docker-compose.yml
└── Dockerfile             # Kalau ini tidak digunakan, bisa dihapus



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

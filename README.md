# 🐳 KEL3_SBTA - Sistem Berbasis Teknologi Awan

Proyek ini merupakan arsitektur aplikasi berbasis Docker yang terdiri dari tiga bagian utama:
- **Frontend**
- **Backend**
- **Service pendukung** (PHP, MySQL, Nginx) melalui Docker

---

## 📦 Struktur Folder

Kel3_SBTA/
├── backend/
│   └── docker/
│       ├── mysql/
│       ├── nginx/
│       └── php/
├── frontend/
├── my-laravel/
├── docker-compose.yml
├── Dockerfile
└── README.md


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

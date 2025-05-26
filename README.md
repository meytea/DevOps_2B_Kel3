# 📦 KEL3_SISTEM BIMBINGAN TUGAS AKHIR 

Repositori ini merupakan bagian dari tugas mata kuliah Pemrograman Berbasis Framework (PBF) yang mengimplementasikan prinsip DevOps menggunakan Docker dan Docker Compose.
- **Frontend**
- **Backend**
- **Database**
- **Nginx**
- **PHP**

---

## 🔧 Apa Itu DevOps?
DevOps adalah praktik yang menggabungkan Development (Dev) dan Operations (Ops) dengan tujuan untuk meningkatkan efisiensi pengembangan perangkat lunak, deployment otomatis, dan kolaborasi tim.

---

## 🐳 Apa Itu Docker?
Docker adalah platform open-source yang memungkinkan developer untuk mengemas aplikasi dan semua dependensinya ke dalam sebuah unit standar yang disebut container.
Keunggulan Docker:
- Portabilitas tinggi (bisa dijalankan di berbagai environment)
- Konsistensi lingkungan pengembangan dan produksi
- Isolasi layanan (tidak saling terganggu)
- Mudah dalam deployment dan scaling

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

```
---

## 🛠️ Persiapan

1. Install Docker dan Docker Compose
Pastikan Anda sudah menginstall:
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

Untuk memastikan instalasi berhasil:
```bash
docker -v
docker-compose -v
```

2. Clone Repository
Buat sebuah folder bary, lalu clone repository ini ke dalamnya:
```bash
git clone <URL_REPOSITORY> frontend //dari repo github backend
git clone <URL_REPOSITORY> backend //dari repo github frontend
git clone <URL_REPOSITORY> //dari repo devops

```
---

## 🚀 Cara Menjalankan 
Untuk membangun dan menjalankan semua container sekaligus:
```bash
docker-compose up -d --build
```
Lalu cek apakah container sudah berjalan dengan:
```bash
docker ps
```
----

## 🌐 Cara Mengakses Aplikasi
Setelah container berjalan, kamu dapat mengakses layanan sebagai berikut (asumsi konfigurasi default dan Nginx sebagai reverse proxy):
```bash
| No | Layanan        | URL Akses                                      | Port Host → Container | Deskripsi                                                |
| -- | -------------- | ---------------------------------------------- | --------------------- | -------------------------------------------------------- |
| 1  | **Backend**    | [http://localhost:8080](http://localhost:8080) | 8080 → 80             | Nginx melayani backend berbasis PHP                      |
| 2  | **Frontend**   | [http://localhost:8082](http://localhost:8082) | 8082 → 80             | Nginx melayani frontend berbasis PHP                     |
| 3  | **phpMyAdmin** | [http://localhost:8081](http://localhost:8081) | 8081 → 80             | GUI untuk mengelola database MySQL                       |
| 4  | **MySQL**      | `localhost:3307`                               | 3307 → 3306           | Akses MySQL lewat client (DBeaver, MySQL Workbench, dll) |

```

----

## 📌 Catatan
- Untuk menghentikan semua container:
```bash
docker-compose down
```
- Pastikan tidak ada service yang menggunakan port yang sama dengan service di docker-compose.yml.
- Selalu periksa file konfigurasi seperti nginx, php, dan mysql agar sesuai dengan kebutuhan proyek.
- Jika menggunakan .env, pastikan file tersebut tersedia dan terisi dengan benar.

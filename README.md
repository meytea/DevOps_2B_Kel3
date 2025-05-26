# 🐳 KEL3_SBTA 

Proyek ini merupakan arsitektur aplikasi berbasis Docker yang terdiri dari tiga bagian utama:
- **Frontend**
- **Backend**
- **Service pendukung** (PHP, MySQL, Nginx) melalui Docker

---

## 📦 Struktur Folder

![image](https://github.com/user-attachments/assets/3b924a7d-b9ab-475c-8b56-7dba22702a52)


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

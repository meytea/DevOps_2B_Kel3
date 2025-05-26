# 🐳 KEL3_SBTA 

Proyek ini merupakan arsitektur aplikasi berbasis Docker yang terdiri dari tiga bagian utama:
- **Frontend**
- **Backend**
- **Service pendukung** (PHP, MySQL, Nginx) melalui Docker

---

## 📦 Struktur Folder

![image](https://github.com/user-attachments/assets/445f00e0-b09a-45c7-b79c-6709427b7194)


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

# 🚀 N8N-Class: Docker Deployment Made Easy & Fun!

Halo! Selamat datang di **N8N-Class** – repositori Docker Compose yang akan membuat deployment N8N Anda menjadi lebih mudah, aman, dan tentunya menyenangkan! ✨

---

## 📖 Apa Itu N8N?

N8N adalah alat workflow automation yang powerful dan open-source. Dengan N8N, Anda dapat:
- 🔗 Menghubungkan berbagai aplikasi dan layanan
- ⚡ Mengotomatisasi proses bisnis
- 🎨 Membuat workflow visual yang keren
- 🔒 Dan tentunya, dengan keamanan yang terjamin!

## 🎯 Fitur Utama Deployment Ini

### 🔐 Security First!
- **Basic Authentication** - Login dengan username dan password yang aman
- **Enforced Settings Permissions** - File konfigurasi yang terlindungi
- **Trusted Proxy Support** - Aman di balik proxy/reverse proxy
- **Encryption Key** - Data Anda terenkripsi dengan baik

### 🌏 Lokalized & Optimized
- **Timezone Jakarta** - Sudah disetel ke Asia/Jakarta
- **Multiple Database Support** - MySQL dan PostgreSQL
- **Email Configuration** - Siap untuk notifikasi email
- **SSE Push Backend** - Real-time updates yang smooth

### 🐳 Docker Power
- **Latest N8N Image** - Selalu up-to-date
- **Auto-restart** - Service selalu hidup
- **Volume Persistence** - Data tidak hilang saat restart
- **Host Integration** - Akses ke host.docker.internal

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose terinstall
- File `.env` yang sudah dikonfigurasi

### Langkah Deployment

1. **Clone repositori ini**
   ```bash
   git clone https://github.com/luridarmawan/n8n-class
   cd n8n-class
   ```

2. **Siapkan file environment**
   ```bash
   cp .env.example .env
   # Edit file .env sesuai kebutuhan Anda
   ```

3. **Jalankan N8N!**
   ```bash
   docker-compose up -d
   ```

4. **Akses N8N**
   - Buka: `http://localhost:5678`
   - Login dengan credentials dari file `.env`

## ⚙️ Konfigurasi Environment

File `.env` adalah jantung dari deployment ini! Pastikan Anda mengatur:

- **Authentication**: `N8N_BASIC_AUTH_USER` & `N8N_BASIC_AUTH_PASSWORD`
- **Database**: Pilih antara MySQL atau PostgreSQL
- **Encryption**: `N8N_ENCRYPTION_KEY` (wajib!)
- **Email**: Untuk notifikasi dan reset password
- **Network**: `N8N_HOST` dan `WEBHOOK_URL`

## 🗂️ Struktur Project

```
n8n-class/
├── docker-compose.yml    # 🐳 Main deployment file
├── .env                  # ⚙️ Configuration (create from .env.example)
├── .n8n/                 # 💾 Persistent data volume
└── README.md             # 📚 This awesome documentation!
```

## 🔧 Customization

### Database Pilihan
Uncomment bagian database yang ingin digunakan di `docker-compose.yml`:
```yaml
# Untuk MySQL:
- DB_MYSQLDB_HOST=${DB_MYSQLDB_HOST}

# Untuk PostgreSQL:  
- DB_POSTGRESDB_HOST=${DB_POSTGRESDB_HOST}
```

### Timezone
Default: `Asia/Jakarta` - bisa diubah sesuai kebutuhan!

## 🛠️ Troubleshooting

### Service tidak jalan?
```bash
docker-compose logs n8n
```

### Lupa password?
Edit file `.env` dan restart service:
```bash
docker-compose restart n8n
```

### Port sudah digunakan?
Edit port di `docker-compose.yml`:
```yaml
ports:
  - "127.0.0.1:5678:5678"  # Ganti 5678 dengan port lain
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests

## 📞 Support & Connect

- **Developer**: Luri Darmawan
- **Website**: [https://carik.id](https://carik.id)
- **Repository**: [https://github.com/luridarmawan/n8n-class](https://github.com/luridarmawan/n8n-class)

## ⭐ Star History

If you find this project helpful, please give it a star! ⭐

---

**Dibuat dengan ☕ dan ❤️ di Indonesia**

*Happy automating! 🎉*

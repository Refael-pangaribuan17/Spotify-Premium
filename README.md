# 🎨✨ Spicetify Installer & Customizer ![badge](https://img.shields.io/badge/Spotify-Customizer-1DB954?style=flat&logo=spotify) ![status](https://img.shields.io/badge/Status-Stable-green?style=flat&logo=github)

> 🎧 Kustomisasi Spotify Desktop kamu dengan tema, ekstensi, dan fitur keren lainnya.  
> 💡 Aman, legal, dan tidak memodifikasi akun menjadi Premium secara ilegal!

---

## 🖥️ Instalasi

### 🪟 Windows

🛠️ **Langkah 1: Install Spicetify CLI**

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
```

🛒 **Langkah 2 (Opsional): Install Spicetify Marketplace**

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/marketplace/main/resources/install.ps1 | iex
```

---

### 🐧 Linux / 🍎 macOS

🛠️ **Langkah 1: Install Spicetify CLI**

```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/cli/main/install.sh | sh
```

🛒 **Langkah 2 (Opsional): Install Spicetify Marketplace**

```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/marketplace/main/resources/install.sh | sh
```

---

## 🚀 Penggunaan Dasar

📦 Setelah terinstal, buka Spotify dan akan muncul tab **Marketplace**.  
Dari sana, kamu bisa:

- 🌈 Ganti Tema Spotify
- ⚙️ Tambah Ekstensi Tambahan
- 💻 Tambah Snippet JavaScript
- 🎮 Ubah UI Spotify sesuka hati

📌 Jalankan perintah:

```bash
spicetify backup apply
```

---

## 🔄 Update Setelah Spotify Update

Spotify sering update, jadi:

🧩 Jalankan ini setelah Spotify diperbarui:

```bash
spicetify update
```

🕹️ Untuk versi Spicetify lama (< 2.27.0):

```bash
spicetify upgrade
```

🔁 Jika tidak berhasil:

```bash
spicetify backup apply
```

---

## 📌 Catatan Penting

- 🚫 Tidak bisa digunakan di Spotify Web atau Mobile.
- 💾 Lakukan backup sebelum apply!
- 🔒 Tidak memberikan fitur Premium secara ilegal — hanya tampilan & UX.

---

## 📄 Lisensi

📝 MIT License  
📎 Proyek ini tidak berafiliasi dengan Spotify AB.

---

## ❤️ Credits

Made with 🎧 by the [Spicetify Community](https://github.com/spicetify)  
Give us a ⭐ if you like it!

# 🎨✨ Spicetify Installer & Customizer ![badge](https://img.shields.io/badge/Spotify-Customizer-1DB954?style=flat&logo=spotify)

> 🎧 Kustomisasi Spotify Desktop dengan tema, ekstensi, dan fitur tambahan.  
> ✅ Legal, aman, dan **tidak** menjadikan akun Spotify menjadi Premium secara ilegal.

---

## 📋 Table of Contents

- [Installation Guide](#-installation-guide)
  - [Windows](#-windows)
  - [Linux & macOS](#-linux--macos)
  - [AUR (Arch Linux)](#-aur-arch-linux)
  - [Snap Installation](#-snap-installation-not-supported)
  - [Flatpak Installation](#-flatpak-installation)
  - [Legacy Installation](#-legacy-installation)
- [Basic Usage](#-basic-usage)
- [Update Guide](#-update-setelah-spotify-update)
- [Uninstallation](#-uninstallation)
- [License](#-license)

---

## 🖥️ Installation Guide

### 🪟 Windows

#### 💡 Recommended (PowerShell)
```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
```

#### 🍫 Chocolatey
Install via Chocolatey:

```powershell
choco install spicetify-cli
```

#### 📦 Scoop
```powershell
scoop install spicetify-cli
```

Jika Spotify di-install via Scoop:

```powershell
scoop prefix spotify
```

Contoh output:
```makefile
C:\Users\<username>\scoop\apps\spotify\current
```

Gunakan path tersebut sebagai `spotify_path` di config Spicetify.

#### 🐦 Winget
```powershell
winget install Spicetify.Spicetify
```

---

### 🐧 Linux & 🍎 macOS

#### 💡 Recommended (Shell Script)
```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/cli/main/install.sh | sh
```

#### 🍺 Homebrew / LinuxBrew
```bash
brew install spicetify-cli
```

📍 **Untuk macOS**, set `spotify_path` di:
```arduino
~/.config/spicetify/config-xpui.ini
```

Menjadi:
```swift
/Applications/Spotify.app/Contents/Resources
```

---

### 🧱 AUR (Arch Linux)

```bash
yay -S spicetify-cli
```

Ubah izin sebelum apply:

```bash
sudo chmod a+wr /opt/spotify
sudo chmod a+wr /opt/spotify/Apps -R
```

Jika menggunakan `spotify-launcher`, Spotify berada di:
```swift
$HOME/.local/share/spotify-launcher/install/usr/share/spotify/
```

Gunakan path ini di `spotify_path`.

📌 **Penting:** `spotify_path` harus absolut, jangan gunakan `~`.

---

### 🧩 Snap Installation (Not Supported)

Snap tidak bisa dimodifikasi, lakukan:

1. **Uninstall Snap Spotify:**
   ```bash
   sudo snap remove spotify
   ```

2. **Install via APT:**
   ```bash
   curl -sS https://download.spotify.com/debian/pubkey_C85668DF69375001.gpg | sudo gpg --dearmor --yes -o /etc/apt/trusted.gpg.d/spotify.gpg
   echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
   sudo apt-get update && sudo apt-get install spotify-client
   ```

3. **Beri izin:**
   ```bash
   sudo chmod a+wr /usr/share/spotify
   sudo chmod a+wr /usr/share/spotify/Apps -R
   ```

---

### 📦 Flatpak Installation

1. **Cari path Spotify:**
   ```bash
   flatpak --installations
   ```

   Biasanya di:
   ```swift
   /var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify/
   ```

   Atau:
   ```swift
   ~/.local/share/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify/
   ```

   Set `spotify_path` ke direktori tersebut.

2. **Temukan file prefs:**
   - `~/.config/spotify/prefs`
   - `~/.var/app/com.spotify.Client/config/spotify/prefs`

3. **Set prefs_path:**
   ```bash
   spicetify config prefs_path ~/.var/app/com.spotify.Client/config/spotify/prefs
   ```

4. **Beri izin akses:**
   ```bash
   sudo chmod a+wr /var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify
   sudo chmod a+wr -R /var/lib/flatpak/app/com.spotify.Client/x86_64/stable/active/files/extra/share/spotify/Apps
   ```

---

### 🧓 Legacy Installation

Untuk Spotify lama (v1.1.56 ke bawah), install Spicetify versi lama.

#### Windows (PowerShell):
```powershell
$v="1.2.1"; Invoke-WebRequest -UseBasicParsing "https://raw.githubusercontent.com/spicetify/cli/main/install.ps1" | Invoke-Expression
```

#### Linux/macOS:
```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/cli/main/install.sh -o /tmp/install.sh
sh /tmp/install.sh 1.2.1
```

---

## 🚀 Basic Usage

Setelah instalasi:

```bash
spicetify backup apply
```

Atau gunakan tab **Marketplace** untuk install tema, ekstensi, dan snippet.

---

## 🔁 Update Setelah Spotify Update

```bash
spicetify update
```

Untuk versi lama (<2.27.0):
```bash
spicetify upgrade
```

Jika gagal:
```bash
spicetify backup apply
```

---

## ❌ Uninstallation

### Windows (PowerShell)
```powershell
spicetify restore
rmdir -r -fo $env:APPDATA\spicetify
rmdir -r -fo $env:LOCALAPPDATA\spicetify
```

### Linux/macOS

Jika install pakai package manager, gunakan metode uninstall default.

```bash
spicetify restore
rm -rf ~/.spicetify
rm -rf ~/.config/spicetify
```

---

## 🎨 Features

- ✨ **Custom Themes**: Berbagai tema untuk mengubah tampilan Spotify
- 🧩 **Extensions**: Fitur tambahan seperti lyrics, visualizer, dan lainnya
- 🔧 **Custom Apps**: Aplikasi mini dalam Spotify
- 📱 **Responsive Design**: Tema yang responsif untuk berbagai ukuran layar
- 🌙 **Dark/Light Mode**: Support untuk mode gelap dan terang
- 🎵 **Enhanced UI**: Peningkatan antarmuka pengguna

---

## 📚 Documentation

- [Official Documentation](https://spicetify.app)
- [Themes Repository](https://github.com/spicetify/spicetify-themes)
- [Extensions Repository](https://github.com/spicetify/spicetify-extensions)
- [Community Discord](https://discord.gg/VnevqPp2Rr)

---

## ⚠️ Disclaimer

- Spicetify adalah tool legal untuk kustomisasi tampilan Spotify
- Tidak mengubah fungsionalitas Premium atau bypass pembayaran
- Gunakan dengan risiko sendiri
- Backup data sebelum menggunakan

---

## 🤝 Contributing

Kontribusi selalu diterima! Silakan:

1. Fork repository
2. Buat branch untuk fitur baru
3. Commit perubahan
4. Push ke branch
5. Buat Pull Request

---

## 📄 License

📝 [MIT License](LICENSE)

---

## 🙏 Credits

- [Spicetify Team](https://github.com/spicetify) - Developer utama
- [Community Contributors](https://github.com/spicetify/cli/graphs/contributors) - Kontributor komunitas
- [Theme Creators](https://github.com/spicetify/spicetify-themes/graphs/contributors) - Pembuat tema

---

**Made with ❤️ by the Spicetify Community**

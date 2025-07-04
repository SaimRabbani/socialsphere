# SocialSphere - The Ultimate Social Media Downloader

A powerful and modern Flask-based web application that allows you to download videos, reels, posts, and media from top social media platforms like YouTube, Instagram, TikTok, Facebook, Twitter/X, Reddit, and more — all in one place.

---

## 👤 Made with ❤️ by **Saim Rabbani**

---

## 🚀 Features

### ✅ Multi-Platform Support
- **YouTube**: Videos, Shorts, Playlists, Subtitles
- **Instagram**: Reels, Posts, Stories, IGTV, Profile Posts
- **TikTok**: HD Videos with metadata
- **Facebook**: Videos and Posts
- **Twitter/X**: Videos, Threads, and Media
- **Reddit**: Videos, Images, GIFs
- **Generic URLs**: via `yt-dlp` support

### 🌟 Advanced Features
- **Auto Platform Detection**
- **Bulk Downloading**
- **High-Quality 1080p Media**
- **Subtitles Download (if available)**
- **Metadata Retention**
- **Organized Folder System**
- **ZIP Folder Download**
- **Modern Web UI (Responsive)**

---

## 🛠 Installation

### 🧾 Prerequisites:
- Python 3.7 or higher
- pip (Python package manager)

### 🔧 Install Requirements

Using `requirements.txt`:
```bash
pip install -r requirements.txt
```

Or install manually:
```bash
pip install flask requests yt-dlp instaloader werkzeug
```

---

## 🚦 Running the App

```bash
python app.py
```

Then open your browser at:
```
http://localhost:5000
```

---

## 🌐 Web Interface Usage

1. Paste the URL of a supported platform
2. Click **Download**
3. View files in the **Downloads** tab
4. Optionally clear all or download as ZIP

---

## 📡 API Endpoints

### 🎯 Single Download
```http
POST /download
Content-Type: application/json

{
  "url": "https://www.youtube.com/watch?v=VIDEO_ID"
}
```

### 📦 Bulk Download
```http
POST /bulk-download
Content-Type: application/json

{
  "urls": [
    "https://youtu.be/example",
    "https://instagram.com/reel/example"
  ]
}
```

### 📁 Get Downloads
```http
GET /downloads
```

### 📥 Download Specific File
```http
GET /download-file/<filename>
```

### 🗂 Download Folder as ZIP
```http
GET /download-folder/<foldername>
```

### 🧹 Clear All Downloads
```http
POST /clear-downloads
```

---

## 🔐 Configuration

### Secret Key (Security)
Update the `app.py`:
```python
app.config['SECRET_KEY'] = 'your-strong-secret-key'
```

### Download Folder Path
```python
DOWNLOAD_DIR = os.path.join(os.getcwd(), 'downloads')
```

---

## 📂 Folder Structure

```
SocialSphere/
├── app.py
├── requirements.txt
├── templates/
│   └── index.html
├── downloads/
├── README.md
└── LICENSE
```

---

## ⚠️ Limitations

- Does not support private/restricted content
- Instagram stories require login
- Rate limits apply on some platforms
- Geo-blocked content may fail

---

## ❓ Troubleshooting

| Issue | Solution |
|-------|----------|
| `ModuleNotFoundError` | Run: `pip install -r requirements.txt` |
| `PermissionError` | Ensure app has access to `/downloads` folder |
| `Download failed` | Make sure URL is public and valid |
| `App not starting` | Ensure Python ≥ 3.7 and no port conflict |

---

## 📜 License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for full details.

---

## 📣 Disclaimer

> This tool is intended for **educational and personal use only**.  
Downloading or using content without permission may violate the terms of service of respective platforms.  
**Use responsibly.**

---

## ✨ Future Ideas

- Add login system
- Enable cloud download & storage
- Add Telegram bot or mobile version
- Analytics dashboard for downloads

---

> Built with 🚀 by **Saim Rabbani**

# NoTraceFiles 🛡️

[![Release](https://img.shields.io/badge/release-v2.0.1-0891b2.svg)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Android-00253f.svg)](#downloads)
[![Zero Telemetry](https://img.shields.io/badge/telemetry-0%20packets-emerald.svg)](#privacy-guarantee)
[![Quality](https://img.shields.io/badge/pixel%20drift-0.00%25%20lossless-cyan.svg)](#architecture)

> **"Share the photo, keep the details to yourself."**  
> Fast, personal, and completely offline privacy utility. Removes hidden satellite GPS tags, camera hardware serials, and timestamps directly on your device before you share.

---

## 🌟 Highlights

- **100% Offline Local Processing**: Operates strictly within local device RAM. No telemetry servers, no analytical trackers, and zero cloud uploads.
- **Lossless Quality (0.00% Pixel Drift)**: Surgical byte removal keeps your original pixels 100% untouched. No quality degradation, no JPEG artifacting, and zero visual blur.
- **Cross-Platform**:
  - **Windows Desktop**: Batch drag-and-drop processing for up to 80 photos per second with Windows Explorer right-click shell integration.
  - **Android Mobile**: Lightweight (<1 MB) Share Sheet hook for one-tap sanitization before posting to WhatsApp, Signal, Instagram, or X.
- **Free & Open Utility**: Created by **Yeasin Arafat Sadiq**. No subscription walls, no ads, and no data brokers.

---

## 📦 Downloads & Releases (v2.0.1)

| Platform | Format | Size | Description |
| :--- | :--- | :--- | :--- |
| **Windows** | [Setup.exe](https://github.com/) | 51.7 MB | Full installer with Explorer shell integration |
| **Windows** | [Portable.exe](https://github.com/) | 40.8 MB | Standalone portable executable (runs from USB) |
| **Android** | [Release.apk](https://github.com/) | 921 KB | Sideloadable APK for Android 8.0+ |
| **Android** | [Release.aab](https://github.com/) | 921 KB | Android App Bundle for Google Play |

### Integrity Verification (SHA-256 Checksums)

```text
e53563d2701a23a34b54a52c2552608ef4050bc68db1ef9dcc8a349992509acb  NoTrace_Files_Setup.exe
328ad8d6ba62f2faddd1bb38f3c2f23cca83a59ecdfdd3d263e8cc89bca2ded6  NoTrace_Files.exe
2af5c763c5ae9794f289230a31d7ed19a64ebd54f59f4d1b5391b0db4066c99c  NoTrace-Files-2.0.1.apk
f41a27b13fd6cb97b6e232160a915f450c577102563b315ddb7606760479a5c4  NoTrace-Files-2.0.1.aab
```

---

## 🔍 The Threat: What an Unstripped File Reveals

Every digital photo taken by smartphones and modern cameras embeds extensive hidden metadata headers:

1. **GPS Coordinates (EXIF 0x0002)**: Satellite latitude, longitude, and altitude pinpointing your residence, workplace, or private locations.
2. **Camera Hardware Fingerprints (EXIF 0xA431)**: Camera body serial numbers and lens IDs that allow data scrapers to link anonymous posts across disparate platforms.
3. **Behavioral Timeline (EXIF 0x9003)**: Millisecond-accurate capture timestamps and timezone offsets mapping your daily schedule.
4. **Ghost Thumbnails (IFD1 / XMP)**: Hidden preview caches that frequently retain the uncropped original even after editing.

NoTraceFiles parses and purges these headers at the binary stream level before saving.

---

## 🚀 Building from Source

### Windows App (Python + CustomTkinter + PyInstaller)
```bash
# Clone the repository
git clone https://github.com/your-username/notracefiles.git
cd notracefiles

# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install requirements
pip install -r requirements.txt

# Run GUI
python gui/app.py

# Build binaries
pyinstaller NoTrace_Files.spec
pyinstaller NoTrace_Files_Setup.spec
```

### Android App (Android Studio / Gradle)
```bash
cd android
./gradlew assembleRelease
./gradlew bundleRelease
```

### Landing Page Website (React + TypeScript + Vite + Tailwind CSS)
```bash
cd website
npm install
npm run build
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

Developed with ❤️ by **[Yeasin Arafat Sadiq](https://www.sadiqtbh.info)**.

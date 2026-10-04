# Step-by-Step GitHub Publishing Guide

Follow these steps to publish NoTraceFiles on your GitHub account:

### 1. Initialize Git Repository
In your terminal, navigate to the `github/` folder:
```bash
cd "C:\Users\Sadiq\Documents\Codex\2026-10-01\a\outputs\NoTraceFiles-Publish-Package\github"
git init
git add .
git commit -m "feat: initial commit for NoTraceFiles v2.0.1"
```

### 2. Create Repository on GitHub
1. Go to https://github.com/new
2. Name the repository: `notracefiles` (or `notrace-files`)
3. Choose **Public**
4. Do NOT initialize with README (you already have one)
5. Click **Create repository**

### 3. Push Local Code to GitHub
```bash
git remote add origin https://github.com/YOUR_USERNAME/notracefiles.git
git branch -M main
git push -u origin main
```

### 4. Create GitHub Release
1. In your GitHub repository, click **Releases** -> **Draft a new release**.
2. Tag version: `v2.0.1`
3. Release title: `NoTraceFiles v2.0.1 — Official Release`
4. Copy description from `RELEASE_NOTES_v2.0.1.md`.
5. Attach the binary assets from `windows app exe/` and `andriod/`:
   - `NoTrace_Files_Setup.exe`
   - `NoTrace_Files.exe`
   - `NoTrace-Files-2.0.1.apk`
   - `NoTrace-Files-2.0.1.aab`
6. Click **Publish release**!

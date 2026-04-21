---

# 🤖 Messenger Bot Deployment Guide

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-%3E%3D20-339933?style=for-the-badge&logo=node.js">
  <img src="https://img.shields.io/badge/Platform-VPS%20%7C%20Termux%20%7C%20Hosting-1f6feb?style=for-the-badge">
  <img src="https://img.shields.io/badge/License-Free-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Stable-success?style=for-the-badge">
</p>

<p align="center">
  🚀 Hướng dẫn đầy đủ để deploy bot Messenger 🚀
</p>

---

## 📑 Table of Contents

* [📌 Overview](#-overview)
* [🚀 VPS Deployment](#-vps-deployment-ubuntu)
* [📱 Termux Deployment](#-termux-deployment-android)
* [☁️ Free Hosting 24/7](#️-free-hosting-247)
* [📦 Source Code](#-source-code)
* [⚡ Optimization](#-optimization)
* [🧩 Troubleshooting](#-troubleshooting)

---

## 📌 Overview

| Platform   | Mục đích       | Độ ổn định |
| ---------- | -------------- | ---------- |
| 🖥 VPS     | Chạy chính     | ⭐⭐⭐⭐⭐      |
| ☁️ Hosting | Treo 24/7 free | ⭐⭐⭐⭐       |
| 📱 Termux  | Test nhanh     | ⭐⭐         |

---

# 🚀 VPS Deployment (Ubuntu)

🎥 Video guide:
👉 [https://www.youtube.com/watch?v=k55JNgzihXg](https://www.youtube.com/watch?v=k55JNgzihXg)

### ⚙️ One-line Setup

```bash id="p6ydg5"
sudo apt update && sudo apt upgrade -y
&& sudo apt-get install -y curl git
&& curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
&& sudo apt-get install -y nodejs
```

---

### 📦 Clone & Run

```bash id="d6gxyn"
git clone https://github.com/LunarKrystal/Mirai
cd Mirai
npm install
npm start
```

---

## 📱 Termux Deployment (Android)

🎥 Video:
👉 [https://www.youtube.com/watch?v=v5hi6KSfqn0](https://www.youtube.com/watch?v=v5hi6KSfqn0)

### ⚙️ Bootstrap

```bash id="9j2vnb"
apt update && apt upgrade -y
&& apt install proot-distro -y
&& proot-distro install ubuntu
&& proot-distro login ubuntu
```

---

### 🧱 Setup Ubuntu Environment

```bash id="r5yrbf"
apt update && apt upgrade -y
&& apt-get install -y git curl sudo
&& curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
&& sudo apt-get install -y nodejs
```

---

### ▶️ Run Bot

```bash id="n9yqg4"
proot-distro login ubuntu
cd Mirai
npm start
```

---

# ☁️ Free Hosting 24/7

🎥 Video:
👉 [https://www.youtube.com/watch?v=bPvM3Ud30jo](https://www.youtube.com/watch?v=bPvM3Ud30jo)

🌐 Dashboard:
👉 [https://katabump.com](https://katabump.com)

---

## ⚙️ Server Configuration

| Key              | Value                                                                                          |
| ---------------- | ---------------------------------------------------------------------------------------------- |
| **Docker Image** | NodeJS 20+                                                                                     |
| **Repository**   | [https://github.com/LunarKrystal/Lunar-Krystal](https://github.com/LunarKrystal/Lunar-Krystal) |
| **Branch**       | `hosting`                                                                                      |

---

# 📦 Source Code

```bash id="hlpgre"
git clone https://github.com/LunarKrystal/Mirai
```

---

# ⚡ Optimization

### 🔥 Run with PM2 (recommended for VPS)

```bash id="x9w6rm"
npm install -g pm2
pm2 start index.js --name messenger-bot
pm2 save
pm2 startup
```

---

### 🧠 Why PM2?

* Auto restart khi crash
* Chạy background
* Log dễ debug

---

# 🧩 Troubleshooting

### ❌ Node version lỗi

```bash id="3hbyd7"
node -v
```

👉 Phải >= 20

---

### ❌ Missing modules

```bash id="w0xvhl"
npm install
```

---

### ❌ Permission error (Termux)

```bash id="zghj96"
termux-setup-storage
```

---

# 💎 Pro Tips

```diff id="wq5o4y"
+ Dùng VPS nếu muốn bot ổn định lâu dài
+ Dùng PM2 để tránh crash
+ Backup config & session thường xuyên
- Không chạy bot bằng Termux lâu (dễ bị kill nền)
```

---

# ❤️ Credits

* 👑 Author: **LunarKrystal**

---

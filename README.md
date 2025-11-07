‎# 🤖 AI-on-Ubuntu
‎
‎Welcome to **AI-on-Ubuntu** — a ready-to-use setup for running **Open WebUI** on **Ubuntu** with **Python 3.12+** support.  
‎This repository documents the complete installation and activation process for Open WebUI, including building Python 3.12 from source for environments where it’s not pre-installed.
‎
‎---
‎
‎## 🧠 Overview
‎
‎This setup allows you to:
‎- Run **Open WebUI** locally on Ubuntu.
‎- Use **Ollama** and **Python 3.12+** for advanced AI workflows.
‎- Quickly launch the AI interface via a browser at `http://localhost:8080`.
‎
‎
‎---
‎
‎## ⚙️ Prerequisites
‎
‎Make sure you’re running Ubuntu (or a compatible Linux environment) with **sudo privileges** and **Internet access**.
‎
‎---
‎
‎## 🚀 Installation Steps
‎
‎### 1️⃣ Install Required Dependencies
‎
‎```bash```
‎apt update && apt install sudo -y &&
‎sudo apt install -y build-essential git wget tar zlib1g-dev libssl-dev
‎libffi-dev libsqlite3-dev libreadline-dev libbz2-dev libncurses5-dev &&
‎cd /usr/src &&
‎wget https://www.python.org/ftp/python/3.12.7/Python-3.12.7.tgz &&
‎tar -xf Python-3.12.7.tgz &&
‎cd Python-3.12.7 &&
‎./configure --enable-optimizations &&
‎make -j$(nproc) &&
‎make altinstall &&
‎ln -sf /usr/local/bin/python3.12 /usr/bin/python3.12 &&
‎python3.12 --version

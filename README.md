‎# 🤖 AI-on-TERMUX
‎
‎Welcome to **AI-on-Ubuntu** — a ready-to-use setup for running **Open WebUI** on **Ubuntu** with **Python 3.12+** support. 

‎This repository documents the complete installation and activation process for Open WebUI, including building Python 3.12 from source for environments where it’s not pre-installed.
‎
‎---
‎

‎## 🧠 Overview


‎- This is on proot-distro (ubuntu)
‎This setup allows you to:
‎- Run **Open WebUI** locally on Ubuntu  
‎- Use **Ollama** and **Python 3.12+** for advanced AI workflows  
‎- Quickly launch the AI interface in your browser at  
‎  👉 `http://localhost:8080`
‎

‎> ⏱️ The full setup may take around **25-30 minutes**, mainly due to Python 3.12 compilation.
‎

‎---
‎
‎## ⚙️ Prerequisites
‎
‎Make sure you’re running **Ubuntu** (or a compatible Linux environment) with:
‎
‎- 🧑‍💻 `sudo` privileges  
‎- 🌐 Active internet connection  
‎- 💾 At least 2 GB free space for Python build  
‎
‎---
‎
‎## 🚀 Installation Steps
‎
‎### 1️⃣ Install Required Dependencies
‎### ollama
‎`curl -fsSL https://ollama.com/install.sh | sh`
‎#Run ollama
‎`ollama serve`
‎### Python3.12.7
‎```
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
‎```


‎### OPEN-WEBUI 


‎``` pip install venv && python3.12 -m venv openwebui && source openwebui/bin/activate && open-webui serve --host 0.0.0.0 --port 8080 ```


‎#HOW TO LOGIN PROOT-DISTRO


‎``` proot-distro login ubuntu --bind /dev/null:/proc/sys/net/ipv6/conf/default/disable_ipv6 --bind /dev
‎```

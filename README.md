# Ai-on-ubuntu
In This repo there is Openwebui installed which took my 2-3 hours as python 3.12iss not installed'apt install sudo -y '
'
sudo apt update && \
sudo apt install -y build-essential git wget tar zlib1g-dev libssl-dev \
libffi-dev libsqlite3-dev libreadline-dev libbz2-dev libncurses5-dev && \
cd /usr/src && \
wget https://www.python.org/ftp/python/3.12.7/Python-3.12.7.tgz && \
tar -xf Python-3.12.7.tgz && \
cd Python-3.12.7 && \
./configure --enable-optimizations && \
make -j$(nproc) && \
make altinstall && \
ln -sf /usr/local/bin/python3.12 /usr/bin/python3.12 && \
python3.12 --version
'
'TO ACTIVE UBUNTU'
ollama serve
source openwebui/bin/active
source openwebui/bin/activate
open-webui serve --host 0.0.0.0 --port 8080
#Go to 
http://localhost:8080
#DOWNLOAD FILE
https://drive.google.com/file/d/1hz0XWJ_eeoc9DO2FaEPDtWP4kNG8Y8h-/view?usp=drivesdk

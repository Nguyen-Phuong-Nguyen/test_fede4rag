# 🚀 Hướng dẫn cài đặt và chạy FedE4RAG trên DigitalOcean

---

```bash
# Tải và cài đặt Miniconda
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh

# Kích hoạt Conda
source ~/.bashrc

# Kiểm tra phiên bản Conda
conda --version

conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r

conda create -n fedrag python=3.11 -y
conda init bash
source ~/.bashrc
conda activate fedrag

git clone https://github.com/Nguyen-Phuong-Nguyen/test_fede4rag
cd FedE4RAG/FedE
pip install -r requirements.txt
pip install transformers==4.35.0
pip install "numpy<2"

# chạy upstream
bash /root/FedE4RAG/FedE/run.sh

# nếu repo private cần credential thì có thể sử dụng token này
git token de dang nhap -> bypass github credential de clone ve xai: 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

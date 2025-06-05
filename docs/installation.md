# RWKV模型部署指南

## ‌一、环境准备

### 更新系统

#### EulerOS2.0
```bash
yum -y update  
yum -y upgrade
```

## ‌二、下载

### EulerOS2.0

####1.创建虚拟环境
```bash
# 创建Python 3.10环境
conda create -n rwkv python=3.10 -y
conda activate rwkv
```
####2.安装 PyTorch

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```
####3.克隆 ChatRWKV 仓库
```bash
git clone https://github.com/BlinkDL/ChatRWKV.git
cd ChatRWKV
```

####4. 安装其他依赖
```bash
pip install -r requirements.txt
```
####5. 下载模型文件
将 RWKV-4-Pile-1B5-EngChn-test4-20230115.pth 模型文件下载到 ./models 目录：
```bash
mkdir -p models && cd models
# 从Hugging Face或其他来源下载模型
wget https://modelscope.cn/models/Blink_DL/rwkv-4-pile-1b5/resolve/master/RWKV-4-Pile-1B5-EngChn-test4-20230115.pth -O RWKV-4-Pile-1B5-EngChn-test4-20230115.pth
cd ..
```

##三、配置与运行
####1. 配置文件（可选）
创建或编辑 ./v2/config.json，设置模型路径和推理参数：
```json
{
  "model_path": "models/RWKV-4-Pile-1B5-EngChn-test4-20230115.pth",
  "strategy": "cpu fp32",
  "tokenizer_path": "20B_tokenizer.json",
  "ctx_len": 1024,
  "gpu_on_mem": true
}
```
####2. 启动推理服务
```bash
python v2/app.py
```
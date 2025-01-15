# 🎥 Frigate Docker Setup

This repository contains a Docker Compose configuration for running Frigate NVR

## ⚡ Prerequisites

- 🐳 Docker and Docker Compose installed
- 🔌 USB Coral TPU (optional but recommended)
- 💾 Sufficient storage space for video recordings

## 🚀 Quick Start

1. Clone this repository:
```bash
git clone https://github.com/racksync/frigate-docker
cd frigate-docker
```

2. Create a config.yml file in the config directory:
```bash
mkdir -p config
touch config/config.yml
```

3. Configure environment variables:
```bash
# Core settings
FRIGATE_RTSP_PASSWORD=your_password
SET_TZ=Asia/Bangkok

# MQTT Settings (optional)
MQTT_HOST=mosquitto
MQTT_USER=your_mqtt_user
MQTT_PASSWORD=your_mqtt_password

# Debug Options
DEBUG_LOGS=false
```

4. Start the container:
```bash
docker-compose up -d
```

## 📁 Directory Structure

```
.
├── config/
│   └── config.yml
├── storage/
├── docker-compose.yml
└── .gitignore
```

## ⚙️ Configuration

The docker-compose.yml includes:
- 🧠 Shared memory allocation: 2048MB
- 🎯 USB Coral TPU support
- 🌐 External network configuration
- 📡 RTSP and WebRTC ports exposed
- 💿 Persistent storage for recordings
- 🏥 Container health monitoring
- 📊 Resource limits (4GB max, 1GB reserved)

## 🔌 Ports

- 🌍 5000: Web interface
- 📹 8554: RTSP feeds
- 🌊 8555: WebRTC (TCP/UDP)

## 🔗 Network

Uses external 'backend' network for container communication.

## 📦 Storage

- 📼 Media storage: ./storage
- ⚙️ Configuration: ./config
- 💫 Temporary cache: 2GB RAM disk

### 📚 Automation Training

- 🛒 [สินค้าและบริการ](http://racksync.com)
- 📖 [เทรนนิ่งคอร์ส](https://facebook.com/racksync)

### 👥 Community

- 🏘️ [Home Automation Thailand](https://www.facebook.com/groups/hathailand)
- 🛍️ [Home Automation Marketplace](https://www.facebook.com/groups/hatmarketplace)
- 💬 [Home Automation Thailand Discord](https://discord.gg/Wc5CwnWkp4) 

## 🏢 [RACKSYNC CO., LTD.](https://racksync.com)

บจก.แรคซิงค์ คือผู้เชี่ยวชาญด้าน Automation และ Smart Solutions ทุกขนาด เรามีบริการให้คำปรึกษาตลอดจนวางระบบ ติดตั้งและมอนิเตอร์โดยผู้เชี่ยวชาญ นอกจากนี้เรายังเป็นบริษัทรับพัฒนา Software As A Service แบบครบวงจรอีกด้วย
\
\
📍 RACKSYNC COMPANY LIMITED \
🌏 Suratthani, Thailand 84000 \
📧 Email : devops@racksync.com \
📞 Tel : +66 85 880 8885 

[![Home Automation Thailand Discord](https://img.shields.io/discord/986181205504438345?style=for-the-badge)](https://discord.gg/Wc5CwnWkp4) [![Github](https://img.shields.io/github/followers/racksync?style=for-the-badge)](https://github.com/racksync) 
[![WebsiteStatus](https://img.shields.io/website?down_color=grey&down_message=Offline&style=for-the-badge&up_color=green&up_message=Online&url=https%3A%2F%2Fracksync.com)](https://racksync.com)




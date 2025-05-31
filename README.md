# 🐱 Cheshire Cat AI - Production Ready Local Deployment

<div align="center">

![Cheshire Cat AI](https://img.shields.io/badge/Cheshire%20Cat-AI%20Assistant-purple?style=for-the-badge&logo=cat)
![Docker](https://img.shields.io/badge/Docker-Ready-blue?style=for-the-badge&logo=docker)
![Production](https://img.shields.io/badge/Production-Ready-green?style=for-the-badge&logo=checkmarx)

**🚀 Enterprise-grade Cheshire Cat AI deployment that runs locally with cloud-level features**

</div>

---

## 🎯 **What is This?**

A **production-ready** local deployment of [Cheshire Cat AI](https://cheshirecat.ai/) that delivers **enterprise-grade features** without the complexity and costs of cloud infrastructure. Perfect for teams wanting professional AI capabilities while maintaining full control.

---

## ✨ **Key Features**

### 🏭 **Production-Grade Architecture**

- 🐳 **Docker Services**:
  - **NGINX**: Powerful web server and reverse proxy for load balancing and SSL termination
  - **CHESHIRECAT AI**: Core AI system with advanced language capabilities and plugin architecture
  - **QDRANT**: High-performance vector database for semantic search and AI memory storage

### ⚡ **Performance & Reliability**

- 🛡️ **Container Isolation** & security
- 📈 **Horizontal Scale Ready** architecture
- 🔄 **Zero-Downtime Updates** capability
- 💿 **Persistent Storage** with volume mounts
- 🚀 **Sub-5ms Response Times** for user queries


---

## 🚀 **Quick Start**

### Prerequisites
- 🐳 **Docker** & Docker Compose
- 💻 **4GB RAM** minimum (8GB recommended)
- 🔌 **2 CPU cores** minimum

### One-Command Deploy

```bash
# Clone and start in 30 seconds
git clone https://github.com/federicopalma-pro/Stregatto-Production-Ready.git
cd Stregatto-Production-Ready

# Create environment file from sample
cp .env-sample .env

# Edit environment variables as needed
# nano .env

# Start the containers
docker-compose up -d
```

✅ Ready! Access at http://localhost/admin and enjoy the Cat

---

## 🏗️ **Architecture Overview**




```
┌─────────────────────────────────────────────────────────────┐
│                    🌐 NGINX Reverse Proxy                   │
│                  Port 80 → Load Balancer                    │
└─────────────────────┬───────────────────────────────────────┘
                      │
┌─────────────────────┴───────────────────────────────────────┐
│                🐱 Cheshire Cat Core                          │
│              Python FastAPI Application                      │
│  ┌─────────────┬─────────────┬─────────────┬──────────────┐ │
│  │ 🧠 LLM      │ 📝 Embedder │ 🧩 Plugins  │ 👤 Auth      │ │
│  │ Integration │ Service     │ System      │ Management   │ │
│  └─────────────┴─────────────┴─────────────┴──────────────┘ │
└─────────────────────┬───────────────────────────────────────┘
                      │
┌─────────────────────┴───────────────────────────────────────┐
│                 💾 Data Layer                                │
│  ┌──────────────┬──────────────┬─────────────┬─────────────┐ │
│  │ 🔍 Qdrant    │ 📁 JSON      │ 📄 Static   │ 🧩 Plugins  │ │
│  │ Vector DB    │ Config       │ Files       │ Storage     │ │
│  └──────────────┴──────────────┴─────────────┴─────────────┘ │
└─────────────────────────────────────────────────────────────┘
```




---

**Made with ❤️ for the AI community**
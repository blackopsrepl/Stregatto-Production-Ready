<div align="center">

# 🐱 Cheshire Cat AI - Production Ready Local

![Cheshire Cat AI](https://img.shields.io/badge/Cheshire%20Cat-AI%20Assistant-purple?style=for-the-badge&logo=cat)
![Docker](https://img.shields.io/badge/Docker-Ready-blue?style=for-the-badge&logo=docker)
![Kubernetes](https://img.shields.io/badge/k8s-Ready-blue?style=for-the-badge&logo=kubernetes)
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

- 🐳 **Docker** & Docker Compose or Podman (version >= 5.4.2) **OR**
- ☸️ **K3s/Kubernetes** cluster with kubectl configured  
- 💻 **4GB RAM** minimum (8GB recommended)
- 🔌 **2 CPU cores** minimum
- 🛠️ **Make** (usually pre-installed on Linux/macOS)

### **🎯 Super Quick Start (Recommended)**

```bash
# Clone the repository
git clone https://github.com/federicopalma-pro/Stregatto-Production-Ready.git
cd Stregatto-Production-Ready

# 🐳 Docker deployment (one command!)
make docker-up

# ☸️ OR K3s deployment (one command!)
make k3s-deploy
```

✅ That's it! 
- **Docker**: Access at <http://localhost/auth/login>
- **K3s**: Access at <http://localhost:30080/auth/login>

### **📋 Available Commands**

```bash
make help              # 📚 Show all available commands
make env               # 🔑 Generate secure environment keys
make docker-up         # 🐳 Start Docker deployment  
make docker-down       # 🛑 Stop Docker deployment
make k3s-deploy        # ☸️ Deploy to K3s/Kubernetes
make k3s-cleanup       # 🗑️ Clean up K3s deployment
make k3s-status        # 📊 Check K3s deployment status
```

### **🔧 Manual Installation (Alternative)**

<details>
<summary>Click to expand manual installation steps</summary>

#### Docker Deployment
```bash
# Generate environment keys
scripts/generate-env.sh

# Start Docker services
cd docker && docker-compose up -d
```

#### K3s/Kubernetes Deployment  
```bash
# Generate environment keys
scripts/generate-env.sh

# Deploy to K3s
scripts/k3s-deploy.sh
```

</details>

---

## 🔐 **Automated Key Generation**

We provide multiple ways to generate secure API keys and JWT secrets:

### **🛠️ Using Makefile (Recommended)**
```bash
make env                # Generate secure environment keys
```

### **🚀 Direct Scripts**  
```bash
scripts/generate-env.sh     # Linux/macOS
scripts/generate-env.ps1    # Windows (PowerShell)
```

### **📝 Manual Setup (Alternative)**
```bash
# Copy sample and edit manually
cp .env-sample .env
nano .env
```

### **🔑 What Gets Generated**
- **JWT_SECRET** (64 chars): For user authentication tokens
- **API_KEY** (32 chars): For REST API authentication  
- **API_KEY_WS** (32 chars): For WebSocket connections
- **QDRANT_API_KEY** (32 chars): For vector database access

All keys use cryptographically secure random generation with proper entropy.

---

## ⚙️ **Architecture Overview**

```plaintext
🌐 NGINX Reverse Proxy (Port 80 → Load Balancer)
          │
          ▼
🐱 Cheshire Cat Core (Python FastAPI Application)
  ├── 🧠 LLM Integration
  ├── 📝 Embedder Service
  ├── 🧩 Plugins System
  └── 👤 Auth Management
          │
          ▼
💾 Data Layer
  ├── 🔍 Qdrant Vector DB
  ├── 📁 JSON Config
  ├── 📄 Static Files
  └── 🧩 Plugins Storage
```

---

**Made with ❤️ for the AI community**
<div align="center">
  <img src="frontend/public/logo_512.png" alt="Mayura Logo" width="120" height="120">
  
  # Mayura
  
  **Intelligent AI Routing Platform**
  
  *One prompt, perfect AI model selection, superior results.*
  
  [![Next.js](https://img.shields.io/badge/Next.js-14-black.svg)](https://nextjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5-blue.svg)](https://www.typescriptlang.org/)
  [![Go](https://img.shields.io/badge/Go-1.23-00ADD8.svg)](https://golang.org/)
  [![Python](https://img.shields.io/badge/Python-3.9+-3776AB.svg)](https://python.org/)
  [![Docker](https://img.shields.io/badge/Docker-Compose-2496ED.svg)](https://docker.com/)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
  
  [🌐 Live Demo](https://mayura.rocks)
  
</div>

---

## What is Mayura?

Mayura is an **intelligent AI routing platform** that solves the problem of choosing the right AI model for your specific task. Instead of juggling multiple AI services and guessing which one to use, Mayura automatically analyzes your prompt and routes it to the most suitable AI model.

### The Problem We Solve

- **Choice Paralysis**: With dozens of AI models available, which one should you use?
- **Context Switching**: Constantly switching between different AI platforms is inefficient
- **Suboptimal Results**: Using the wrong model for your task leads to poor outcomes
- **Complexity**: Managing multiple API keys, rate limits, and pricing models

### Our Solution

Mayura provides a **single interface** to access the best AI models through intelligent routing:

---

## Key Features

### **Intelligent Routing**
- Automatic prompt analysis and classification
- Context-aware model recommendation

### **Multi-Model Support**
- **Google**: Gemini 2.5 Pro, Gemini 1.5 Pro
- **Meta**: Llama 3.3 70B, Llama 3.1 405B
- **DeepSeek**: DeepSeek R1, DeepSeek V3
- ...can be extended to more models

---

## 🏗️ Architecture

Mayura follows a **microservices architecture** designed for scalability and reliability:

### 🔧 **Tech Stack**

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Infrastructure** | Docker, AWS(Storage), GCP(AI Models, Auth), Azure(Compute) | Deployment and scaling |
| **Frontend** | Next.js 14, React 18, TypeScript | Modern web interface |
| **Gateway** | Go 1.23, Gin, Firebase | API gateway and routing |
| **Classifier** | Python 3.9+, FastAPI, Transformers | AI model classification |
| **Payment** | Go 1.23, LemonSqueezy, DynamoDB | Subscription management |
| **Cache** | Redis 7 | High-performance caching |
| **Database** | DynamoDB, Firebase Firestore | Data persistence |

---

## 🚀 Getting Started

### 📋 Prerequisites

- **Node.js** 18+ and **npm/pnpm**
- **Go** 1.23+
- **Python** 3.9+
- **Docker** and **Docker Compose**

### 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone --recurse-submodules https://github.com/mayuraai/mayura.git
   cd mayura
   ```

2. **Set up environment variables**
   ```bash
   # Frontend
   cp frontend/.env.example frontend/.env
   
   # Backend services
   cp backend/gateway/.env.example backend/gateway/.env
   cp backend/payment/.env.example backend/payment/.env
   ```

   Obtain your Firebase service account JSON file from the Firebase console.
   Copy this file to both `backend/gateway` and `backend/payment` directories, and rename it to `firebase_env.json` in each location.

3. **Install dependencies for frontend**
   ```bash
   # Frontend
   cd frontend
   npm install
   # or
   pnpm install
   ```

4. **Start backend services with Docker**
   ```bash
   cd backend
   docker-compose up -d
   ```

5. **Start the frontend**
   ```bash
   cd frontend
   npm run dev
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Gateway API: http://localhost:8080
   - Classifier API: http://localhost:8000


---

## 🛡️ Security

### **Security Features**
- **JWT Authentication** with refresh tokens
- **Rate limiting** per user and tier
- **CORS protection** with allowlist
- **Request/response logging**

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

<div align="center">
<br/>
<br/>
<br/>
<br/>

  **Built with ❤️ by the Mayura Team**
  
  [Pavan Manish](https://github.com/pavanmanishd) • [Sai Vishal](https://github.com/Vishal0129)
  
  **⭐ If you found this helpful, please give us a star!**
  
</div> 
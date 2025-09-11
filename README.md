# Headlamp Demo 🚀

[![Kubernetes](https://img.shields.io/badge/Kubernetes-KWOK-lightblue?logo=kubernetes)](https://kwok.sigs.k8s.io/)  
[![Docker](https://img.shields.io/badge/Docker-Compose-informational?logo=docker)](https://docs.docker.com/compose/)  
![Platform](https://img.shields.io/badge/platform-linux%20%7C%20macOS%20%7C%20windows-lightgrey)
![License](https://img.shields.io/github/license/mjrgr/rustlet)

A **lightweight demo setup** for running [Headlamp](https://github.com/headlamp-k8s/headlamp) — the open-source Kubernetes web UI.  
This project lets you quickly spin up Headlamp locally with Docker Compose, using a local [KWOK](https://kwok.sigs.k8s.io/).

---

## ✨ Features
- ☸️️ Run and initialize KWOK cluster with Docker Compose
- 🐳 Run Headlamp with Docker Compose
- 🔒 Easy-to-configure environment via `.env`
- 🧩 Clean setup for testing and local exploration
---

## 📦 Prerequisites
Make sure you have:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/) (to verify and manage kwok cluster)
---

## 🚀 Getting Started

1. **Clone this repo**
   ```bash
   git clone https://github.com/mjrgr/headlamp-demo.git
   cd headlamp-demo
   ```

2. **Start the demo**
   ```bash
   docker compose up -d
   ```

3. **Access Headlamp UI**
    - Open [http://localhost:4466](http://localhost:4466) in your browser
    - Login with your cluster context 🎉


4. **Check CLI access**
   ```bash
   kubectl get nodes --kubeconfig ./kubeconfig.yml --context kwok-ext-access
   ```

5. **Clean up**
   ```bash
   docker compose down
   ```

---

## 🛠 Configuration

You can tweak settings in `.env`, for example:

```env
KWOK_K8S_VERSION=1.30.0
HEADLAMP_VERSION=xxx
```

⚠️ KWOK cluster images are available here => [https://github.com/kwok-ci/cluster/pkgs/container/cluster](https://github.com/kwok-ci/cluster/pkgs/container/cluster)
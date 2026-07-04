#  Azure Container Registry (ACR) Demo with Docker

![GitHub Repo Views](https://komarev.com/ghpvc/?username=poornamadhushan\&style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/poornamadhushan/REPOSITORY_NAME?style=for-the-badge)

A beginner-friendly demonstration of how to push a Docker image to **Microsoft Azure Container Registry (ACR)** using the **Azure CLI**.

---

# 📖 Overview

This project demonstrates how to:

* Install Docker
* Install Azure CLI
* Create an Azure Container Registry (ACR)
* Authenticate with Azure
* Tag a Docker image
* Push the image to Azure Container Registry
* Verify the uploaded image

---

# 📋 Prerequisites

Before starting, install the following:

## 1. Docker Desktop

Download and install Docker Desktop.

🔗 https://www.docker.com/products/docker-desktop/

Verify installation:

```bash
docker --version
```

---

## 2. Microsoft Azure Account

Create a free Azure account if you don't already have one.

🔗 https://azure.microsoft.com/free?wt.mc_id=studentamb_378285

---

## 3. Azure CLI

Download and install Azure CLI.

🔗 https://learn.microsoft.com/cli/azure/install-azure-cli

Verify installation:

```bash
az --version
```

---

# 🛠 Demo Steps

## Step 1 — Login to Azure

```bash
az login
```

Authenticates your Azure account.

---

## Step 2 — Login to Azure Container Registry

```bash
az acr login --name <your-acr-name>
```

Authenticates Docker with Azure Container Registry.

---

## Step 3 — Tag Docker Image

```bash
docker tag hello-world <your-acr-name>.azurecr.io/samples/hello-world:v1
```

Creates an Azure-compatible image tag.

---

## Step 4 — Push Docker Image

```bash
docker push <your-acr-name>.azurecr.io/samples/hello-world:v1
```

Uploads the Docker image to Azure Container Registry.

---

## Step 5 — Verify Repository

```bash
az acr repository list --name <your-acr-name> --output table
```

Displays repositories inside ACR.

---

## Step 6 — Verify Image Tags

```bash
az acr repository show-tags --name <your-acr-name> --repository samples/hello-world --output table
```

Shows available image versions.

---

# 📂 Project Workflow

```text
Docker Image
      │
      ▼
Tag Image
      │
      ▼
Azure Container Registry
      │
      ▼
Verify Repository
      │
      ▼
Ready for Deployment
```

---

# 📚 References

* Microsoft Azure Documentation
* Azure CLI Documentation
* Docker Documentation
* Microsoft Learn

---

# 🤝 Contributing

Contributions, issues, and feature requests are welcome.

---

# ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

---

## 👨‍💻 Author

**Poornamadhushan**

GitHub: **@poornamadhushan**

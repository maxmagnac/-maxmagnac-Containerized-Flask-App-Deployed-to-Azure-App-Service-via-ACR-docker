#Containerized Flask App on Azure App Service

A Python Flask application containerized with Docker, pushed to Azure Container Registry (ACR), and deployed to Azure App Service. This project demonstrates a full container-based deployment pipeline on Microsoft Azure.

🌐 Live App

> Deployed via Azure App Service using a Docker container pulled from Azure Container Registry.

📐 Architecture Overview

```
graph LR
 A[Local Machine] -->|docker build| B[Docker Image]
 B -->|docker tag| C[ACR Tagged Image]
 C -->|docker push| D[Azure Container Registry]
 D -->|pull on deploy| E[Azure App Service]
 E -->|serves| F[Live Web App]
```

🛠️ Technologies Used

- Python 3.11 - Application runtime
- Flask - Web framework
- Docker - Containerization
- Azure Container Registry (ACR) - Private container image storage
- Azure App Service - Managed container hosting
- Gunicorn - Production WSGI server
- Azure CLI - Infrastructure management

🏗️ Infrastructure Components

| Component | Name | Purpose |
|---|---|---|
| Container Registry | myportfolioacr2026 | Stores Docker image |
| App Service | myPortfolioApp2026 | Hosts containerized Flask app |
| Docker Image | flask-app:latest | Packaged application |

🚀 Docker Pipeline Steps

1. Build the Image

`bash
docker build -t flask-app .
`

Docker Build (screenshots/screenshot-docker-build.png)

2. Log In to Azure Container Registry

`bash
az acr login --name myportfolioacr2026
`

ACR Login (screenshots/screenshot-acr-login.png)

3. Tag the Image

`bash
docker tag flask-app myportfolioacr2026.azurecr.io/flask-app:latest
`

Docker Tag (screenshots/screenshot-docker-tag.png)

4. Push the Image to ACR

`bash
docker push myportfolioacr2026.azurecr.io/flask-app:latest
`

Docker Push (screenshots/screenshot-docker-push.png)

📸 Deployment Screenshots

ACR Repository
ACR Repository (screenshots/screenshot-1-acr-repository.png)

Environment Variables
Environment Variables (screenshots/screenshot-2-environment-variables.png)

App Service Configuration
App Service Configuration (screenshots/screenshot-3-app-service-configuration.png)

Live App
Live App (screenshots/screenshot-4-live-app.png)

Log Stream
Log Stream (screenshots/screenshot-5-log-stream.png)

📁 Project Structure

`
azure-webapp/
├── app.py
├── Dockerfile
├── requirements.txt
├── .gitignore
├── LICENSE
├── README.md
└── screenshots/
 ├── screenshot-docker-build.png
 ├── screenshot-acr-login.png
 ├── screenshot-docker-tag.png
 ├── screenshot-docker-push.png
 ├── screenshot-1-acr-repository.png
 ├── screenshot-2-environment-variables.png
 ├── screenshot-3-app-service-configuration.png
 ├── screenshot-4-live-app.png
 └── screenshot-5-log-stream.png
`

👤 Author

Maurrin Carter
Cloud Engineer | Azure | Docker | Python
LinkedIn (#) | GitHub (#)

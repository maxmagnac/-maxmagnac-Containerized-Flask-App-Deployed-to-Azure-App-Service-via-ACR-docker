## 1. Build the Image
```bash
docker build -t flask-app .
```
**Docker Build**
![Docker Build](screenshots/screenshot-docker-build.png)

## 2. Log In to Azure Container Registry
```bash
az acr login --name myportfolioacr2026
```
**ACR Login**
![ACR Login](screenshots/screenshot-acr-login.png)

## 3. Tag the Image
```bash
docker tag flask-app myportfolioacr2026.azurecr.io/flask-app:latest
```
**Docker Tag**
![Docker Tag](screenshots/screenshot-docker-tag.png)

## 4. Push the Image to ACR
```bash
docker push myportfolioacr2026.azurecr.io/flask-app:latest
```
**Docker Push**
![Docker Push](screenshots/screenshot-docker-push.png)

## 📸 Deployment Screenshots

### ACR Repository
![ACR Repository](screenshots/screenshot-1-acr-repository.png)

### Environment Variables
![Environment Variables](screenshots/screenshot-2-environment-variables.png)

### App Service Configuration
![App Service Configuration](screenshots/screenshot-3-app-service-configuration.png)

### Live App
![Live App](screenshots/screenshot-4-live-app.png)

### Log Stream
![Log Stream](screenshots/screenshot-5-log-stream.png)

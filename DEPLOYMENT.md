# Guía de Despliegue en AlmaLinux 9

## 1. Preparar el servidor
```bash
sudo dnf update -y
sudo dnf install -y nginx git
curl -fsSL https://rpm.nodesource.com/setup_20.x | sudo bash -
sudo dnf install -y nodejs
sudo npm install -g pm2
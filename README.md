# Project Odoo 19 with Docker and custome Module

## 📌 Descripción
This Project deploys **Odoo 19 Community Edition** on a VPS server using **Docker Compose**, with PostgreSQL like database and volumes for persistence.  
Also, includes a **custome module** that extends the contacts model (`res.partner`) with additional fields.

---

## ⚙️ VPS Configuration

### 1. Update system packages and linux user
```bash
sudo apt update && sudo apt upgrade -y
sudo adduser carlosq
sudo usermod -aG sudo carlosq
```
### 1. Install git
```bash
sudo apt install curl git vim -y
```
### 1. Install and config docker
```bash
sudo apt install docker.io -y
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker carlos
sudo apt install docker-compose -y
```

---

## 🚀 Prerequisites
- VPS with Ubuntu/Debian updated
- Docker y Docker Compose installed
- Git configured

---

## 📂 Project structure

odoo_project/
```text
├── docker-compose.yml
├── README.md
├── config/
│   ├── odoo.conf
├── src/
│   └── partner_extension/
│       ├── manifest.py
│       ├── init.py
│       ├── models/
│       │   └── partner.py
│       └── views/
│           └── partner_view.xml
└── docs/
```
# Launch services once the Project has been cloned.
Create root path: proyecto_odoo/

**On the path run:**
docker-compose up

Login User Odoo:
Email: admin
Password: admin1234

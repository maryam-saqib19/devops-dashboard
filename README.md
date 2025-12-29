
---

## ⚙️ Prerequisites

Make sure the following are installed on your system or server:

- Docker
- Docker Compose
- AWS EC2 instance (Amazon Linux recommended)

---

## 🐳 Docker Services

### docker-compose.yml

The project uses **two containers**:

- **app**
  - Laravel application
  - Runs PHP-FPM on port `9000`

- **nginx**
  - Acts as a reverse proxy
  - Exposes port `8080` to the public

---

## 🔐 Environment Variables

Environment variables are managed using a `.env` file and injected into the Laravel container using Docker Compose.

### Example `.env`

```env
APP_NAME=Laravel
APP_ENV=production
APP_KEY=base64:GENERATED_KEY
APP_DEBUG=false
APP_URL=http://<EC2_PUBLIC_IP>:8080

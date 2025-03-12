# Django Web Application

This is a full-stack web application built with **Django** as the backend and **Webpack** for managing frontend assets. The application is containerized using **Docker** for easy deployment and development.

## 🚀 Features

- Django-based backend with REST capabilities
- Webpack for bundling frontend assets
- Docker support for isolated development and deployment
- Environment configuration using `.env`
- Font and media file support
- Modular app structure for scalability

## 🛠️ Tech Stack

- **Backend:** Django (Python)
- **Frontend:** Webpack (JavaScript bundling)
- **Containerization:** Docker & Docker Compose
- **Deployment:** WSGI (via `core/wsgi.py`)
- **Configuration:** `.env`, `settings.py`

## 📁 Project Structure

```
.
├── core/                   # Main Django project files
├── media_stacksCont/      # Media assets
├── fonts/                 # Fonts used in the app
├── manage.py              # Django CLI utility
├── Dockerfile             # Docker image definition
├── docker-compose.yml     # Docker services configuration
├── requirements.txt       # Python dependencies
├── webpack.config.js      # Frontend build setup
└── .env                   # Environment variables
```

## 🐳 Getting Started (with Docker)

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <project-directory>
```

### 2. Setup `.env` File

Create a `.env` file using the provided template:

```bash
cp .env.example .env
```

Edit the values inside `.env` as needed.

### 3. Build and Run with Docker

```bash
docker-compose up --build
```

The app should be available at `http://localhost:8000`.

## 🧪 Development Commands

### Migrations

```bash
docker-compose exec web python manage.py migrate
```

### Create Superuser

```bash
docker-compose exec web python manage.py createsuperuser
```

### Collect Static Files

```bash
docker-compose exec web python manage.py collectstatic
```

## 📄 License

This project is licensed under the terms of the **MIT License**. See the [LICENSE](./LICENSE) file for details.

# 🏥 Healthcare Management System

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Django](https://img.shields.io/badge/Django-5.x-green?style=for-the-badge&logo=django)
![DRF](https://img.shields.io/badge/Django_REST_Framework-red?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge&logo=postgresql)
![JWT](https://img.shields.io/badge/JWT-Authentication-orange?style=for-the-badge)

A secure backend application built with **Django REST Framework** for managing patients, doctors, and their relationships through RESTful APIs.

The project demonstrates backend engineering concepts including authentication, relational database design, modular architecture, CRUD operations, and API development.

---

# ✨ Features

- 🔐 JWT Authentication
- 👨‍⚕️ Doctor Management
- 🧑 Patient Management
- 🔗 Patient–Doctor Mapping
- ⚡ RESTful APIs
- 🗄 PostgreSQL Integration
- 📦 Modular Django Apps
- 🔄 Full CRUD Operations

---

# 🏗 Architecture

```
                   JWT Authentication
                           │
                           ▼
                  Django REST Framework
                           │
         ┌─────────────────┼─────────────────┐
         ▼                 ▼                 ▼
    Patients           Doctors          Mappings
                           │
                           ▼
                     PostgreSQL
```

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python 3 |
| Framework | Django |
| API | Django REST Framework |
| Authentication | JWT (Simple JWT) |
| Database | PostgreSQL |
| Version Control | Git |

---

# 📂 Project Structure

```text
healthcare_backend/

├── patients/          # Patient APIs & Models
├── doctors/           # Doctor APIs & Models
├── mappings/          # Patient–Doctor Relationships
├── healthcare/        # Project Configuration
├── manage.py
├── requirements.txt
└── README.md
```

---

# 🚀 Getting Started

## 1. Clone Repository

```bash
git clone https://github.com/neha-singh-dev/healthcare-backend-assignment.git
cd healthcare-backend-assignment
```

---

## 2. Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Configure PostgreSQL

Create a PostgreSQL database.

```bash
createdb healthcare_db
```

Update your `settings.py`

```python
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.postgresql",
        "NAME": "healthcare_db",
        "USER": "your_username",
        "PASSWORD": "your_password",
        "HOST": "localhost",
        "PORT": "5432",
    }
}
```

---

## 5. Apply Migrations

```bash
python manage.py migrate
```

---

## 6. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

---

## 7. Run Development Server

```bash
python manage.py runserver
```

Server runs at

```
http://127.0.0.1:8000/
```

---

# 🔐 Authentication

This project uses **JSON Web Token (JWT)** authentication.

### Login

**POST**

```
/api/auth/login/
```

Request

```json
{
    "username": "your_username",
    "password": "your_password"
}
```

Response

```json
{
    "refresh": "<JWT_REFRESH_TOKEN>",
    "access": "<JWT_ACCESS_TOKEN>"
}
```

For protected endpoints include

```
Authorization: Bearer <ACCESS_TOKEN>
```

---

# 📡 API Endpoints

| Resource | Endpoints |
|-----------|-----------|
| Patient | GET, POST `/api/patients/` |
| Patient | GET, PUT, DELETE `/api/patients/<id>/` |
| Doctor | GET, POST `/api/doctors/` |
| Doctor | GET, PUT, DELETE `/api/doctors/<id>/` |
| Mapping | GET, POST `/api/mappings/` |
| Mapping | GET, PUT, DELETE `/api/mappings/<id>/` |

---

# 📝 Example Requests

## Create Patient

```json
{
    "name": "John Doe",
    "age": 35,
    "medical_history": "Lung Cancer"
}
```

Response

```json
{
    "id": 1,
    "name": "John Doe",
    "age": 35,
    "medical_history": "Lung Cancer"
}
```

---

## Create Doctor

```json
{
    "name": "Dr. Smith",
    "specialization": "Cardiology",
    "email": "drsmith@example.com",
    "experience_years": 7
}
```

---

## Create Mapping

```json
{
    "patient": 1,
    "doctor": 1
}
```

---

# 💡 Skills Demonstrated

- Backend Development
- Django REST Framework
- REST API Design
- JWT Authentication
- PostgreSQL Integration
- Database Relationships
- CRUD Operations
- Modular Django Architecture

---

# 🔮 Future Improvements

- 👥 Role-Based Access Control (RBAC)
- 📅 Appointment Scheduling
- 📄 Medical Records Module
- 📑 Swagger / OpenAPI Documentation
- 🐳 Docker Support
- ✅ Unit & Integration Testing
- ☁️ Cloud Deployment (Render / Railway / AWS)

---

# 👩‍💻 Author

**Neha Singh**

Backend Developer • Python • Django • REST APIs

GitHub: https://github.com/neha-singh-dev

---

⭐ If you found this project interesting, consider giving it a star!

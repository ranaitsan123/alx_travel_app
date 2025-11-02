# ALX Travel App

A fully containerized web-based travel application built with **Django**, **MySQL**, and **Docker**. The app provides a travel listings feature and a REST API documented with Swagger, demonstrating modern web development and deployment practices.

## Table of Contents

- Project Overview
- Features
- Tools & Technologies
- Project Structure
- Setup & Installation
- Usage
- Contributing
- License

## Project Overview

**ALX Travel App** allows users to browse and manage travel listings.  
The backend is powered by Django and MySQL, all orchestrated using Docker Compose for easy development and deployment.

This project demonstrates:

- Django fundamentals (models, views, URLs, migrations)
- MySQL database integration
- Automatic API documentation with Swagger UI
- Containerization using Docker

## Features

- View travel listings at: `/listings/`
- Admin panel for managing data: `/admin/`
- REST API documentation via Swagger: `/swagger/`
- Entire environment runs in Docker for easy setup and portability

## Tools & Technologies

| Category | Technology |
|---------|------------|
| Backend Framework | Django 5.2.x |
| Database | MySQL 8.4.x |
| Containerization | Docker & Docker Compose |
| API Documentation | Swagger UI |
| Programming Language | Python 3.12+ |
| Version Control | Git & GitHub |

## Project Structure

```
alx_travel_app/
├─ alx_travel_app/        # Django project settings
│  ├─ settings.py
│  ├─ urls.py
│  └─ wsgi.py
├─ listings/              # Travel listings app
│  ├─ models.py
│  ├─ views.py
│  └─ urls.py
├─ Dockerfile
├─ docker-compose.yml
└─ requirements.txt
```

## Setup & Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/alx_travel_app.git
   cd alx_travel_app
   ```

2. Start the containers
   ```bash
   docker-compose up -d
   ```

   This launches:
   - `travel_web` (Django application)
   - `travel_db` (MySQL database)

3. Apply database migrations
   ```bash
   docker exec -it travel_web python manage.py migrate
   ```

4. Create a superuser (for admin access)
   ```bash
   docker exec -it travel_web python manage.py createsuperuser
   ```

5. Access the application
   - Listings: http://localhost:8000/listings/
   - Admin Panel: http://localhost:8000/admin/
   - Swagger Docs: http://localhost:8000/swagger/

## Usage

- Manage travel listings using the Django **Admin Panel**
- Query the API using Swagger UI
- Extend functionality by adding new Django apps, models, and endpoints

## Contributing

1. Fork the repository
2. Create a new feature branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Submit a Pull Request

## License

This project is licensed under the **MIT License**.

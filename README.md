# LMS - Learning Management System

A powerful and scalable Learning Management System (LMS) built using **FastAPI**, **PostgreSQL**, and modern backend architecture. Designed to provide a seamless experience for administrators, educators, and learners.

---

## Tech Stack

| Technology      | Purpose                         |
|-----------------|---------------------------------|
| **FastAPI**     | High-performance API framework  |
| **PostgreSQL**  | Relational database             |
| **SQLAlchemy**  | ORM for database interaction    |
| **Alembic**     | Database migrations             |
| **Pydantic**    | Data validation and settings    |
| **Docker**      | Containerization                |
| **JWT/Authlib** | Authentication & Authorization  |
| **Uvicorn**     | ASGI server for FastAPI         |
| **Pytest**      | Testing framework               |

---

## Features

- User Authentication (JWT)
- Role Management (Admin, Instructor, Student)
- Course Management (Create, Edit, Delete)
- Enrollment System
- Assignment Submissions
- Grading System
- Announcements and Notifications
- RESTful API Structure
- Database Migrations with Alembic
- Dockerized for Easy Deployment

---

## Project Structure

```
lms/
├── app/
│   ├── api/               # API routes
│   ├── core/              # Core configurations
│   ├── models/            # Database models
│   ├── schemas/           # Pydantic schemas
│   ├── services/          # Business logic
│   ├── db/                # DB session and migrations
│   └── main.py            # Entry point
├── tests/                 # Test cases
├── alembic/               # Migrations
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

## Getting Started

### Prerequisites

- Python 3.10+
- Docker & Docker Compose
- Make (optional)

---

### Run Locally (Using Docker)

```bash
# Clone the repo
git clone https://github.com/your-username/lms-fastapi.git
cd lms-fastapi

# Build and start services
docker-compose up --build
```

The API will be available at:

**http://localhost:8000/docs**

---

### Run Locally (Manual Setup)

```bash
python -m venv venv
source venv/bin/activate

pip install -r requirements.txt

# Run database migrations
alembic upgrade head

# Start the app
uvicorn app.main:app --reload
```

---

## API Documentation

FastAPI provides an interactive Swagger UI at:

- **http://localhost:8000/docs**

Or use ReDoc:

- **http://localhost:8000/redoc**

---

## Environment Variables

Create a `.env` file in the root directory:

```
DATABASE_URL=postgresql://postgres:postgres@db:5432/lms
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

## Testing

```bash
pytest
```

---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## License

[MIT](LICENSE)

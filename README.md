
# Order Fulfillment & Inventory Management Platform

A backend REST API built with FastAPI and PostgreSQL to manage orders, inventory, warehouses, returns, and fulfillment operations.

## Features

- JWT authentication and role-based authorization
- User and warehouse management
- Product and category management
- Inventory tracking and stock adjustments
- Inventory reservation during order creation
- Order processing and status history
- Fulfillment agent assignment
- Order cancellation and stock release
- Return and refund management
- Notifications and low-stock alerts
- Audit logging
- Idempotency support for order creation
- Database transactions and row-level locking
- Pagination for list endpoints
- Scheduled background jobs

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| FastAPI | REST API framework |
| PostgreSQL | Relational database |
| SQLAlchemy | ORM and database operations |
| Alembic | Database migrations |
| Pydantic | Data validation |
| JWT | Authentication |
| APScheduler | Background jobs |
| Pytest | Testing framework |

## User Roles

- Admin
- Warehouse Manager
- Fulfillment Agent
- Customer

## Project Structure

```text
order_fulfillment_platform/
├── alembic/
├── app/
│   ├── background/
│   ├── core/
│   ├── models/
│   ├── repositories/
│   ├── routers/
│   ├── schemas/
│   ├── services/
│   └── utils/
├── docs/
├── postman/
├── tests/
├── .env
├── .gitignore
├── alembic.ini
├── requirements.txt
└── README.md
```

## Setup and Installation

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd order_fulfillment_platform
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the environment

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 5. Configure environment variables

Create a `.env` file and configure your PostgreSQL database URL, JWT secret, and application settings.

Do not commit your actual `.env` file.

### 6. Apply database migrations

```bash
python -m alembic upgrade head
```

### 7. Start the application

```bash
python -m uvicorn app.main:app --reload
```

## API Documentation

After starting the server, open:

- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

## Database Migrations

Create a migration:

```bash
python -m alembic revision --autogenerate -m "migration_message"
```

Apply migrations:

```bash
python -m alembic upgrade head
```

## Current Project Status

- Database migrations applied successfully.
- Main application dependencies imported successfully.
- Database connection and Alembic migration verified.
- Automated test cases have not yet been added.

## Author

Developed as a backend project demonstrating REST API development, authentication, database management, inventory control, and order fulfillment using FastAPI and PostgreSQL.

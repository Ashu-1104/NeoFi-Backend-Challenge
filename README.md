# NeoFi-Backend-Challenge
# Collaborative Event Management System - NeoFi Backend Challenge

This is a RESTful API backend built with FastAPI for managing events with collaborative editing, version control, and role-based sharing.

## Features

- JWT Authentication (Register, Login, Logout)
- Role-based Access Control (Owner, Editor, Viewer)
- Create, Update, Delete Events
- Recurring Event Support
- Share Events with Granular Permissions
- View/Edit History with Versioning and Rollback
- Changelog Diff Between Versions
- PostgreSQL + SQLAlchemy ORM
- Swagger API Docs

---

## Tech Stack

- FastAPI
- PostgreSQL
- SQLAlchemy
- Alembic (migrations)
- JWT (python-jose)
- Uvicorn (server)

---

## Installation

```bash
# 1. Clone the repository or unzip the project
git clone <[your-repo-url](https://github.com/Ashu-1104/NeoFi-Backend-Challenge)>
cd event_management

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up environment variables
cp .env.example .env
# Edit .env to include your PostgreSQL connection string

# 5. Run migrations
alembic upgrade head

# 6. Start server
uvicorn main:app --reload

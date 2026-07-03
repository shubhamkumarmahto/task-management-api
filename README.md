# 🚀 Task Management API

A RESTful Task Management API built using **FastAPI**, **PostgreSQL**, **SQLAlchemy**, **Alembic**, and **JWT Authentication**. This project allows users to register, log in, and securely manage their personal tasks.

---

## 📌 Features

* User Registration
* User Login (JWT Authentication)
* Create Task
* Update Task
* Delete Task
* Get All Tasks
* Get Single Task
* Mark Task as Completed
* Search Tasks
* Protected Routes using JWT
* PostgreSQL Database
* Database Migrations with Alembic

---

## 🛠 Tech Stack

* Python 3
* FastAPI
* PostgreSQL
* SQLAlchemy
* Alembic
* Pydantic
* JWT (python-jose)
* Uvicorn

---

## 📂 Project Structure

```
task-management-api/
│
├── src/
│   ├── user/
│   ├── task/
│   ├── utils/
│   └── ...
│
├── migrations/
├── main.py
├── alembic.ini
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/task-management-api.git
```

```bash
cd task-management-api
```

---

### Create Virtual Environment

#### macOS/Linux

```bash
python3 -m venv env
source env/bin/activate
```

#### Windows

```bash
python -m venv env
env\Scripts\activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Create a `.env` File

```env
DB_CONNECTION=postgresql://username:password@localhost:5432/database_name

SECRET_KEY=your_secret_key

ALGORITHM=HS256

EXP_TIME=60
```

---

### Run Database Migrations

```bash
alembic upgrade head
```

---

### Start the Server

```bash
fastapi dev main.py
```

or

```bash
uvicorn main:app --reload
```

---

## 📖 API Endpoints

### Authentication

| Method | Endpoint       | Description   |
| ------ | -------------- | ------------- |
| POST   | /user/register | Register User |
| POST   | /user/login    | Login User    |
| GET    | /user/is_auth  | Verify JWT    |

---

### Tasks

| Method | Endpoint   | Description    |
| ------ | ---------- | -------------- |
| POST   | /task      | Create Task    |
| GET    | /task      | Get All Tasks  |
| GET    | /task/{id} | Get Task by ID |
| PUT    | /task/{id} | Update Task    |
| DELETE | /task/{id} | Delete Task    |

---

## 🔐 Authentication

This project uses **JWT (JSON Web Tokens)** for authentication.

Protected endpoints require the following header:

```
Authorization: Bearer <your_jwt_token>
```

---

## 🧪 Testing

You can test the API using:

* Swagger UI
* Postman
* Thunder Client (VS Code)

Swagger Documentation:

```
http://127.0.0.1:8000/docs
```

---

## 🚀 Future Improvements

* Task Categories
* Task Priority
* Due Date
* Pagination
* Sorting
* Email Verification
* Password Reset
* Docker Support
* CI/CD Pipeline
* AWS Deployment

---

## 👨‍💻 Author

**Shubham Mahto**

GitHub: https://github.com/shubhamkumarmahto

---

## ⭐ If you like this project

Give this repository a ⭐ on GitHub!

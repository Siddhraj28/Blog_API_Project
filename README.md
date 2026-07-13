# 📝 Blog API Project

A RESTful Blog API built with **FastAPI**, **SQLAlchemy**, and **JWT Authentication**. This project demonstrates CRUD operations, secure authentication, pagination, search functionality, and PostgreSQL database integration.

---

## 🚀 Features

- 🔐 JWT Authentication
- ✍️ Create Blog (Protected)
- 📖 Read All Blogs
- 📄 Read Single Blog
- ✏️ Update Blog (Protected)
- 🗑️ Delete Blog (Protected)
- 🔍 Search Blogs by Title
- 📑 Pagination
- 🗄️ PostgreSQL Database
- ✅ Pydantic Request & Response Validation
- ⚡ FastAPI Automatic Swagger Documentation

---

## 🛠️ Tech Stack

- Python 3.x
- FastAPI
- SQLAlchemy
- PostgreSQL
- JWT (python-jose)
- Pydantic
- Uvicorn
- python-dotenv

---

## 📂 Project Structure

```
Blog_API_Project/
│
├── auth.py             # JWT Authentication
├── database.py         # Database Configuration
├── main.py             # API Routes
├── models.py           # SQLAlchemy Models
├── schemas.py          # Pydantic Schemas
├── requirements.txt
├── .env
└── README.md
```

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/Siddhraj28/Blog_API_Project.git

cd Blog_API_Project
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure Environment Variables

Create a `.env` file.

```env
DATABASE_URL=postgresql://username:password@localhost/blogdb

SECRET_KEY=your_secret_key

ALGORITHM=HS256

ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

### 5. Run the Server

```bash
uvicorn main:app --reload
```

Server will start at:

```
http://127.0.0.1:8000
```

---

## 📚 API Documentation

Swagger UI

```
http://127.0.0.1:8000/docs
```

ReDoc

```
http://127.0.0.1:8000/redoc
```

---

# 🔑 Authentication

Generate JWT Token

### POST

```
/login
```

Response

```json
{
  "access_token": "your_jwt_token",
  "token_type": "bearer"
}
```

Use the token in the Authorization header.

```
Authorization: Bearer <your_token>
```

---

# 📌 API Endpoints

| Method | Endpoint | Description | Authentication |
|---------|----------|-------------|---------------|
| POST | `/login` | Generate JWT Token | ❌ |
| POST | `/blog` | Create Blog | ✅ |
| GET | `/blog` | Get All Blogs | ❌ |
| GET | `/blog/{id}` | Get Blog by ID | ❌ |
| PUT | `/blog/{id}` | Update Blog | ✅ |
| DELETE | `/blog/{id}` | Delete Blog | ✅ |

---

## 🔍 Search

```
GET /blog?search=fastapi
```

---

## 📑 Pagination

```
GET /blog?page=1&limit=5
```

---

## 📦 Sample Request

```json
{
    "title":"FastAPI Tutorial",
    "content":"FastAPI is a modern web framework for building APIs."
}
```

---

## 🏆 Future Improvements

- User Registration
- Password Hashing (bcrypt)
- User Login with Username & Password
- Refresh Tokens
- Docker Support
- Unit Testing
- Alembic Database Migrations
- Role-Based Authorization
- File Upload Support

---

## 👨‍💻 Author

**Siddhraj Dabhi**

- GitHub: https://github.com/Siddhraj28
- LinkedIn: www.linkedin.com/in/siddhraj-dabhi

---

## 📄 License

This project is licensed under the MIT License.

⭐ If you found this project helpful, don't forget to star the repository!

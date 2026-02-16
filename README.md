# SDS ERP Backend

SDS ERP Backend is a RESTful API built with **Flask (Python)** that handles core ERP functionalities such as user management, departments, attendance, leaves, permissions, tasks, and more.  
This backend is designed to work with a frontend ERP application to deliver a complete enterprise resource planning solution.

---

## 🚀 Features

- User Authentication (JWT)
- User Management (Create, Read, Update, Delete)
- Department & Designation API
- Attendance Recording
- Leave & Permission Requests
- Task Management
- Role & Access Control
- RESTful API Design

---

## 🛠️ Tech Stack

- Python 3.x  
- Flask  
- Flask-SQLAlchemy  
- Flask-Migrate  
- Flask-JWT-Extended  
- MySQL or SQLite  
- REST API Architecture

---

## 📁 Project Structure

```
sdserp/
│
├── app/
│   ├── auth/
│   ├── users/
│   ├── departments/
│   ├── attendance/
│   ├── leaves/
│   ├── permissions/
│   ├── tasks/
│   └── __init__.py
│
├── migrations/
├── config.py
├── run.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```
git clone https://github.com/mahalakshmi0606/sdserp.git
cd sdserp
```

### 2. Create a Virtual Environment

```
python -m venv venv
```

Activate the environment:

Windows:
```
venv\Scripts\activate
```

Mac/Linux:
```
source venv/bin/activate
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

---

## 🗄️ Database Configuration

Create your database and update the configuration in `config.py`:

Example for MySQL:

```
SQLALCHEMY_DATABASE_URI = "mysql+pymysql://username:password@localhost/sds_erp_db"
```

Or using SQLite:

```
SQLALCHEMY_DATABASE_URI = "sqlite:///sds_erp.db"
```

---

## 🔄 Run Database Migrations

```
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```

---

## ▶️ Run the Application

```
python run.py
```

The backend server will run at:

```
http://127.0.0.1:5000
```

---

## 📡 API Endpoints

### Authentication
- `POST /api/auth/login` – User login

### Users
- `GET /api/users` – List all users
- `POST /api/users` – Create new user
- `PUT /api/users/<id>` – Update user
- `DELETE /api/users/<id>` – Delete user

### Departments
- `GET /api/departments`
- `POST /api/departments`
- `PUT /api/departments/<id>`
- `DELETE /api/departments/<id>`

### Attendance
- `GET /api/attendance`
- `POST /api/attendance`

### Leaves & Permissions
- `GET /api/leaves`
- `POST /api/leaves`
- `GET /api/permissions`
- `POST /api/permissions`

### Tasks
- `GET /api/tasks`
- `POST /api/tasks`

---

## 🔐 Environment Variables

```
FLASK_ENV=development
SECRET_KEY=your_secret_key
JWT_SECRET_KEY=your_jwt_secret
```

---

## 🤝 Contributing

1. Fork the repository  
2. Create a new branch  
3. Make your changes  
4. Commit and push  
5. Open a Pull Request

---

## 👩‍💻 Author

**Mahalakshmi M**  
Full Stack Developer

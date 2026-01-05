🧳 Trip Management System

Full-Stack Web Application (Django REST + React + JWT Authentication)

A production-ready Trip Management System that allows users to securely manage their trips.
Built with Django REST Framework on the backend and React on the frontend, featuring JWT authentication, protected routes, and user-specific data access.

🚀 Features
🔐 Authentication & Security

JWT authentication (access & refresh tokens)

Protected routes (frontend + backend)

User-specific data isolation (users only see their own trips)

Secure API endpoints using DRF permissions

🧭 Trip Management (CRUD)

Create trips

Edit trips

Delete trips

View personal trip list

Each trip belongs to the authenticated user

🖥️ Frontend

React with functional components & hooks

Axios API layer with JWT interceptor

Login & logout flow

Protected dashboard

Clean and simple UI

⚙️ Backend

Django REST Framework

ModelViewSet architecture

JWT (SimpleJWT)

SQLite (development-ready, easy to swap for PostgreSQL)

🛠️ Tech Stack

Frontend

React

React Router

Axios

JavaScript (ES6+)

Backend

Django

Django REST Framework

SimpleJWT

SQLite (development)

Authentication

JSON Web Tokens (JWT)

📂 Project Structure
trip-management-system/
│
├── backend/
│   ├── backend/
│   ├── trips/
│   ├── manage.py
│   └── db.sqlite3
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── pages/
│   │   └── utils/
│   └── package.json
│
└── README.md

⚙️ Backend Setup
1️⃣ Create Virtual Environment
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

2️⃣ Install Dependencies
pip install django djangorestframework djangorestframework-simplejwt django-cors-headers

3️⃣ Run Migrations
python manage.py makemigrations
python manage.py migrate

4️⃣ Create Superuser
python manage.py createsuperuser

5️⃣ Start Backend Server
python manage.py runserver


Backend runs at:

http://127.0.0.1:8000/

⚙️ Frontend Setup
1️⃣ Install Dependencies
cd frontend
npm install

2️⃣ Start Frontend
npm start


Frontend runs at:

http://localhost:3000/

🔑 Authentication Endpoints
Method	Endpoint	Description
POST	/api/login/	Get access & refresh token
POST	/api/refresh/	Refresh access token
GET	/api/trips/	Get user trips (auth required)
POST	/api/trips/	Create trip
PUT	/api/trips/:id/	Update trip
DELETE	/api/trips/:id/	Delete trip
🧠 How It Works

User logs in → receives JWT tokens

Tokens stored in localStorage

Axios automatically attaches token to every request

Backend filters trips by request.user

Protected routes prevent unauthorized access

🎯 Why This Project Matters

✔ Demonstrates real-world authentication
✔ Shows full CRUD with permissions
✔ Clean full-stack architecture
✔ Production-ready foundation
✔ Recruiter-friendly & scalable

🧑‍💻 Author

Banu Mariwan
Full-Stack Developer (Django + React)

GitHub:
👉 https://github.com/banumariwan

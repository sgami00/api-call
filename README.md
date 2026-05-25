api call

API call in Laravel are requests sent between the client and server to perform operations such as retrieving, creating, updating, or deleting data. Each API call uses an HTTP method like GET, POST, PUT, PATCH, or DELETE to specify the action being performed on the resource.

# Student API System

A simple RESTful API built using Laravel for managing student records.

---

# Features

* Fetch all students
* Fetch one student by ID
* Create a new student
* Update student information
* Partially update student information
* Delete one student
* Delete all students

---

# Technologies Used

* PHP
* Laravel
* MySQL
* Postman

---

# Installation Guide

## Step 1 — Clone the Repository

```bash
git clone https://github.com/your-username/student-api.git
```

---

## Step 2 — Open the Project Folder

```bash
cd student-api
```

---

## Step 3 — Install Dependencies

```bash
composer install
```

---

## Step 4 — Configure Environment File

Copy the `.env.example` file:

```bash
cp .env.example .env
```

Generate application key:

```bash
php artisan key:generate
```

---

## Step 5 — Configure Database

Open the `.env` file and update:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=student_db
DB_USERNAME=root
DB_PASSWORD=
```

Create the database in MySQL Workbench or phpMyAdmin.

---

## Step 6 — Run Database Migration

```bash
php artisan migrate
```

---

## Step 7 — Start Laravel Server

```bash
php artisan serve
```

Server URL:

```txt
http://127.0.0.1:8000
```

---

# API Routes

| Method | Endpoint             | Description         |
| ------ | -------------------- | ------------------- |
| GET    | `/api/students`      | Fetch all students  |
| GET    | `/api/students/{id}` | Fetch one student   |
| POST   | `/api/students`      | Create new student  |
| PUT    | `/api/students/{id}` | Update student      |
| PATCH  | `/api/students/{id}` | Partial update      |
| DELETE | `/api/students/{id}` | Delete one student  |
| DELETE | `/api/students`      | Delete all students |

---

# Example API Requests

## GET All Students

```http
GET /api/students
```

---

## POST Create Student

```http
POST /api/students
```

Example JSON Body:

```json
{
  "name": "John Doe",
  "course": "BSIT"
}
```

---

## PUT Update Student

```http
PUT /api/students/1
```

Example JSON Body:

```json
{
  "name": "Jane Doe",
  "course": "BSCS"
}
```

---

## DELETE Student

```http
DELETE /api/students/1
```

---

# Testing Using Postman

1. Open Postman
2. Create a new request
3. Select HTTP Method
4. Enter API URL
5. Click Send

Example URL:

```txt
http://127.0.0.1:8000/api/students
```

---

# Project Structure

```txt
app/
 ├── Http/
 │    └── Controllers/
 │         └── StudentsController.php
 ├── Models/
 │    └── Student.php
routes/
 └── api.php
database/
 └── migrations/
```





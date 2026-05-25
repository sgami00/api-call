api-call

Short Description:

API call in Laravel are requests sent between the client and server to perform operations such as retrieving, creating, updating, or deleting data. Each API call uses an HTTP method like GET, POST, PUT, PATCH, or DELETE to specify the action being performed on the resource.


Instructions in api call

# Student API System

A simple RESTful API built using Laravel for managing student records. This project allows users to perform CRUD operations such as creating, retrieving, updating, and deleting student information using API endpoints.

---

## Features

- Fetch all students
- Fetch student by ID
- Create new student
- Update student information
- Partially update student information
- Delete one student
- Delete all students

---

## Technologies Used

- PHP
- Laravel
- MySQL
- Postman
- Composer
- Git

---

# Installation Guide

Follow the steps below to clone and run the project on your local machine.

---

## Step 1 — Clone the Repository

Open Terminal, Git Bash, Command Prompt, or VS Code Terminal and run:

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

Install Laravel dependencies using Composer:

```bash
composer install
```

---

## Step 4 — Setup Environment File

Copy the `.env.example` file:

```bash
cp .env.example .env
```

Generate the Laravel application key:

```bash
php artisan key:generate
```

---

## Step 5 — Configure Database

Open the `.env` file and update the database configuration:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=student_db
DB_USERNAME=root
DB_PASSWORD=
```

---

## Step 6 — Create Database

Open MySQL Workbench or phpMyAdmin and create a database named:

```txt
student_db
```

---

## Step 7 — Run Database Migration

```bash
php artisan migrate
```

This command creates the necessary database tables.

---

## Step 8 — Run Laravel Server

```bash
php artisan serve
```

Server URL:

```txt
http://127.0.0.1:8000
```

---

# API Endpoints

| Method | Endpoint | Description |
|--------|-----------|-------------|
| GET | `/api/students` | Fetch all students |
| GET | `/api/students/{id}` | Fetch one student |
| POST | `/api/students` | Create new student |
| PUT | `/api/students/{id}` | Update student |
| PATCH | `/api/students/{id}` | Partial update student |
| DELETE | `/api/students/{id}` | Delete one student |
| DELETE | `/api/students` | Delete all students |

---

# API Request Examples

## GET All Students

```http
GET /api/students
```

Example URL:

```txt
http://127.0.0.1:8000/api/students
```

---

## GET Student by ID

```http
GET /api/students/1
```

---

## POST Create Student

```http
POST /api/students
```

JSON Body:

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

JSON Body:

```json
{
  "name": "Jane Doe",
  "course": "BSCS"
}
```

---

## PATCH Partial Update Student

```http
PATCH /api/students/1
```

JSON Body:

```json
{
  "course": "BS Information Technology"
}
```

---

## DELETE Student

```http
DELETE /api/students/1
```

---

# Testing API Using Postman

1. Open Postman
2. Create a new request
3. Select HTTP method
4. Enter API URL
5. Add JSON body if needed
6. Click **Send**

Example URL:

```txt
http://127.0.0.1:8000/api/students
```

---

<h1>Project Structure</h1>


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

Common Laravel Commands

Run Server

php artisan serve


Run Migration

php artisan migrate


Clear Cache

php artisan optimize:clear


Author

Developed using Laravel API-call for educational purposes.

Google Drive link video

https://drive.google.com/drive/folders/1pblfwm5rVkCM5B4sOMp6_e2d_Sd85W6n?usp=sharing
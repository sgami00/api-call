# API CALL

API calls in Laravel are requests sent between the client and server to perform operations such as retrieving, creating, updating, or deleting data. Each API call uses an HTTP method like GET, POST, PUT, PATCH, or DELETE to specify the action being performed on the resource.

---

# Installation Guide

Follow the steps below to clone and run the project on your local machine.

---

## Step 1 — Clone the Repository

Open Terminal, Git Bash, Command Prompt, or VS Code Terminal and run:

git clone https://github.com/your-username/student-api.git


---

## Step 2 — Open the Project Folder

cd student-api


---

## Step 3 — Install Dependencies

Install Laravel dependencies using Composer:

composer install


---

## Step 4 — Setup Environment File

Copy the `.env.example` file:


cp .env.example .env


Generate the Laravel application key:

php artisan key:generate


---

## Step 5 — Configure Database

Open the `.env` file and update the database configuration:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=student_db
DB_USERNAME=root
DB_PASSWORD=
```
## Take Note

Depending on the name of your database

---

## Step 6 — Create Database

Open MySQL Workbench or SQLite and create a database named:


student_db or It depends on the name of your database


---

## Step 7 — Run Database Migration

php artisan migrate

This command creates the necessary database tables.

---

## Step 8 — Run Laravel Server

php artisan serve


Server URL:


http://127.0.0.1:8000


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


GET /api/students


Example URL:


http://127.0.0.1:8000/api/students

---

## GET Student by ID


GET http://127.0.0.1:8000/api/students/1


---

## POST Create Student


POST http://127.0.0.1:8000/api/students


JSON Body:


{
  "name": "John Doe",
  "email": "JDoe@email.com" ,
  "course": "BSIT"
}


---

## PUT Update Student


PUT http://127.0.0.1:8000/api/students/1


JSON Body:

{
  "name": "Jane Doe",
  "email": "JDoe@email.com" ,
  "course": "BSCS"
}


---

## PATCH Partial Update Student


PATCH http://127.0.0.1:8000/api/students/1


JSON Body:

{
  "course": "BS Information Technology"
}


---

## DELETE Student

DELETE http://127.0.0.1:8000/api/students/1


---

# Testing API Using Postman

1. Open Postman
2. Create a new request
3. Select HTTP method
4. Enter API URL
5. Add JSON body if needed
6. Click **Send**

Example URL:


http://127.0.0.1:8000/api/students


---

# Project Structure

```
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

---

# Common Laravel Commands

## Run Server


php artisan serve


## Run Migration

php artisan migrate


## Clear Cache

php artisan optimize:clear



# Author

Developed using Laravel API-call for educational purposes.

Google Drive link video

https://drive.google.com/drive/folders/1pblfwm5rVkCM5B4sOMp6_e2d_Sd85W6n?usp=sharing
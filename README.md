api call

API call in Laravel are requests sent between the client and server to perform operations such as retrieving, creating, updating, or deleting data. Each API call uses an HTTP method like GET, POST, PUT, PATCH, or DELETE to specify the action being performed on the resource.

Instructions in api call

Student API System

A simple RESTful API project built with Laravel for managing student records. This API allows users to create, retrieve, update, and delete student information using different HTTP requests.

Features
View all students
View a single student by ID
Add new student records
Update existing student information
Partially update student details
Delete a specific student
Delete all student records

Built With
PHP
Laravel
MySQL
Postman

Installation
1. Clone the Repository
git clone https://github.com/your-username/student-api.git
2. Go to the Project Folder
cd student-api
3. Install Laravel Dependencies
composer install
4. Setup Environment File

Copy the example environment file:

cp .env.example .env

Generate the application key:

php artisan key:generate
5. Configure the Database

Open the .env file and update the database credentials:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=student_db
DB_USERNAME=root
DB_PASSWORD=

After that, create a database named:

student_db

You can create it using MySQL Workbench or phpMyAdmin.

6. Run Migration
php artisan migrate

This will create the necessary tables in the database.

7. Run the Laravel Server
php artisan serve

The project will run at:

http://127.0.0.1:8000
API Endpoints
Method	Endpoint	Description
GET	/api/students	Get all students
GET	/api/students/{id}	Get student by ID
POST	/api/students	Create a student
PUT	/api/students/{id}	Update student
PATCH	/api/students/{id}	Partially update student
DELETE	/api/students/{id}	Delete one student
DELETE	/api/students	Delete all students
Sample Requests
Get All Students
GET /api/students
Create Student
POST /api/students

Request Body:

{
  "name": "Test1",
  "email": "Test1@gmail.com",
  "course": "BSIT"
}
Update Student
PUT /api/students/1

Request Body:

{
  "name": "Test1",
  "email": "Test1@gmail.com",
  "course": "BSCS"
}
Delete Student
DELETE /api/students/1
Testing the API in Postman
Open Postman
Create a new request
Choose the HTTP method
Enter the API endpoint
Click Send

Example:
http://127.0.0.1:8000/api/students
Project Structure
app/
 ├── Http/
 │    └── Controllers/
 │         └── StudentsController.php
 │
 ├── Models/
 │    └── Student.php
 │
routes/
 └── api.php
 │
database/
 └── migrations/

Note:
Make sure MySQL is running before starting the Laravel server.
Use Postman to test all API endpoints.
Migration must be completed before using the API.





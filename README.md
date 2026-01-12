# Employee_Management_System
A full stack Employee management System built using Lightweight operations.
Step 1:
Setup Database(MySQL Workbench->New Query and run:

CREATE DATABASE employee_system;
USE employee_system;

CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
email VARCHAR(100),
password VARCHAR(100)
);

INSERT INTO users (email, password) VALUES
('admin@test.com', '123456');

CREATE TABLE employees (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
email VARCHAR(100),
department VARCHAR(100)
);

CREATE TABLE leaves (
id INT AUTO_INCREMENT PRIMARY KEY,
employee_name VARCHAR(100),
reason VARCHAR(200),
from_date DATE,
to_date DATE,
status VARCHAR(20) DEFAULT 'Pending'
);

CREATE TABLE attendance (
id INT AUTO_INCREMENT PRIMARY KEY,
employee_name VARCHAR(100),
date DATE,
status VARCHAR(20)
);

Step 2:
Backend Setup:

Open Terminal:
cd employee-system/backend
npm install
npx nodemon index.js

Then you should see:
Server running on http://localhost:5000
MySQL Connected
Backend runs.

Step 3:
Frontend Setup:

Open new Terminal:
cd employee-system/frontend
npm install
npm start

Then you should see
Frontend runs at:http://localhost:3000/

Login Details:
Email: admin@test.com
Password: 123456

Key Features of the Project:
Authentication System
 Secure login using email and password
 Only authenticated users can access system modules
 
Employee Management (CRUD)
 Add new employees
 View employee list
 Edit employee details
 Delete employees
 Data stored and fetched from MySQL database

Leave Management System
 Employees can apply for leave
 Admin can view all leave requests
 Leave status tracking
 
Attendance Management System
 Mark employees as Present or Absent
 Date-wise attendance records
 View complete attendance history 

Real-Time Data Synchronization
Frontend updates automatically after:
Add
Update
Delete
No page refresh required (Single Page Application)

REST API Integration
Backend provides REST APIs using Express
Frontend communicates using Axios
Supports:
GET
POST
PUT
DELETE operations

Database Integration (MySQL)
Structured relational database
Separate tables for:
Users
Employees
Leaves
Attendance
Ensures data consistency and reliability.


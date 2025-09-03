# csc-312-assignment-repo
Name: James Ekemini Okon

Matric number: 23/CSC/312

Course code: CSC 282

Assignment title: Student Registration System 


INSTRUCTIONS ON HOW TO SETUP AND RUN THE PROJECT 

A simple PHP web application for registering and managing student records. 
This project uses **PHP** and **XAMPP**

User Instructions

#Register a Student

1. Go to the registration page.
2. Fill in Full Name, Email, Department, Matric Number.
3. Click Submit.
4. If successful, you’ll see a confirmation message.
If an error occurs, use the Go Back link to retry.

#View Students
1. Go to view.php or click View Records.
2. A table will list all students.
   
#Delete Student
1. On view.php, click the Delete button beside a record.
2. The student will be removed.

#Notes

IDs are automatically assigned.

Each email and matric number must be unique.


## Features
- Register new students with:
  - Fullname
  - Email
  - Department
  - Matric Number
    
- Validation:
  - All fields are required
  - Email must be valid
  - Duplicate emails and matric number are not allowed
    
- View all registered students in a table
- Delete student records

## Setup Instructions (For Developers)

  Install [XAMPP](https://www.apachefriends.org/index.html).
  
  Start **Apache** and **MySQL** from the XAMPP Control Panel.
  
  Open [phpMyAdmin](http://localhost/phpmyadmin/).
  
  Create a database:
  
  sql
  
  CREATE DATABASE registration;
  
  Create a table:
  
  CREATE TABLE students (
  
  id INT AUTO_INCREMENT PRIMARY KEY,
  
  fullname VARCHAR(100) NOT NULL,
  
  email VARCHAR(100) NOT NULL UNIQUE,
  
  department VARCHAR(100) NOT NULL,
  
  matric_number VARCHAR(50) NOT NULL UNIQUE

);


Place the project files inside: C:\xampp\htdocs\php_form\

Files include:

index.php (registration form)

process.php (handles form submission)

##XAMPP DATABASE OUTPUT 
http://localhost/phpmyadmin/index.php?route=/database/structure&db=registration

view.php (view & delete records)


Open the app in your browser:

http://localhost/php_form/index.php

Student Academic Tracker

A web-based platform for tracking student performance, attendance and activities, built using SQL, HTML, CSS, PHP & JavaScript.



Overview

The Student Academic Tracker is designed for schools/colleges to manage and monitor student academic data via a simple web interface. It allows administrators, teachers, students and parents to view and manipulate data for attendance, grades, activities and classes in one place.

Features

User authentication: login/logout (Admin, Teacher, Student, Parent)

Dashboard views based on user role (Admin, Teacher, Student, Parent)

Attendance tracking & history

Grade management (adding grades, viewing student grades)

Activity / extra-curricular management

Classes and subject setup, student management

AJAX endpoints for dynamic retrieval of students, grades, attendance etc.

Responsive front-end (HTML/CSS + JavaScript)

Initial database SQL file included for setup

Tech Stack

Back-end: PHP

Front-end: HTML, CSS, JavaScript

Database: MySQL 



Optional: further improvements possible (e.g., using frameworks)

Setup & Installation

Clone the repository:

git clone https://github.com/TUSHAR-7436/STUDENT_ACADEMIC_TRACKER.git
cd STUDENT_ACADEMIC_TRACKER


Set up your web server (Apache/Nginx) with PHP and MySQL support.

Create a database (e.g., academic_tracker) in MySQL.

Import the SQL file (database.sql) to set up tables and sample data.

mysql -u username -p academic_tracker < database.sql


Edit the configuration file (config.php) to set your database host, user, password and database name.

Place the project folder in your server’s root (e.g., htdocs or www).

Open a browser and navigate to http://localhost/PROJECT_FOLDER/index.php (or your configured URL).

Login with default credentialsor create new users via admin dashboard.

Usage

Admin: manage users, classes, subjects, grades, attendance and activities.

Teacher: mark attendance, enter student grades, view class activity.

Student: view personal grades, attendance, activities.

Parent: view child’s performance.

Use the navigation bar to move between dashboards, manage modules, and view reports.

Project Structure
/
├── index.php               # Login page
├── login.php
├── logout.php
├── dashboard.php           # Generic dashboard redirect depending on role
├── admin_dashboard.php
├── teacher_dashboard.php
├── student_dashboard.php
├── parent_dashboard.php     
├── manage_users.php
├── manage_classes.php
├── manage_grades.php
├── manage_attendance.php
├── manage_activities.php
├── attendance.php
├── grades.php
├── activities.php
├── view_attendance.php
├── view_grades.php
├── view_activities.php
├── ajax_get_students_for_grades.php
├── get_attendance_records.php
├── …                       # other AJAX endpoints, scripts, utilities
├── config.php              # DB connection and settings
├── setup_db.php            # initial setup scripts
├── database.sql            # SQL for schema and sample data
├── style.css
└── scripts.js

Database Schema

The included database.sql file creates tables such as:

users (id, name, role, password_hash, …)

classes (id, class_name, …)

subjects (id, name, class_id, …)

students (id, name, class_id, user_id, …)

attendance (id, student_id, subject_id, date, status, …)

grades (id, student_id, subject_id, grade, remarks, …)

activities (id, student_id, activity_name, date, remarks, …)

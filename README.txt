SU10 Django School Management System - Full Updated Project
============================================================

This build includes:
- Star Admin dashboard
- Core layout/navbar/sidebar/footer
- Teacher CRUD: list, search, add, view, edit, delete
- Teacher submenu in sidebar
- Student, Subject, Enrollment, Attendance, Examination, Payment, Report, UserManagement app skeletons
- Fixed Student/Subject ForeignKey app references
- XAMPP MySQL/MariaDB configuration

IMPORTANT VERSION NOTE
----------------------
XAMPP in your current setup reports MariaDB 10.4.x.
Use Python 3.12 + Django 4.2 for this project.

1) Start XAMPP MySQL
--------------------
Open XAMPP Control Panel and Start MySQL.

2) Create the database
----------------------
Open http://localhost/phpmyadmin
Go to SQL and run:

CREATE DATABASE IF NOT EXISTS school_management
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;

Or import setup_xampp.sql.

3) Database settings
--------------------
SchoolManagement/settings.py is configured for the normal XAMPP defaults:
Database: school_management
User: root
Password: blank
Host: 127.0.0.1
Port: 3306

If your XAMPP root account has a password, edit PASSWORD in settings.py.

4) Create a Python 3.12 virtual environment
-------------------------------------------
From the project folder:

py -3.12 -m venv .venv
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
.\.venv\Scripts\Activate.ps1

5) Install packages
-------------------
python -m pip install --upgrade pip
pip install -r requirements.txt

6) Create tables
----------------
python manage.py check
python manage.py makemigrations
python manage.py migrate

7) Create admin account (optional)
----------------------------------
python manage.py createsuperuser

8) Run project
--------------
python manage.py runserver

Open:
http://127.0.0.1:8000/

Teacher module:
http://127.0.0.1:8000/teachers/

Django admin:
http://127.0.0.1:8000/admin/

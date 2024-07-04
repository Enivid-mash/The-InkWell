### A Blog Web Application

Welcome to the Microblog Web Application project! This project is a simple yet powerful platform for users to share their thoughts and experiences through microblogging.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Developer](#developer)
- [License](#license)

## Introduction
This microblog web application allows users to:
- Register and log in to their accounts
- Create, edit, and delete blog posts
- View blog posts written by all users

The project is developed as a full-stack application to provide hands-on experience with both front-end and back-end technologies.

## Features
- User Authentication: Register and log in to your account.
- CRUD Operations: Create, read, update, and delete blog posts.
- Responsive Design: User-friendly interface accessible on various devices.
- Secure Data Handling: Secure user data with proper encryption and secure authentication mechanisms.

## Technologies
### Primary Technologies
- **HTML**: For structuring web content.
- **CSS**: For styling web content.
- **Python**: The primary programming language.
- **Flask**: A lightweight web framework for Python.
- **MySQL**: A relational database management system.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/Enivid-mash/The-InkWell.git
    cd The-InkWell 
    ```

2. Set up a virtual environment:
    ```bash
    python3.8 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Configure the MySQL database:
    - Create a database named `your_database_name`.
    - Update the MySQL configurations in `app.py`:
        ```python
        app.config['MYSQL_HOST'] = 'localhost'
        app.config['MYSQL_USER'] = 'your_mysql_user'
        app.config['MYSQL_PASSWORD'] = 'your_mysql_password'
        app.config['MYSQL_DB'] = 'your_database_name'
        ```

5. Create the necessary tables:
    ```sql
	CREATE DATABASE <your_database_name>;
	USE <your_database_name>;
	CREATE TABLE user(user_id int auto_increment, first_name varchar(20), last_name varchar(20), username varchar(20) unique, email varchar(30) unique, password varchar(100), primary key(user_id));

	CREATE TABLE blog(blog_id int auto_increment, title varchar(100), author varchar(40), body varchar(20000), primary key(blog_id));

    CREATE TABLE subscribers (
        id INT AUTO_INCREMENT PRIMARY KEY,
        email VARCHAR(255) NOT NULL
    );
    ```

6. Run the application:
    ```bash
   	python3 main.py 
    ```

## Usage
1. Navigate to `http://127.0.0.1:5000/` in your web browser.
2. Register a new account or log in with an existing account.
3. Start creating, editing, and deleting blog posts.
4. View blog posts created by other users.
5. Subscribe to the newsletter using the email subscription form.

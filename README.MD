# Django Todo App

A simple multi-user to-do application built with Django, allowing users to manage their tasks. Users can sign up, log in, and organize their tasks with features to create, edit, delete, and mark tasks as completed. The app also includes a dark-themed UI with colored status highlighting for tasks. This project is designed to help learn and practice Django basics like models, views, templates, authentication, and working with databases.

![Python](https://img.shields.io/badge/python-3.8%2B-blue) ![Django](https://img.shields.io/badge/django-3.2%2B-green)

## Table of Contents

1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Getting Started](#getting-started)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Contributing](#contributing)

## Features

- **User Authentication**: Users can sign up, log in, and log out.
- **Task Management**: Users can create, edit, and delete tasks.
- **Task Status**: Tasks can be marked as completed or not completed.
- **Dark Theme UI**: The app features a dark theme with colored status highlights for tasks.
- **Multi-User Support**: Each user has their own task list.

## Tech Stack

- **Python 3.x**
- **Django 3.2+**
- **SQLite** (default database, can be swapped for others)
- **HTML/CSS** (with a focus on simple, modern UI design)

## Getting Started

### Prerequisites

- **Python**: Version 3.8 or higher
- **pip**: Python package installer
- **Virtual Environment**: Recommended to isolate dependencies

### Installation

Follow these steps to get the project running locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/snakyv/django-todo-app.git
   cd django-todo-app
   ```

2. **Create and activate a virtual environment** (using `venv`):
   - On macOS/Linux:
     ```bash
     python3 -m venv env
     source env/bin/activate
     ```
   - On Windows:
     ```bash
     python -m venv env
     .\env\Scripts\activate
     ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run database migrations**:
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional but recommended)**:
   This step will allow you to log in to the admin panel:
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server**:
   ```bash
   python manage.py runserver
   ```

The application will be accessible in your browser at [http://localhost:8000](http://localhost:8000).

## Usage

Once the server is running, follow these steps to use the application:

1. **Register an account** by clicking on the "Sign Up" button.
2. **Log in** to your account with the credentials you just created.
3. **Manage your tasks**:
   - Create a new task by clicking the "Add Task" button.
   - Edit an existing task by clicking on the "Edit" button next to the task.
   - Delete a task by clicking "Delete".
   - Mark tasks as "Completed" or "Incomplete" by clicking on the status checkbox.

## Project Structure

Here's a quick overview of the project structure:

```text
django-todo-app/
├─ manage.py
├─ db.sqlite3                 # created automatically after running migrations
└─ todo/
   ├─ __init__.py
   ├─ admin.py                # model registration in Django admin
   ├─ apps.py                 # app configuration
   ├─ models.py               # Todo model definition
   ├─ views.py                # request handlers (todo logic)
   ├─ urls.py                 # URL routes for the app
   ├─ settings.py             # main Django project settings
   ├─ asgi.py                 # ASGI entry point
   ├─ wsgi.py                 # WSGI entry point
   ├─ migrations/
   │   ├─ 0001_initial.py
   │   ├─ 0002_alter_todoo_srno.py
   │   ├─ 0003_alter_todoo_status.py
   │   └─ __init__.py
   ├─ static/
   │   ├─ css/
   │   │   ├─ index.css       # styles for auth pages and shared layout
   │   │   └─ styles.css      # styles for the todo list UI
   │   └─ js/
   │       └─ todo.js         # client-side logic for todo interactions
   └─ templates/
       ├─ edit_todo.html      # edit task page
       ├─ loginn.html         # login page
       ├─ signup.html         # signup page
       └─ todo.html           # main todo list page
```

## Contributing

Contributions are welcome! To contribute to the project:

1. Fork the repository.
2. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add feature/bug fix"
   ```
4. Push to your fork:
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request to the main repository.
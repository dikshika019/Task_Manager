# Task Manager

A simple **Task Management application built with Django** that allows users to manage tasks and demonstrates the core concepts of Django models, migrations, Django Admin, and ORM queries.

## 🚀 Features

* Create and manage tasks
* Store task title and description
* Mark tasks as completed or pending
* Manage tasks through Django Admin Panel
* Perform database operations using Django ORM
* Basic task filtering and querying

## 🛠️ Tech Stack

* **Python**
* **Django**
* **SQLite** (default Django database)
* **Django ORM**
* **Django Admin Panel**

## 📁 Project Structure

```text
TaskManager/
│
├── TASKMANAGER/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── Home/
│   ├── migrations/
│   ├── admin.py
│   ├── models.py
│   ├── views.py
│   └── apps.py
│
├── manage.py
└── db.sqlite3
```

## 📌 Task Model

The project contains a `Task` model with the following fields:

| Field         | Type         | Description                          |
| ------------- | ------------ | ------------------------------------ |
| `title`       | CharField    | Stores the task title                |
| `description` | TextField    | Stores task details                  |
| `completed`   | BooleanField | Stores whether the task is completed |

Example:

```python
class Task(models.Model):
    title = models.CharField(max_length=100)
    description = models.TextField()
    completed = models.BooleanField(default=False)
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd TaskManager
```

### 2. Create a virtual environment

```bash
python -m venv myenv
```

### 3. Activate the virtual environment

**Windows:**

```bash
myenv\Scripts\activate
```

**macOS/Linux:**

```bash
source myenv/bin/activate
```

### 4. Install Django

```bash
pip install django
```

### 5. Apply migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Create a superuser

```bash
python manage.py createsuperuser
```

### 7. Start the development server

```bash
python manage.py runserver
```

Open the application at:

```text
http://127.0.0.1:8000/
```

## 🔐 Django Admin Panel

To access the Django Admin Panel, open:

```text
http://127.0.0.1:8000/admin/
```

Log in using the superuser credentials.

From the Admin Panel, you can:

* Add new tasks
* View existing tasks
* Update tasks
* Delete tasks
* Mark tasks as completed or pending

## 🗄️ Django ORM Queries

The project uses Django ORM to interact with the database.

### Import the model

```python
from Home.models import Task
```

### Get all tasks

```python
Task.objects.all()
```

### Get a specific task

```python
Task.objects.get(id=1)
```

### Get completed tasks

```python
Task.objects.filter(completed=True)
```

### Get pending tasks

```python
Task.objects.filter(completed=False)
```

### Get the first task

```python
Task.objects.first()
```

### Get the last task

```python
Task.objects.last()
```

### Count all tasks

```python
Task.objects.count()
```

## 🧠 Django Concepts Practiced

This project was created to practice the following Django concepts:

* Django Project and App structure
* Django Models
* Model Fields
* Database Migrations
* `makemigrations`
* `migrate`
* Django Admin Panel
* Superuser
* Model Registration
* Django ORM
* `all()`
* `filter()`
* `get()`
* `first()`
* `last()`
* `count()`

## 🔮 Future Improvements

The project can be extended with:

* User authentication
* User-specific tasks
* Create, Read, Update, Delete (CRUD) functionality
* Task categories
* Task deadlines
* Search functionality
* REST API using Django REST Framework
* Frontend integration


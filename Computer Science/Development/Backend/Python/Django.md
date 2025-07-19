# 📝 **Django Full Beginner Notes: Setup, Structure & First App**

---

## ✅ What is Django?

**Django** is a powerful, full-stack web framework for Python. It comes with:

- ORM (Object-Relational Mapping)
    
- Built-in admin panel
    
- User authentication
    
- URL routing
    
- Templating engine (for HTML)
    
- REST support (via Django REST Framework)

---

## 🔧 Step 0: Install Django

First, install Django:

```bash
pip install django
```

To check if it worked:

```bash
django-admin --version
```

---

## ✅ Step 1: Create a Django **Project**

Run:

```bash
django-admin startproject myproject
cd myproject
```

This creates this structure:

```
myproject/
├── manage.py
└── myproject/
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

---

### 📁 What do these files do?

|File|Purpose|
|---|---|
|`manage.py`|Command-line tool to run server, create apps, manage DB|
|`myproject/`|The actual project configuration|
|`__init__.py`|Makes this folder a Python package|
|`settings.py`|Project settings (DB, apps, security, etc.)|
|`urls.py`|Main URL routing file|
|`asgi.py` / `wsgi.py`|For deployment (not important right now)|

---

## ✅ Step 2: Run the Server

```bash
python manage.py runserver
```

Go to: [http://127.0.0.1:8000](http://127.0.0.1:8000/)

You should see Django's welcome screen 🎉

---

## ✅ Step 3: Create an App

In Django, a **project** is your full site. An **app** is a component of your site (like “blog”, “users”, “orders”, etc).

Run:

```bash
python manage.py startapp users
```

Now you get:

```
users/
├── admin.py
├── apps.py
├── models.py       <-- Database models (like tables)
├── tests.py
├── views.py        <-- Request handlers (logic)
├── migrations/
└── __init__.py
```

---

### 📁 What do these app files do?

|File|Purpose|
|---|---|
|`models.py`|Define database models (tables)|
|`views.py`|Write functions that handle requests and return responses|
|`admin.py`|Customize admin panel|
|`apps.py`|App configuration|
|`migrations/`|Tracks DB changes|
|`tests.py`|Write tests (not important for now)|
|`__init__.py`|Makes it a Python package|

---

## ✅ Step 4: Register Your App

In `myproject/settings.py`, find this line:

```python
INSTALLED_APPS = [
```

Add your app `'users',` to the list:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    ...
    'users',
]
```

This tells Django your app exists and should be included in the project.

---

## ✅ Step 5: Create a Model (i.e. a Table)

Open `users/models.py`:

```python
from django.db import models

class User(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()
```

### 🔍 What’s Happening Here?

- `User` is a **model** — like a database table.
    
- `name = models.CharField(...)` means it's a string column.
    
- `age = models.IntegerField()` means it’s an integer column.


---

## ✅ Step 6: Make Migrations (DB setup)

Tell Django to detect the new model:

```bash
python manage.py makemigrations
```

Apply it to the actual DB:

```bash
python manage.py migrate
```

Now Django creates an actual table for the `User` model in your database.

(Default DB = SQLite unless you change it)

---

## ✅ Step 7: Use the Admin Panel

Create an admin user:

```bash
python manage.py createsuperuser
```

Enter username, password, email.

Then open `users/admin.py`:

```python
from django.contrib import admin
from .models import User

admin.site.register(User)
```

Now go to:

[http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)  
Login with the admin credentials, and you can **add/edit/delete users from the web UI**.

---

## ✅ Step 8: Add a Route

We'll create a simple endpoint to list all users as JSON.

### 🧩 Create `users/urls.py` (this file doesn’t exist yet):

```python
from django.urls import path
from .views import get_users

urlpatterns = [
    path("users/", get_users),
]
```

### 🔌 Plug it into main project’s `urls.py`:

Open `myproject/urls.py`:

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('users.urls')),
]
```

---

## ✅ Step 9: Add a View (Logic)

In `users/views.py`:

```python
from django.http import JsonResponse
from .models import User

def get_users(request):
    users = list(User.objects.values())  # Query all users
    return JsonResponse(users, safe=False)
```

Now when you go to [http://127.0.0.1:8000/users/](http://127.0.0.1:8000/users/), you get a list of users in JSON format.

---

## 🧠 Summary

|Feature|Django Component|
|---|---|
|Start project|`django-admin startproject`|
|Create app|`python manage.py startapp`|
|Create model|`models.py`|
|Run DB migration|`makemigrations` → `migrate`|
|Admin panel|`admin.site.register()`|
|Views (logic)|`views.py`|
|Routing|`urls.py` in project + app|
|Return JSON|`JsonResponse`|

---

## ❓ 5 Beginner Questions

1. What is the difference between a Django **project** and an **app**?
    
2. What does `models.Model` represent?
    
3. Why do we run `makemigrations` and `migrate`?
    
4. What does `JsonResponse` do?
    
5. Where do you define routes/URLs in a Django app?


---

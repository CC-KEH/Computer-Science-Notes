## 📝 **Flask – Lightweight Web Backend in Python**

**Flask** is a lightweight, minimal web framework for Python.  
Perfect for learning how backend APIs work — and building REST APIs fast.

---

### 📦 Install Flask

```bash
pip install Flask
```

---

### 📁 Folder structure (basic)

```
project/
│
├── app.py         ← your main Flask app
```

---

## 🚀 Step-by-Step Flask Basics

---

### ✅ 1. Create a basic Flask app

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, Flask!"

if __name__ == "__main__":
    app.run(debug=True)
```

#### 🔍 Explanation:

- `Flask(__name__)`: creates the Flask app
- `@app.route("/")`: maps a URL to a Python function
- `home()`: function that runs when user visits `/`
- `app.run(debug=True)`: starts the server in debug mode (auto-reloads)

---

### ✅ 2. Add More Routes (URLs)

```python
@app.route("/about")
def about():
    return "This is the about page"
```

Now:

- `/` → "Hello, Flask!"
- `/about` → "This is the about page"

---

### ✅ 3. Route with Variables

```python
@app.route("/user/<name>")
def greet_user(name):
    return f"Hello, {name}!"
```

- Visiting `/user/Alice` returns: `Hello, Alice!`

---

### ✅ 4. Return JSON (API style)

```python
from flask import jsonify

@app.route("/api/user")
def get_user():
    return jsonify({"name": "Alice", "age": 25})
```

---

### ✅ 5. Handle POST Requests (Send data to backend)

```python
from flask import request

@app.route("/api/create", methods=["POST"])
def create_user():
    data = request.json
    return jsonify({
        "message": "User created",
        "data": data
    })
```

✅ You can now send a POST request with JSON (from Postman, cURL, JS frontend, etc.)

---

### ⚙️ Summary of Flask Essentials

|Concept|Code Example|
|---|---|
|Basic route|`@app.route("/")`|
|Dynamic route|`@app.route("/user/<name>")`|
|JSON response|`jsonify({...})`|
|POST request data|`request.json`|
|Run server|`app.run(debug=True)`|

---

## ❓ 5 Questions to Test You

1. What does `@app.route("/")` do in Flask?
    - creates a landing url, and maps it to a function. 
2. How do you return JSON from a route?
    - `return jsonify({"Name": "Arbash"})`
3. What does `request.json` contain?
    - returns the json data sent through the request.
4. How do you run the Flask development server?
    - `app.run(port="8080", debug=True)`
5. What happens if you visit `/user/Bob`?
    - `@app.route("/user/<name>")`

---

## 📝 **CRUD API in Flask + MongoDB**

This is where backend magic happens: you'll build an API that can **Create, Read, Update, and Delete** users from a MongoDB collection.

---

### 📦 Requirements

```bash
pip install Flask pymongo
```

---

## ✅ Step 1: Basic Setup (`app.py`)

```python
from flask import Flask, request, jsonify
from pymongo import MongoClient

app = Flask(__name__)

# Connect to MongoDB
client = MongoClient("mongodb://localhost:27017")
db = client["mydatabase"]
users = db["users"]  # MongoDB collection
```

---

## ✅ Step 2: Create (POST)

```python
@app.route("/users", methods=["POST"])
def create_user():
    data = request.json
    result = users.insert_one(data)
    return jsonify({"message": "User created", "id": str(result.inserted_id)})
```

---

## ✅ Step 3: Read All (GET)

```python
@app.route("/users", methods=["GET"])
def get_all_users():
    user_list = []
    for user in users.find():
        user["_id"] = str(user["_id"])  # convert ObjectId to string
        user_list.append(user)
    return jsonify(user_list)
```

---

## ✅ Step 4: Read One (GET by ID)

```python
from bson import ObjectId

@app.route("/users/<id>", methods=["GET"])
def get_user(id):
    user = users.find_one({"_id": ObjectId(id)})
    if user:
        user["_id"] = str(user["_id"])
        return jsonify(user)
    return jsonify({"error": "User not found"}), 404
```

---

## ✅ Step 5: Update (PUT)

```python
@app.route("/users/<id>", methods=["PUT"])
def update_user(id):
    data = request.json
    result = users.update_one({"_id": ObjectId(id)}, {"$set": data})
    if result.modified_count:
        return jsonify({"message": "User updated"})
    return jsonify({"message": "No changes made"})
```

---

## ✅ Step 6: Delete (DELETE)

```python
@app.route("/users/<id>", methods=["DELETE"])
def delete_user(id):
    result = users.delete_one({"_id": ObjectId(id)})
    if result.deleted_count:
        return jsonify({"message": "User deleted"})
    return jsonify({"message": "User not found"})
```

---

## ✅ Step 7: Run the Server

```python
if __name__ == "__main__":
    app.run(debug=True)
```

---

## 📬 Example Requests (use Postman or curl)

- **POST** `/users`
    
    ```json
    {"name": "Alice", "age": 25}
    ```
    
- **GET** `/users`
    
- **GET** `/users/<user_id>`
    
- **PUT** `/users/<user_id>`
    
    ```json
    {"age": 30}
    ```
    
- **DELETE** `/users/<user_id>`

---

## 🧠 Summary of HTTP Methods

|Method|Action|Route|
|---|---|---|
|POST|Create|`/users`|
|GET|Read all|`/users`|
|GET|Read one|`/users/<id>`|
|PUT|Update|`/users/<id>`|
|DELETE|Delete|`/users/<id>`|

---

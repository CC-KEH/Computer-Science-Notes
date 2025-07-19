## 📝 **FastAPI – A Fast Modern Web Framework**

### 🚀 Why use FastAPI over Flask?

|Feature|Flask|FastAPI|
|---|---|---|
|Speed|Good|Blazing fast (ASGI support)|
|Type Hints|Optional|Required (built-in validation)|
|Auto Docs|❌ Manual|✅ Auto-generated (Swagger + ReDoc)|
|Async Support|Manual|Built-in `async` support|

**Note:** ASGI servers are web servers that implement the Asynchronous Server Gateway Interface (ASGI) specification

---

## 📦 Installation

```bash
pip install fastapi uvicorn
```

- `fastapi` – the framework
- `uvicorn` – the ASGI server to run the app

---

## ✅ Step 1: Basic FastAPI App

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Hello from FastAPI!"}
```

### ▶️ Run it

```bash
uvicorn app:app --reload
```

- `app:app` → file name `app.py`, object `app`
- `--reload` → auto-reloads like Flask `debug=True`

---

## ✅ Step 2: Create a GET Route

```python
@app.get("/hello/{name}")
def greet(name: str):
    return {"message": f"Hello, {name}!"}
```

- **Path parameter** with type hint `str`
- FastAPI automatically checks types!

---

## ✅ Step 3: POST Request with JSON

```python
from pydantic import BaseModel

class User(BaseModel):
    name: str
    age: int

@app.post("/users")
def create_user(user: User): # Expect a JSON payload in the request body and parse it into a `User` model."
    return {"message": "User created", "user": user}
```

- `User` is a **data model** using `pydantic`
    
- FastAPI:
    
    - Validates input (e.g. age must be int)
        
    - Converts JSON → Python model

---

## ✅ Step 4: Automatic API Docs

Visit in browser when app is running:

- **Swagger UI**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
    
- **ReDoc**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

Generated **automatically** 🎉

---

## ✅ Step 5: PUT & DELETE

```python
@app.put("/users/{user_id}")
def update_user(user_id: int, user: User):
    return {"message": f"Updated user {user_id}", "user": user}

@app.delete("/users/{user_id}")
def delete_user(user_id: int):
    return {"message": f"Deleted user {user_id}"}
```

---

## ✅ Summary

|Feature|FastAPI Code Example|
|---|---|
|GET route|`@app.get("/path")`|
|POST + JSON|`@app.post(...)`, use `BaseModel`|
|Swagger docs|Auto at `/docs`|
|Path params|`@app.get("/item/{id}")`|
|Async support|Use `async def` if you want async code|

---

## ❓ 5 Questions to Test You

1. What library does FastAPI use to validate request data?
    - `pydantic`
2. How do you define a POST endpoint that accepts JSON?
    - `@app.post("/route")`
3. Where can you see the auto-generated Swagger docs?
    - `http:localhost:8000/docs` 
4. What's the purpose of `uvicorn`?
    - Acts as an ASGI web server.
5. How is type checking enforced in FastAPI routes?
    - `pydantic BaseModel`

---

## 📝 **FastAPI + MongoDB (CRUD API)**

We’ll use `pymongo` with FastAPI to create, read, update, and delete users from a MongoDB database.

---

## 📦 Requirements

```bash
pip install fastapi pymongo uvicorn
```

> Make sure MongoDB is running locally.

---

## ✅ Step 1: Set Up the App

```python
from fastapi import FastAPI, HTTPException
from pydantic import BaseModel
from pymongo import MongoClient
from bson import ObjectId

app = FastAPI()

client = MongoClient("mongodb://localhost:27017")
db = client["mydatabase"]
collection = db["users"]
```

---

## ✅ Step 2: Define User Model

```python
class User(BaseModel):
    name: str
    age: int
```

---

## ✅ Step 3: Create User (POST)

```python
@app.post("/users")
def create_user(user: User):
    result = collection.insert_one(user.dict()) # model to dictionary => insert
    return {"message": "User created", "id": str(result.inserted_id)}
```

---

## ✅ Step 4: Get All Users (GET)

```python
@app.get("/users")
def get_users():
    users = []
    for user in collection.find():
        user["_id"] = str(user["_id"])
        users.append(user)
    return users
```

---

## ✅ Step 5: Get One User (GET by ID)

```python
@app.get("/users/{user_id}")
def get_user(user_id: str):
    user = collection.find_one({"_id": ObjectId(user_id)})
    if not user:
        raise HTTPException(status_code=404, detail="User not found")
    user["_id"] = str(user["_id"])
    return user
```

---

## ✅ Step 6: Update User (PUT)

```python
@app.put("/users/{user_id}")
def update_user(user_id: str, user: User):
    result = collection.update_one(
        {"_id": ObjectId(user_id)},
        {"$set": user.dict()}
    )
    if result.modified_count == 0:
        raise HTTPException(status_code=404, detail="User not found or not updated")
    return {"message": "User updated"}
```

---

## ✅ Step 7: Delete User (DELETE)

```python
@app.delete("/users/{user_id}")
def delete_user(user_id: str):
    result = collection.delete_one({"_id": ObjectId(user_id)})
    if result.deleted_count == 0:
        raise HTTPException(status_code=404, detail="User not found")
    return {"message": "User deleted"}
```

---

## ✅ Run the Server

```bash
uvicorn app:app --reload
```

---

## 🌐 Test Endpoints

- **POST** `/users`
    
    ```json
    { "name": "Alice", "age": 25 }
    ```
    
- **GET** `/users`
    
- **GET** `/users/<user_id>`
    
- **PUT** `/users/<user_id>`
    
- **DELETE** `/users/<user_id>`

---

## 🧠 Summary

|Operation|HTTP Method|URL|
|---|---|---|
|Create|POST|/users|
|Read All|GET|/users|
|Read One|GET|/users/{id}|
|Update|PUT|/users/{id}|
|Delete|DELETE|/users/{id}|

---

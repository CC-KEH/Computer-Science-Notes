## 📝 **MongoDB with Python using `pymongo`**

MongoDB is a **NoSQL database** — it stores data as flexible **JSON-like documents**, not rows and tables. Great for things like user profiles, logs, product catalogs, etc.

---

In Python, we use:

### 📦 Library: `pymongo`

Install it with:

```bash
pip install pymongo
```

If you're running Mongo locally, make sure MongoDB is installed and running (`mongodb://localhost:27017`).

---

## 🧱 Step 1: Connect to MongoDB

```python
from pymongo import MongoClient

client = MongoClient("mongodb://localhost:27017") # Create Connection <Client>
db = client["mydatabase"] # Accesses (or creates, if it doesn’t exist yet) a new database "mydatabase" <Database>
collection = db["users"]  # Accesses (or creates, if it doesn’t exist yet) a new collection "users" <Table>
```

---

## 📝 Step 2: Insert Data

### 🔹 Insert one document

```python
collection.insert_one({"name": "Alice", "age": 24})
```

### 🔹 Insert multiple documents

```python
collection.insert_many([
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 22}
])
```

---

## 🔍 Step 3: Query Documents

### 🔹 Get all documents

```python
for doc in collection.find():
    print(doc)
```

### 🔹 Find one document

```python
user = collection.find_one({"name": "Alice"})
print(user)
```

### 🔹 Find multiple documents

```python
users = collection.find({"age": {"$gt": 20}})
for user in users:
    print(user)
```

---

## ✏️ Step 4: Update Documents

### 🔹 Update one

```python
collection.update_one(
    {"name": "Alice"},             # Filter (which document to update)
    {"$set": {"age": 25}}          # Update operation (what to change)
)
```

### 🔹 Update many

```python
collection.update_many(
    {"age": {"$lt": 25}},          # Filter: age less than 25
    {"$set": {"young": True}}      # Add or update the "young" field to True
)
```

---

## ❌ Step 5: Delete Documents

### 🔹 Delete one

```python
collection.delete_one({"name": "Bob"})
```

### 🔹 Delete many

```python
collection.delete_many({"age": {"$lt": 18}})
```

---

## ⚡ Step 6: Query Filters

MongoDB uses a different syntax for conditions:

|SQL Equivalent|MongoDB Filter|
|---|---|
|`WHERE age = 20`|`{"age": 20}`|
|`WHERE age > 20`|`{"age": {"$gt": 20}}`|
|`WHERE age <= 20`|`{"age": {"$lte": 20}}`|
|`WHERE name LIKE 'A%'`|`{"name": {"$regex": "^A"}}`|

---

## 🧠 Summary: SQL vs MongoDB Terms

|SQL Term|MongoDB Equivalent|
|---|---|
|Table|Collection|
|Row|Document|
|Column|Field|
|Primary Key|`_id`|
|`SELECT`|`find()`|
|`INSERT`|`insert_one()`|
|`UPDATE`|`update_one()`|
|`DELETE`|`delete_one()`|

---

## ❓ 5 Questions to Test You

1. What is the MongoDB equivalent of a SQL "table"?
    - `collection`
2. Write a Python line to insert `{"name": "Dave", "age": 32}` into MongoDB.
    - `cursor.insert_one({"name": "Dave" , "age" : 32})`
3. How would you find all users with age greater than 25?
    - `cursor.find({age: {"$gt": 25}})`
4. What does `update_many()` do and when would you use it?
    - update many is used for updating multiple docs.
5. How would you delete all documents where age is less than 18?
    - `cursor.delete_many({"age": {"$lt": 18}})`

---

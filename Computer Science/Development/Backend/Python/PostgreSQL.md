## **PostgreSQL with Python using `psycopg2`**

PostgreSQL is a powerful, open-source relational database used in serious web apps (e.g. Django, Flask, FastAPI projects).

---

To use it with Python, we use:

### 📦 Library: `psycopg2`

- A PostgreSQL driver for Python
- Requires manual installation:

```bash
pip install psycopg2-binary
```

---

### 🧱 Step 1: Connect to PostgreSQL

```python
import psycopg2

conn = psycopg2.connect(
    dbname="your_db",
    user="your_user",
    password="your_password",
    host="localhost",
    port="5432"
)
cursor = conn.cursor()
```

- Replace `your_db`, `your_user`, etc. with real PostgreSQL credentials.

---

### 🏗️ Step 2: Create a Table

```python
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
    id SERIAL PRIMARY KEY,
    name TEXT NOT NULL,
    age INTEGER
)
""")
conn.commit()
```

- `SERIAL`: Auto-incrementing ID (like `AUTOINCREMENT` in SQLite)

---

### 📝 Step 3: Insert Data (Use `%s` for placeholders)

```python
cursor.execute("INSERT INTO users (name, age) VALUES (%s, %s)", ("Alice", 24))
conn.commit()
```

---

### 🔍 Step 4: Query Data

```python
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()
for row in rows:
    print(row)
```

---

### ✏️ Step 5: Update & Delete

```python
# Update
cursor.execute("UPDATE users SET age = %s WHERE name = %s", (25, "Alice"))

# Delete
cursor.execute("DELETE FROM users WHERE name = %s", ("Alice",))

conn.commit()
```

---

### 🔁 Step 6: Bulk Insert with `executemany()`

```python
data = [("Tom", 22), ("Jerry", 19), ("Spike", 28)]
cursor.executemany("INSERT INTO users (name, age) VALUES (%s, %s)", data)
conn.commit()
```

---

### 🛑 Step 7: Close the Cursor and Connection

```python
cursor.close()
conn.close()
```

---

### 🧠 psycopg2 Key Differences from SQLite

|Feature|sqlite3|psycopg2|
|---|---|---|
|Param style|`?`|`%s`|
|Auto-increment|`AUTOINCREMENT`|`SERIAL`|
|Database file|`.db` file|External server|
|Installation needed?|❌ built-in|✅ yes (`pip`)|

---

## ❓ 5 Questions to Test You

1. What function is used to connect to a PostgreSQL database in Python?
    - `psycopg2.connect()`
2. What placeholder symbol does `psycopg2` use in SQL statements?
    - `%s`
3. Write a Python line to insert `("Bob", 30)` into the `users` table.
    - `cursor.execute("INSERT INTO USERS VALUES (%s)", ("Bob", 30))`
4. How do you bulk insert rows in psycopg2?
    - `cursor.executemany("INSERT INTO USERS VALUES (%s)", data)`
5. What does `conn.commit()` do and why is it needed?
	- Finalizes the transaction permanently.
---

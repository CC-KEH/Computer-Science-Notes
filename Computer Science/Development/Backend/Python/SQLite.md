## **SQLite in Python (Complete Guide)**

SQLite is a lightweight, file-based SQL database engine that comes **built into Python**, making it perfect for learning and small projects.

---

### 🔧 Step 1: Import & Connect to the Database

```python
import sqlite3

# Create a new database file or connect to existing
conn = sqlite3.connect("mydata.db")
```

---

### 📌 Step 2: Create a Cursor Object

```python
cursor = conn.cursor()
```

- The **cursor** is your tool for executing SQL statements.

---

### 🏗️ Step 3: Create a Table

```python
cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    age INTEGER
)
""")
conn.commit()
```

- `AUTOINCREMENT`: Auto-generates the ID
- `NOT NULL`: Ensures `name` is not empty
- `commit()`: Saves the changes

---

### 📝 Step 4: Insert Data

```python
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 24))
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Bob", 30))
conn.commit()
```

- Use **parameterized queries (`?`)** to prevent SQL injection
- `conn.commit()` saves changes

---

### 🚀 Step 5: Querying Data

#### ✅ `fetchall()`: Get all rows

```python
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()
for row in rows:
    print(row)
```

#### ✅ `fetchone()`: Get the first row

```python
cursor.execute("SELECT * FROM users")
row = cursor.fetchone()
print(row)
```

#### ✅ `fetchmany(n)`: Get the next `n` rows

```python
cursor.execute("SELECT * FROM users")
rows = cursor.fetchmany(2)
print(rows)
```

---

### ✏️ Step 6: Update Data

```python
cursor.execute("UPDATE users SET age = ? WHERE name = ?", (25, "Alice"))
conn.commit()
```

---

### ❌ Step 7: Delete Data

```python
cursor.execute("DELETE FROM users WHERE name = ?", ("Bob",))
conn.commit()
```

---

### 🔁 Step 8: Bulk Insertion Using `executemany()`

```python
data = [("Tom", 22), ("Jerry", 19), ("Spike", 28)]
cursor.executemany("INSERT INTO users (name, age) VALUES (?, ?)", data)
conn.commit()
```

---

### 🛑 Step 9: Close the Cursor and Connection

```python
cursor.close()
conn.close()
```

- Always clean up when done

---

### 📄 Bonus: Rollback Example

```python
try:
    cursor.execute("DELETE FROM users WHERE age < 20")
    raise Exception("Oops, fake error!")
    conn.commit()
except:
    conn.rollback()  # undo delete if something goes wrong
```

---

## 🧠 Summary Table

|Function|Purpose|
|---|---|
|`connect()`|Open/create a DB|
|`cursor()`|Create a cursor object|
|`execute()`|Run SQL command|
|`executemany()`|Run SQL command with multiple sets of data|
|`fetchone()`|Get one result row|
|`fetchmany(n)`|Get next `n` result rows|
|`fetchall()`|Get all result rows|
|`commit()`|Save changes|
|`rollback()`|Undo uncommitted changes|
|`close()`|Close connection or cursor|

---

## ❓ 5 Questions to Test You

1. What’s the difference between `fetchone()` and `fetchmany()`?
	- fetchone() retrieves the next row from a query result, while fetchmany(size) retrieves the specified number of rows. 
2. Why should you use parameterized queries instead of f-strings in SQL?
	- Parameterized queries prevent SQL injection by safely handling user input, unlike f-strings which can expose vulnerabilities.
3. How do you insert multiple rows in one go using Python?
	- Use executemany() with a list of tuples to insert multiple rows efficiently in one query.
	- `data = [('Alice', 25),('Bob', 30),('Charlie', 35)]`
	- `cursor.executemany('INSERT INTO users (name, age) VALUES (?, ?)', data)`
4. What happens if you don’t call `commit()` after an `INSERT`?
	- Without commit(), changes from an INSERT are not saved to the database and may be lost. 
5. What does `rollback()` do and when might you use it?
	- rollback() discards changes made in a transaction; use it to undo operations after an error.

---

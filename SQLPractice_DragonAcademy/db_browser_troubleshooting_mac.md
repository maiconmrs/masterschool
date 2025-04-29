
# 🛠 Quick Troubleshooting Guide for DB Browser for SQLite on MacBook

---

## Problem 1: Can't Open the App (Security Warning)

**Symptom:**  
- You double-click DB Browser but macOS blocks it with a message like: "App cannot be opened because it is from an unidentified developer."

**Solution:**
1. Open **System Preferences**.
2. Go to **Security & Privacy**.
3. In the **General** tab, you will see an option to **"Open Anyway"** next to the app name.
4. Click **Open Anyway**.
5. Confirm by clicking **Open** when prompted.

✅ You should now be able to open DB Browser normally.

---

## Problem 2: "Execute SQL" Tab Doesn't Show Results

**Symptom:**  
- You write SQL queries, click "Execute All", but don't see results below.

**Solution:**
- Make sure you are running a **SELECT** statement if you expect results.
- Some actions like **INSERT**, **UPDATE**, or **DELETE** don't produce visible results — they just modify data silently.
- After modifying, use a **SELECT** query to check your table.

✅ Remember: SELECT shows results, others modify data.

---

## Problem 3: Changes Are Lost After Closing the App

**Symptom:**  
- You add or edit data, but when you reopen the database, changes are missing.

**Solution:**
- Always click the **"Write Changes"** button (the blue floppy disk icon 💾) after modifying data.
- If you don't, your modifications stay only in memory and are discarded when you exit.

✅ Make it a habit to save regularly!

---

## Problem 4: Foreign Key Constraints Not Working

**Symptom:**  
- You create tables with foreign keys, but inserting wrong data doesn't trigger any error.

**Solution:**
- In DB Browser, foreign key enforcement is **off by default**.
- To enable it:
  1. Click on **Execute SQL**.
  2. Run this command first:  
     ```sql
     PRAGMA foreign_keys = ON;
     ```
  3. Then continue working normally.

✅ This will enforce foreign key rules properly.

---

## Problem 5: SQL Syntax Errors

**Symptom:**  
- Error messages appear when trying to run SQL queries.

**Solution:**
- Double-check every keyword (e.g., `CREATE TABLE`, `INSERT INTO`).
- Make sure columns are separated by commas.
- Pay attention to parentheses and quotation marks.

✅ Always re-read your query carefully!

---

## Problem 6: No Table Selected in "Browse Data"

**Symptom:**  
- "No data" shows in the "Browse Data" tab even after inserting.

**Solution:**
- Go to the **table selector dropdown** at the top left of the "Browse Data" tab.
- Select the correct table (e.g., Dragons, Training_Records, etc.).

✅ Then you will see the correct data.

---

## Problem 7: Unexpected NULL Values

**Symptom:**  
- You insert a new record, but some columns show `NULL`.

**Solution:**
- Double-check your `INSERT INTO` query.
- Make sure you insert values for all **NOT NULL** columns.
- If you don't insert a value for a normal column, NULL will appear by default (it's normal unless restricted).

✅ It's okay if not every column is filled, unless required.

---

## Problem 8: Wrong Database Opened

**Symptom:**  
- You don't see your table or data anymore.

**Solution:**
- Double-check the database file you're working on (e.g., `dragons.db`, `project.db`).
- Use **File > Open Database** to load the correct `.db` file.

✅ Always check the database name in the top window title!

---

# 🎯 Final Tip
If anything feels stuck:
- Try closing and reopening DB Browser.
- Make sure you saved the database properly before running new commands.

---

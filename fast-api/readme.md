# 🚀 FastAPI Beginner Guide: Build Your First API

<div align="center">
  <img src="https://fastapi.tiangolo.com/img/logo-margin/logo-teal.png" alt="FastAPI" width="600"/>
</div>

---

If you’re just starting with FastAPI or backend development, this guide is for you.

Let’s create a simple and functional API using FastAPI — step by step. You’ll learn how to set up your project, create routes, and run your first server. 💻

---

## ✅ Step 1: Set Up the Project

Open your terminal and run:

```bash
mkdir my-fastapi-app
cd my-fastapi-app
```

✅ Step 2: Create a Virtual Environment
A virtual environment keeps your project’s dependencies isolated.

For Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
``` 

For macOS/Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

Once activated, your terminal prompt will show something like:

```bash
(.venv) C:\Users\YourName\fastapi-app>
```

✅ Step 3: Install FastAPI and Tools
Use uv or pip to install FastAPI and its required components:

```bash
uv pip install "fastapi[all]"
```

This installs:

fastapi – The web framework

uvicorn – The server to run your app

httpx – (Optional) Tool for testing APIs

✅ Step 4: Create Your First API File
Create a new file named main.py and paste this code:

```bash
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def home():
    return {"message": "Hello, World"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str | None = None):
    return {"item_id": item_id, "query": q}
🧠 What’s Happening Here:
FastAPI() creates the app instance

@app.get("/") is a route that returns a welcome message

/items/{item_id} accepts a path and optional query parameter
```

✅ Step 5: Run Your Server
You have two options to start your server:

Option 1 (Recommended):

```bash
fastapi dev main.py
```

Option 2 (Using Uvicorn):

```bash
uvicorn main:app --reload
```

--reload means the server restarts automatically when you make changes.

✅ Step 6: Test Your API in the Browser
Now open these URLs:

http://localhost:8000 → {"message": "Hello, World"}

http://localhost:8000/items/5?q=hello → See item and query

http://localhost:8000/docs → Interactive Swagger API Docs

📁 Folder Structure
After setup, your folder should look like this:

```bash
fastapi-app/
├── main.py
├── .venv/
└── pyproject.toml
``` 

🎉 What You’ve Built
A FastAPI app that handles GET requests

Dynamic routing with query parameters

Auto-generated Swagger documentation

🔜 What’s Next?
In the next article, we’ll cover how to:

Add POST, PUT, and DELETE routes

Build request models using Pydantic

Connect to a real database

If this helped you, share it with others learning FastAPI. Let’s build cool stuff together! 💡


---

## 📖 Read More on Medium

[👉 Click here to read the full article on Medium](https://medium.com/@zainabmustaqeem123/fastapi-beginner-guide-build-your-first-api-f91823cad26d)

---

*Written by: Faria Mustaqim*  
*Currently learning at: Governor Sindh Initiative for Artificial Intelligence (GIAIC)*  
*Exploring the world of Generative AI*
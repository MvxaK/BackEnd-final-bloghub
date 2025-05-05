# 📝 Blog Management Web App (Flask)

## 1. Introduction and Objectives
This Flask web application is a blogging platform with authentication, user profile management (including avatar uploads), and CRUD operations for blog posts. It uses SQLAlchemy for the database, JWT for session handling, and a clean structure for user and post management.

---

## 2. Description of Features

- 🔐 User registration & login with JWT cookies  
- 📝 Create, read, update, delete (CRUD) blog posts  
- 🧑 User profile editing with avatar upload  
- 🖼️ Image upload (avatars stored in `static/uploads/avatars`)  
- 🧠 Password hashing using `werkzeug.security`  
- 🔒 Access control using `@jwt_required`  
- 💾 SQLite database backend  
- 🧱 Structured with SQLAlchemy models  

---
## 3. ER Diagram (Inferred)
(user,post)
(id from user_id)
username,id
email,title
password,content
avatar,created_at

---

## 4. Code Structure (OOP & Modules)

Although Blueprints are not used, the project is well-structured:

- SQLAlchemy class-based models  
- Modular function definitions for routes  
- JWT session management  
- Secure password handling via hashing  

### 🗂 Directory Tree
Exam5/
├── app.py
├── requirements.txt
├── static/uploads/avatars/ ← image uploads
├── templates/ ← HTML templates
└── blog.db ← SQLite database


---

## 5. Key Pages (Screenshots Placeholder)

Key HTML templates:

- `index.html` – Homepage/dashboard  
- `login.html` / `register.html` – Authentication  
- `create_post.html` / `edit_post.html` – Post creation/editing  
- `profile.html` / `edit_profile.html` – User profile  
- `moderate_comments.html` – Comment moderation  
- `view_post.html` – Post detail view  

---

## 6. Challenges Faced and Solutions

| Challenge                         | Solution                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| User session security            | Implemented JWT in cookies with expiration and secret key                |
| File upload safety               | Used `secure_filename` and validated file extensions                     |
| Password storage                 | Applied `werkzeug.security` for password hashing and validation          |
| Access control for posts/profile| Used `@jwt_required` decorators and user ID checks                       |
| No Blueprints used               | Modular logic and route handling for separation of concerns              |

---

## 📦 RequirementsRe

Install packages using:

```bash
pip install -r requirements.txt


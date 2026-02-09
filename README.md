# 📚 Library Management System (Java Servlet + Tomcat)

A simple Library Management web application built using **Java Servlets, JSP/HTML, JDBC, and Apache Tomcat**.  
This project demonstrates basic CRUD-style operations, MVC layering, and session handling in a Java web environment.

---

## 🚀 Features

- ➕ Add new book details
- 👤 Store author information
- 💾 JDBC database connectivity
- 🧠 DAO + Service layer architecture
- 🌐 Servlet-based request handling
- 📄 HTML pages for UI
- 🔄 Session-based data sharing
- ⚙️ Runs on Apache Tomcat 10 (Jakarta Servlet)

---

## 🏗️ Project Structure

```
src/main/java/com/kce/book/
│
├── bean/
│   ├── BookBean.java
│   └── AuthorBean.java
│
├── DAO/
│   ├── BookDAO.java
│   └── AuthorDAO.java
│
├── services/
│   └── Administrator.java
│
├── servlet/
│   ├── MainServlet.java
│   └── ViewServlet.java
│
└── util/
    └── DBUtil.java

webapp/
├── AddBook.html
├── Menu.html
├── ViewBook.html
├── Failure.html
└── Invalid.html
```

---

## 🛠️ Tech Stack

- Java 11+ / 16
- Jakarta Servlet API
- JDBC
- Apache Tomcat 10
- HTML
- Eclipse IDE
- MySQL / Oracle (depending on DBUtil config)

---

## ⚙️ Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/LibraryManagement.git
```

---

### 2️⃣ Download Tomcat 10.0.x

Download from Apache archive:

- Choose **Tomcat 10.0.x (zip)**
- Extract to:
```
C:\Tomcat10
```

---

### 3️⃣ Configure in Eclipse

```
Servers → New Server → Tomcat v10.0
→ Select Tomcat folder
→ Add project
```

---

### 4️⃣ Update Servlet Imports (Important)

Tomcat 10 requires **Jakarta** packages:

```java
import jakarta.servlet.*;
import jakarta.servlet.http.*;
```

---

### 5️⃣ Configure Database

Update DB connection details inside:

```
util/DBUtil.java
```

Example:

```java
url = jdbc:mysql://localhost:3306/library
username = root
password = root
```

---

### 6️⃣ Run Project

```
Right click project → Run on Server
```

Open browser:

```
http://localhost:8080/LibraryManagement/AddBook.html
```

---

## 🔄 Application Flow

```
AddBook.html
   ↓
MainServlet
   ↓
Service Layer
   ↓
DAO Layer
   ↓
Database

Menu.html → ViewServlet → Display Book
```

---

## 📸 Sample Pages

- Add Book Page
- Menu Page
- View Book Details Page
- Error / Invalid Input Pages

---

## 🧠 Concepts Demonstrated

- MVC Architecture
- Servlet Lifecycle
- Session Management
- DAO Pattern
- Layered Design
- Form Handling
- Redirect vs Forward
- JDBC Integration

---

## ⚠️ Common Issues

**Tomcat startup error**
→ Ensure Tomcat version matches Eclipse server adapter

**Servlet not found**
→ Check `@WebServlet` mapping

**ClassNotFoundException**
→ Verify Tomcat installation path

---

## 👨‍💻 Author

Developed as a Java Web Technology learning project.

---

## 📜 License

Free to use for learning and academic purposes.

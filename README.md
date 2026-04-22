# 🚀 Online Exam System (Evalix)

<p align="center">
<img src="https://img.shields.io/badge/Java-17-blue?style=for-the-badge&logo=java&logoColor=white" alt="Java 17">
<img src="https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot 3.x">
<img src="https://img.shields.io/badge/JPA%20%2F%20Hibernate-red?style=for-the-badge" alt="JPA / Hibernate">
<img src="https://img.shields.io/badge/H2%20Database-lightgrey?style=for-the-badge" alt="H2 Database">
</p>

- A comprehensive **Online Examination System** built using **Spring Boot, Spring Security, Thymeleaf, Bootstrap 5**, and **JPA/Hibernate**.  
- The platform provides a secure and user-friendly environment for **Admins** and **Students** to manage and take online tests effectively.

---

# ✨ Features

## 👨‍💻 Admin Features
- Secure Admin Login
- Stats Dashboard (Total Students, Exams, Questions, Submissions)
- **Exam CRUD** (title, duration, description)
- **Question CRUD** per exam
- Cascade deletes for exams → questions → results
- Protect answered questions from accidental delete
- Manage Students
- Reset Student Password
- Delete Student Account (cascade all related data)
- View all submissions for any exam

---

## 🧑‍🎓 Student Features
- Student Registration (Full Name, Email, Mobile, Profile Picture)
- Secure Login
- Dashboard with KPIs + Performance Chart
- Take Exam (paginated interface + question palette)
- Live Timer (auto submit)
- Instant Results (score, percentage, pass/fail)
- Detailed Review Page (correct vs incorrect answers)
- Profile Update
- Upload New Profile Picture
- Change Password
- View All Previous Exam Results

---

# 🛠️ Tech Stack

| Layer | Technology                                 |
|------|--------------------------------------------|
| Backend | Spring Boot 3, Spring Security 6           |
| Frontend | Thymeleaf, Html, Bootstrap 5, Chart.js     |
| Database | H2 (file-based) (configurable to other DB) |
| ORM | Hibernate / JPA                            |
| Build | Maven                                      |
| Storage | Local File System for images               |

---

# 📁 Project Structure

```
project-root/
│── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/yourpackage/
│   │   │       ├── controller/        # Handles user requests
│   │   │       ├── service/           # Business logic layer
│   │   │       ├── dao/               # Database operations
│   │   │       ├── model/             # Entity/POJO classes
│   │   │       └── util/              # Utility classes (DB connection, helpers)
│   │   └── resources/
│   │       ├── application.properties
│   │       └── config files
│
│── lib/                              # External libraries (if any)
│── screenshots/                      # Application screenshots
│── database/
│   └── schema.sql                    # Database script
│
│── README.md
│── pom.xml / build.gradle            # Build configuration
│── .gitignore

```

---

# 🖥️ Screenshots

<h2 align="center">🔐 System Pages</h2>

#### 👤 Dashbord

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230733" src="https://github.com/user-attachments/assets/df90b4ec-bb24-456e-a649-a774e3122ea1" />
<br><br>

#### 🔑 Login Page

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230804" src="https://github.com/user-attachments/assets/59b5af43-10a7-4fa2-a221-fb794f149283" />
<br><br>

---

<h2 align="center">🎓 Student Pages</h2>

#### 📊 Student Dashboard

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230848" src="https://github.com/user-attachments/assets/7742e3ce-54ce-4a5a-b810-e86ceb0e6ece" />
<br><br>

#### 👤 Profile Settings

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230935" src="https://github.com/user-attachments/assets/3b77b48d-06f8-4162-bdbe-3ac1fde041aa" />

<br><br>

#### 📜 Exam History

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230916" src="https://github.com/user-attachments/assets/cc533cca-a6ce-4b8c-b5d5-5db89306b687" />
<br><br>

#### 📝 Create Student Account

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230756" src="https://github.com/user-attachments/assets/25afd216-210e-4840-b767-b8c2c7cb5c76" />
<br><br>

---

<h2 align="center">👤 Admin Pages</h2>

#### 📊 Admin Dashboard

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230812" src="https://github.com/user-attachments/assets/dc6dc894-1184-4151-b324-9b918527c6ff" />
<br><br>

#### ⚙️ Manage Exams

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230821" src="https://github.com/user-attachments/assets/0256bae6-c2e5-4310-99dc-f05ff8f2b22c" />
<br><br>

#### ➕ Create New Exam

<img width="1600" height="900" alt="WhatsApp Image 2026-04-21 at 1 28 52 AM" src="https://github.com/user-attachments/assets/5ab5adcc-f14b-46fa-bee5-1ed6b0437b05" />
<br><br>

#### 👥 Manage Students

<img width="1920" height="1080" alt="Screenshot 2026-04-21 230826" src="https://github.com/user-attachments/assets/f590640b-59df-49e6-8b42-c1adbe7035d6" />
<br><br>

---

# 🚀 How to Run the Project

### ✔️ Prerequisites
- Java **17+**
- Maven
- Any IDE (IntelliJ, VS Code, Eclipse)

---

### ✔️ Clone the Repository

```bash
git clone https://github.com/tushar-patil-1109/Assessly.git
cd Assessly
```

---

### ✔️ Start the Application

Open the project → Run:

`OnlineExamApplication.java`

Server will start at:

👉 http://localhost:7890

---

# 🗄️ Database (H2)

Access H2 Console:

👉 http://localhost:7890/h2-console

```
JDBC URL : jdbc:h2:file:./data/examdb  
Username : sa  
Password : password
```

---

# 🔐 Default Admin User

| Username | Password |
|---------|----------|
| admin | adminpass |

---

# 🔮 Future Enhancements

- JWT Authentication (Stateless Security)
- REST API for React frontend
- Microservices architecture
- Redis caching
- Docker deployment
- AI-based performance analysis

---

# 👨‍💻 Author :- Tushar Patil 

<a href="https://wa.me/+91 8378990863">
<img src="https://img.shields.io/badge/WhatsApp-Chat%20Now-green?style=for-the-badge&logo=whatsapp" >
</a>

- 🎓 Computer Engineering Graduate
- 💻 Java | Spring Boot | SQL | DSA


---

# ❤️ Final Note

This project is built to showcase industry-level backend development skills and can be extended into a full-scale SaaS exam platform.

---

<p align="center">
<strong>Happy Coding ❤️</strong>
</p>

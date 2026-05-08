<div align="center">

<img src="https://img.shields.io/badge/STATUS-OPERATIONAL-8ab452?style=for-the-badge&labelColor=0a0e12" alt="Status"/>
<img src="https://img.shields.io/badge/SECURITY-VERIFIED-8ab452?style=for-the-badge&labelColor=0a0e12" alt="Security"/>
<img src="https://img.shields.io/badge/VERSION-2.0-8ab452?style=for-the-badge&labelColor=0a0e12" alt="Version"/>

<h1>◆ CR ELECTION SYSTEM ◆</h1>

### DIGITAL DEMOCRACY PROTOCOL

*A modern web-based Class Representative Election Platform designed to digitize and secure the democratic process in educational institutions.*

**Developed by Mannat Mishra**

</div>

---

## 📋 Table of Contents

1. [Problem Statement](#problem-statement)
2. [Solution Overview](#solution-overview)
3. [Tech Stack](#tech-stack)
4. [Features](#features)
5. [System Architecture](#system-architecture)
6. [Quick Start](#quick-start)
7. [Database Configuration](#database-configuration)
8. [Running the Application](#running-the-application)
9. [System Workflow](#system-workflow)
10. [Troubleshooting](#troubleshooting)

---

## 🎯 Problem Statement

Traditional paper-based CR elections in educational institutions suffer from:

- **No privacy** — students can see each other's votes
- **Human counting errors** — manual tallying is inaccurate and slow
- **Low participation** — physical presence required at fixed times
- **No audit trail** — impossible to verify results after the fact
- **Resource wastage** — paper, printing, and manual effort
- **Possibility of bias** — counting team may be questioned for partiality

This project replaces the entire process with a secure, automated, and transparent digital platform.

---

## 💡 Solution Overview

The **CR Election System** addresses all the above problems by providing:

- Secure SIC-based student authentication with one vote per student
- Real-time automated vote counting with instant result generation
- Section-wise, branch-wise, and year-wise candidate filtering
- Admin dashboard for complete election management
- CGPA-based candidate eligibility verification via ERP integration
- Bulk student import via Excel
- Mobile-friendly responsive interface

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript |
| **Backend** | JSP (Java Server Pages), Apache Tomcat |
| **Microservice** | Flask (Python) |
| **Database** | MySQL |
| **Libraries** | Apache POI, JDBC, JSON Java |
| **CGPA Integration** | Selenium, PDFPlumber, WebDriver Manager |

---

## ✨ Features

### Student Features
- SIC-based secure authentication
- One-time vote enforcement
- Candidate browsing filtered by branch, section, and year
- Candidate manifesto viewing before voting
- Mobile-responsive voting interface

### Admin Features
- Bulk student import via Excel (.xlsx / .xls / .csv)
- Add and delete candidates with CGPA verification
- Real-time vote analytics and result dashboard
- Year-end student promotion system
- Election reset and selective data deletion

### Security Features
- Duplicate vote prevention
- Protected admin login
- SQL-safe parameterized queries
- Session handling and logout

---

## 🏗️ System Architecture

```
Presentation Layer
(HTML + CSS + JavaScript)
        ↓
Application Layer
(JSP on Apache Tomcat + Flask Microservice)
        ↓
Database Layer
(MySQL)
```

---

## 🤸 Quick Start

### Prerequisites

Make sure you have the following installed:

- [Java JDK 8+](https://www.oracle.com/java/technologies/downloads/)
- [Apache Tomcat 9.0](https://tomcat.apache.org/)
- [MySQL 8.0](https://dev.mysql.com/downloads/)
- [Python 3.8+](https://www.python.org/) (for CGPA microservice)
- [Git](https://git-scm.com/)

### Clone the Repository

```bash
git clone https://github.com/mannatgit22/cr-election-system.git
cd cr-election-system
```

---

## 🗄️ Database Configuration

```sql
mysql -u root -p
CREATE DATABASE cr_election_db;
USE cr_election_db;
SOURCE full_database_setup.sql;
exit;
```

Update the JDBC connection in your JSP files:

```java
String url = "jdbc:mysql://localhost:3306/cr_election_db";
String user = "your_mysql_username";
String password = "your_mysql_password";
```

---

## ▶️ Running the Application

### Step 1 — Deploy to Tomcat

Copy the project folder into Tomcat's webapps directory:

```bash
# Windows
xcopy /E /I /Y "." "C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps\CR_Election"
```

### Step 2 — Start MySQL

```bash
# Windows
net start MySQL80
```

### Step 3 — Start Tomcat

```bash
cd "C:\Program Files\Apache Software Foundation\Tomcat 9.0\bin"
startup.bat
```

### Step 4 — Start Flask Microservice (CGPA verification)

```bash
cd "Download or View CGPA"
python -m venv venv
venv\Scripts\activate
pip install flask selenium webdriver-manager python-dotenv pdfplumber
python app.py
```

### Step 5 — Open in Browser

```
http://localhost:8080/CR_Election/index.html
```

---

## 🔄 System Workflow

```
Student visits platform
        ↓
Authenticates with SIC number
        ↓
Views candidates filtered by section/branch/year
        ↓
Reads manifestos and casts vote
        ↓
Vote recorded → student marked as voted
        ↓
Admin views real-time results and declares winner
```

---

## 🛠️ Troubleshooting

| Issue | Fix |
|-------|-----|
| Page not loading | Ensure Tomcat is running and you're on the correct port (8080) |
| Database connection error | Verify MySQL is running and credentials in JSP are correct |
| CGPA verification fails | Check Flask microservice is running on its port |
| Excel import fails | Ensure column headers match exactly and file is .xlsx/.xls/.csv |
| Can't login as admin | Check admin credentials in the database |

---

## 📜 License

This project is developed for educational purposes.

---

<div align="center">

**Made for Digital Democracy**

[⬆ Back to Top](#-cr-election-system-)

</div># CR_ELECTION

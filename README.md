# 🗳️ Online Voting System

### A Java-Based Web Application for Digital Voting

A web-based voting application developed using **Java, Spring MVC, Hibernate, JSP, and MySQL**. This project demonstrates a basic digital voting workflow, including user registration, authentication, candidate management, vote submission, and result visualization.

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/Spring%20MVC-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring MVC"/>
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="Hibernate"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/JSP-FF6F00?style=for-the-badge" alt="JSP"/>
</p>

> [!IMPORTANT]
> **Educational Use Only:** This project is intended for learning and demonstration. It has not been independently audited or secured for real elections. Do not use it to collect real votes or sensitive personal information.

---

## 📌 Table of Contents

- [✨ Features](#-features)
- [🛠️ Technology Stack](#️-technology-stack)
- [📂 Project Structure](#-project-structure)
- [⚙️ Prerequisites](#️-prerequisites)
- [🚀 Installation and Setup](#-installation-and-setup)
- [🔐 Demo Data and Security](#-demo-data-and-security)
- [⚠️ Limitations](#️-limitations-and-future-improvements)
- [📄 License](#-license)
- [📬 Contact](#-contact)

---

## ✨ Features

### 👤 Voter Module
- User registration and login
- Session-based authentication
- Candidate listing and selection
- Vote submission workflow
- Vote status tracking to help prevent repeat voting
- View election results and candidate vote totals

### 🛡️ Admin Module
- Separate administrator interface
- Add and delete candidates
- Manage the candidate list
- View voting results

### ⚙️ Application Features
- MVC architecture using Spring MVC
- Hibernate ORM for database operations
- MySQL database persistence
- JSP-based dynamic user interfaces
- CSS styling for page presentation
- Maven-based build and WAR deployment

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Java | Core programming language |
| Spring MVC 5 | Web MVC framework |
| Hibernate 5 | Object-relational mapping |
| JSP & JSTL | Dynamic web pages |
| HTML5 & CSS3 | Frontend presentation |
| MySQL | Relational database |
| Apache Maven | Dependency management and build |
| Apache Tomcat 9 | Application deployment |

---

## 📂 Project Structure

```text
OnlineVotingSystem/
├── pom.xml
└── src/
    └── main/
        ├── java/com/
        │   ├── config/       # Startup data seeding
        │   ├── controller/   # MVC controllers
        │   ├── dao/          # Data access layer
        │   ├── model/        # Hibernate entities
        │   └── service/      # Application logic
        ├── resources/        # Configuration resources
        └── webapp/
            ├── resources/    # CSS and static assets
            ├── WEB-INF/
            │   └── view/     # JSP views
            └── index.jsp
```

---

## ⚙️ Prerequisites

Ensure the following software is installed:

- **JDK:** Java 11 or a version compatible with the project configuration
- **Apache Maven:** For building the project
- **MySQL Server:** For database storage
- **Apache Tomcat 9:** For deployment
- **IDE:** Eclipse or another Java-compatible IDE (optional)

---

## 🚀 Installation and Setup

### 1. Clone the Repository

Replace `YOUR_USERNAME` with your actual GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/OnlineVotingSystem.git
cd OnlineVotingSystem
```

### 2. Create the Database

Open MySQL and execute:

```sql
CREATE DATABASE online_voting;
```

### 3. Configure Database Connectivity

Update the database URL, username, password, and Hibernate properties in your project's existing Spring/Hibernate configuration.

Example database URL:

```text
jdbc:mysql://localhost:3306/online_voting
```

**Security tip:** Never upload real database credentials to GitHub. Keep sensitive configuration in environment variables or a local configuration file excluded from version control.

### 4. Build the Project

Run the following command from the project root:

```bash
mvn clean package
```

After a successful build, Maven should generate the WAR file in the `target/` directory.

### 5. Deploy on Apache Tomcat

Copy the generated WAR file into Tomcat's `webapps/` directory and start the server.

Open the application in your browser:

```text
http://localhost:8080/OnlineVotingSystem/
```

The exact URL and WAR filename depend on your project configuration and deployment settings.

---

## 🔐 Demo Data and Security

The project contains startup data seeding for an administrator account and sample candidates. The seeded administrator credentials are defined in `com.config.DataSeeder`.

Before running the application:

- Check the configured demo username and password.
- Remove or change default credentials.
- Never publish working administrator credentials.
- Do not deploy the current implementation publicly.

The current implementation stores passwords as plain strings. This is **not secure for production use**. Use a suitable password-hashing algorithm and strengthen authentication and authorization before considering any real-world deployment.

---

## ⚠️ Limitations and Future Improvements

This is an educational project, not an election-grade voting platform.

Potential improvements include:

- Secure password hashing and credential management
- CSRF protection and stronger session management
- Server-side validation and role-based authorization
- Transaction-safe vote recording and duplicate-vote prevention
- Better error handling and automated testing
- Audit logging and privacy protections
- Secure deployment and database-secret management
- Independent security testing

These are recommendations for future work, not claims that the current application already implements them.

---

## 📄 License

**Copyright © 2026 Chetan Dhawas. All Rights Reserved.**

This repository is provided for viewing and educational demonstration. No permission is granted to copy, modify, redistribute, publish, or commercially use the project without obtaining prior written authorization from the copyright holder, except where permitted by applicable law.

For permission to use any part of this code, contact the copyright holder before use.

See the [`LICENSE`](LICENSE) file for the full terms.

---

## 📬 Contact

**Chetan Dhawas**  
*Java Full Stack Developer | Computer Engineering Student*

- 💻 **GitHub:** [chetandhawas9](https://github.com/chetandhawas9)
- 💼 **LinkedIn:** [chetan-dhawas](https://linkedin.com/in/chetan-dhawas)
- 📧 **Email:** chetandhawas9@gmail.com
For project-related questions, collaboration proposals, or permission to use this source code, please contact me through the details above.

---

<p align="center">
  <b>Developed with ☕ Java by Chetan Dhawas</b>
  <br/>
  <i>Learn • Build • Improve</i>
</p>

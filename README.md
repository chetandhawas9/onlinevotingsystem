# Online Voting System

An educational web-based voting application built with Java, Spring MVC, Hibernate, JSP, and MySQL. The project demonstrates a basic online voting workflow with user registration and login, candidate management, vote submission, and result viewing.

> **Important:** This project is intended for learning and demonstration only. It has not been reviewed or hardened for real elections or other high-stakes voting. Do not use it to collect real votes or sensitive personal information.

## Features

- User registration and login
- Session-based user authentication
- Separate admin and voter views
- Candidate listing and voting
- Vote status tracking to help prevent repeat voting
- Results page showing candidate vote totals
- Admin functions to add and delete candidates
- MySQL persistence through Hibernate ORM
- JSP views styled with CSS

## Technology Stack

- **Language:** Java
- **Web framework:** Spring MVC 5
- **ORM:** Hibernate 5
- **View layer:** JSP, JSTL, HTML, CSS
- **Database:** MySQL
- **Build tool:** Maven
- **Deployment:** WAR application on a compatible servlet container, such as Apache Tomcat 9

## Project Structure

```text
OnlineVotingSystem/
├── pom.xml
└── src/
    └── main/
        ├── java/com/
        │   ├── config/       # Startup data seeding
        │   ├── controller/   # MVC controllers
        │   ├── dao/          # Data access
        │   ├── model/        # Hibernate entities
        │   └── service/      # Application logic
        ├── resources/
        └── webapp/
            ├── resources/    # CSS and other static assets
            ├── WEB-INF/
            │   └── view/     # JSP pages
            └── index.jsp
```

## Prerequisites

- JDK 11 or a compatible JDK
- Apache Maven
- MySQL Server
- Apache Tomcat 9 or another compatible `javax.servlet` container
- Eclipse IDE or another Java IDE (optional)

## Setup and Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/OnlineVotingSystem.git
   cd OnlineVotingSystem
   ```

2. **Create a MySQL database**

   Create a database for the application, for example:
   ```sql
   CREATE DATABASE online_voting;
   ```

3. **Configure the database connection**

   Update the database URL, username, password, and Hibernate settings in the project's Spring/Hibernate configuration. Do not commit real database credentials to GitHub. Use environment variables or a local, ignored configuration file where practical.

4. **Build the WAR**
   ```bash
   mvn clean package
   ```

5. **Deploy to Tomcat**

   Copy `target/OnlineVotingSystem.war` into Tomcat's `webapps` directory, start Tomcat, and open:
   ```text
   http://localhost:8080/OnlineVotingSystem/
   ```

   The exact URL may vary depending on your Tomcat context path and deployment configuration.

## Default Demo Data

The current source includes startup seeding for an administrator account and sample candidates. The seeded administrator credentials are defined in `com.config.DataSeeder`.

**Security warning:** The current implementation seeds a known username and password, and the user model stores the password as a plain string. Change/remove demo credentials and implement secure password hashing before any deployment beyond a local demonstration. Never expose this application publicly in its current state.

## Current Limitations and Security Notes

This is a student/learning project, not an election-grade system. Before any real-world use, it would need, at minimum:

- Secure password hashing and credential management
- CSRF protection and stronger authentication/session controls
- Server-side validation and authorization checks on every sensitive operation
- Transaction-safe vote recording and robust duplicate-vote prevention
- Auditability, privacy protections, testing, and independent security review
- Deployment hardening and protection of database secrets

## Contributing

Suggestions and improvements are welcome. For substantial changes, open an issue first to discuss what you would like to change.

## License

This project is distributed under the MIT License. See the [`LICENSE`](LICENSE) file. Use this license only if you own the project code or have permission to license all included material.

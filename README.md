<div align="center">

# 💬 YapSpace
### *Where Thoughts, Threads, and Vibes Converge — Built from Scratch in Java*

[![Java](https://img.shields.io/badge/Java-OOP%20%26%20Web%20Server-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](#)
[![MySQL](https://img.shields.io/badge/MySQL-Connector%2FJ%2026.10.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](#)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Project-OOP%20Showcase-FF6B6B?style=for-the-badge)](#)

> *"A space to yap, share feelings, spark conversations, and react—engineered with clean Object-Oriented architecture from data models to web routes."*

[🚀 Quick Start](#-quick-start) • [🧱 OOP Blueprint](#-object-oriented-programming-oop-in-yapspace) • [🗺️ Project Map](#️-project-structure) • [👥 Team](#-meet-the-yapspace-crew)

</div>

---

## ✨ What is YapSpace?

**YapSpace** is a Java-powered social and discussion platform where users can register, log in, express **feelings** and **categories**, publish **posts**, exchange **comments**, and drop **reactions**. It combines a custom Java web server layer, service and repository classes, and MySQL persistence (`schema.sql` and `mysql-connector-j-26.10.0.jar`) alongside storage/TSV helpers, a console demo, test runners, and Docker support[cite: 1].

<details>
<summary><b>⚡ Interactive Feature Highlights (Click to Expand)</b></summary>

* **User Accounts & Roles:** Supports `RegularUser` and `AdminUser` (`Role`), paired with password hashing (`PasswordHasher`), input validation (`Validator`), and session management (`Session`, `SessionManager`)
* **Posts, Feelings & Reactions:** Connects `Post`, `Category`, `Feeling`, `Comment`, and `Reaction` (`ReactionType`) into an interactive discussion flow
* **Layered Architecture:** Separates concerns across `model`, `repository`, `service`, `web`, `storage`, and `exception` packages
* **Flexible Execution & Testing:** Ready to run via `Main.java`, `ConsoleDemo.java`, `start-yapspace.bat`, `Dockerfile`, and test scripts (`TestDatabase.java`, `TestUserLogin.java`, `TestUserRegistration.java`, `TestUserRepository.java`, `TestPostRepository.java`)[cite: 1]

</details>

---

## 🗺️ Architecture & Project Structure

```text
YapSpace-main/
├── 🐳 Dockerfile & start-yapspace.bat     # Container & quick-launch scripts
├── 🗄️ database/schema.sql               # MySQL database schema
├── 📦 lib/mysql-connector-j-26.10.0.jar # JDBC driver
├── 🖼️ diagram (1).png                   # System / class / flow diagram
└── src/
    ├── 🧪 Test*.java                    # Database, auth & repository test drivers
    ├── database/DatabaseConnection.java # JDBC connection handling
    └── yapspace/
        ├── Main.java & ConsoleDemo.java # App & console entry points
        ├── model/                     # Core domain entities, enums & roles
        ├── repository/                # Data access (User, Post, Comment, Reaction)
        ├── service/                   # Business logic, validation & hashing
        ├── web/                       # WebServer, Router, Controllers, Views & Assets
        ├── storage/                   # DataStore & TSV persistence helpers
        └── exception/                 # Custom domain exceptions
```

<details>
<summary><b>🔍 Explore Every Package at a Glance (Click to Expand)</b></summary>

| Package / Path | Key Files | Role in YapSpace |
| :--- | :--- | :--- |
| `yapspace.model` | `BaseEntity`, `User`, `RegularUser`, `AdminUser`, `Role`, `Post`, `Comment`, `Reaction`, `ReactionType`, `Category`, `Feeling` | Core domain models representing users, roles, posts, comments, reactions, categories, and feelings |
| `yapspace.repository` | `UserRepository`, `PostRepository`, `CommentRepository`, `ReactionRepository` | Data access layer managing persistence and retrieval for entities |
| `yapspace.service` | `UserService`, `PostService`, `Validator`, `PasswordHasher` | Business logic, validation rules, and credential security |
| `yapspace.web` | `WebServer`, `Router`, `Handler`, `WebRequest`, `WebResponse`, `AuthController`, `PostController`, `Session`, `SessionManager`, `Views`, `Html`, `Assets` | HTTP server, request routing, controllers, session handling, HTML rendering, and assets |
| `yapspace.storage` | `DataStore`, `Tsv` | Local storage and TSV serialization utilities |
| `yapspace.exception` | `YapException`, `AuthenticationException`, `ValidationException`, `PermissionException`, `NotFoundException` | Domain-specific exception hierarchy for clear error handling |
| `database` & `lib` | `schema.sql`, `DatabaseConnection.java`, `mysql-connector-j-26.10.0.jar` | Database schema definition and MySQL JDBC connectivity[cite: 1]

</details>

---

## 🧱 Object-Oriented Programming (OOP) in YapSpace

Here is how the four core pillars of **Object-Oriented Programming**—alongside custom exceptions and clean layering—are applied across **YapSpace**:

### 1. Encapsulation 🔒
* **Where:** Domain models (`BaseEntity`, `User`, `RegularUser`, `AdminUser`, `Post`, `Comment`, `Reaction`, `Category`, `Feeling`), security/validation utilities (`PasswordHasher`, `Validator`), and web/session classes (`Session`, `SessionManager`, `WebRequest`, `WebResponse`)[cite: 1].
* **How we applied it:** Internal state and sensitive operations—such as entity fields, active user sessions, password hashing (`PasswordHasher`), and input validation (`Validator`)—are encapsulated within dedicated classes and accessed through controlled methods and service boundaries rather than exposed directly[cite: 1].

### 2. Inheritance 🧬
* **Where:** `BaseEntity` $\rightarrow$ domain entities (`User`, `Post`, `Comment`, etc.), `User` $\rightarrow$ `RegularUser` and `AdminUser` (paired with `Role`), and `YapException` $\rightarrow$ `AuthenticationException`, `ValidationException`, `PermissionException`, and `NotFoundException`[cite: 1].
* **How we applied it:**
  * `BaseEntity` centralizes shared base properties for entities so subclasses don't duplicate common fields
  * `RegularUser` and `AdminUser` extend `User` to specialize account types and role-based capabilities while inheriting core user attributes
  * Specific exception classes extend `YapException` so distinct error scenarios share a common parent type while remaining clearly identifiable[cite: 1]

### 3. Polymorphism 🎭
* **Where:** `Handler` and `Router` in `yapspace.web`, user role specialization (`User`, `RegularUser`, `AdminUser`, `Role`), and service/repository interactions[cite: 1].
* **How we applied it:** `Router` dispatches incoming web requests through `Handler` implementations uniformly, allowing different routes and behaviors to be executed through a shared contract without tightly coupling routing logic to every individual endpoint[cite: 1].

### 4. Abstraction 🧩
* **Where:** `Handler`, `BaseEntity`, `YapException`, web controllers (`AuthController`, `PostController`), services (`UserService`, `PostService`), repositories (`UserRepository`, `PostRepository`, `CommentRepository`, `ReactionRepository`), storage (`DataStore`, `Tsv`), and `DatabaseConnection`[cite: 1].
* **How we applied it:** High-level components like `AuthController` and `PostController` interact with services and repositories without needing to manage raw SQL statements, connection details, password hashing mechanics, or low-level storage formats directly[cite: 1].

<details>
<summary><b>💡 Architecture & OOP Takeaways (Click to Expand)</b></summary>

* **Custom Exception Hierarchy (`YapException`):** `AuthenticationException`, `ValidationException`, `PermissionException`, and `NotFoundException` give meaningful, structured error signals across authentication, validation, access control, and lookup flows
* **Separation of Concerns (`Controller` $\rightarrow$ `Service` $\rightarrow$ `Repository`):** Keeps HTTP routing/views, business rules/validation, and data persistence modular and easy to maintain[cite: 1]

</details>

---

## 🚀 Quick Start

<details>
<summary><b>Option A: Run Locally (Java + MySQL / Batch Script)</b></summary>

1. **Prepare the Database:** Import `database/schema.sql` into MySQL and update `src/database/DatabaseConnection.java` with your database credentials (`lib/mysql-connector-j-26.10.0.jar` is included in `lib/`)
2. **Start the Application:** Run `start-yapspace.bat` from the project root
3. **Compile & Run Entry Points or Tests:** Compile `src/` with `lib/mysql-connector-j-26.10.0.jar` in the classpath and run `yapspace.Main`, `yapspace.ConsoleDemo`, or any test runner (`TestDatabase`, `TestUserRegistration`, `TestUserLogin`, `TestUserRepository`, `TestPostRepository`)[cite: 1]

</details>

<details>
<summary><b>Option B: Run with Docker 🐳</b></summary>

```bash
docker build -t yapspace .
docker run -p 8080:8080 yapspace
```

*(Adjust the host port mapping if your `WebServer` uses a different port[cite: 1].)*

</details>

---

## 👥 Meet the YapSpace Crew

| Member | Role | Key Contributions |
| :--- | :--- | :--- |
| **Doliente, Ronabel E.** | **Team Leader** | Led team coordination, project planning, and milestone tracking |
| **Ebora, Rodalyn R.** | **Lead Programmer** | Engineered core Java OOP architecture, services, repositories, and backend logic |
| **Panganiban, Kristelle Mhae B.** | **UI Designer** | Crafted user interface layouts, views, and visual styling |

---

## 🙏 Acknowledgements

We sincerely thank our professor, **Ms. Fatima Marie Agdon**, for her guidance, mentorship, and instruction in Object-Oriented Programming throughout the development of **YapSpace**.

---

<div align="center">
  <sub>Built with ☕, Java, and plenty of yapping by <b>YapSpace</b>.</sub>
</div>

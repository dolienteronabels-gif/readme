<div align="center">

<br>

# ✦ 𝐘𝐚𝐩𝐒𝐩𝐚𝐜𝐞 ✦
### *⚡ Where Thoughts Turn Into Threads, Feelings Into Vibes, and Java Into a Living Community ⚡*

<br>

[![Java](https://img.shields.io/badge/☕_Java-OOP_%26_Custom_HTTP_Server-FF5E5B?style=for-the-badge)](#)
[![MySQL](https://img.shields.io/badge/🗄️_MySQL-Connector%2FJ_26.10.0-00BBF9?style=for-the-badge)](#)
[![Docker](https://img.shields.io/badge/🐳_Docker-Container_Ready-00F5D4?style=for-the-badge&labelColor=111827)](#)
[![OOP](https://img.shields.io/badge/🧱_OOP-Encapsulation_·_Inheritance_·_Polymorphism_·_Abstraction-9B5DE5?style=for-the-badge)](#)

<br>

> *"Not just another app—it's a digital hangout where every **feeling** has a voice, every **post** sparks a thread, every **reaction** speaks volumes, and every **class** has a purpose."*

<br>

**[ ✨ Overview](#-what-makes-yapspace-tick)** • **[ 🖼️ Visual Tour](#-visual-tour)** • **[ 🖥️ Live Console Preview](#-sample-output)** • **[ 🧠 OOP Craft](#-how-we-wove-oop-into-yapspace)** • **[ 🗂️ Codebase Map](#-codebase-blueprint)** • **[ 🚀 Launchpad](#-quick-start)** • **[ 💖 Crew & Thanks](#-meet-the-yapspace-crew)**

<br>

</div>

---

## ✨ What Makes YapSpace Tick?

**YapSpace** is a full-stack Java social hangout crafted from the ground up so people can sign up, log in, pick their current **feeling** and **category**, start **yapping** in posts, chime in through **comments**, and express instant **reactions**[cite: 1]. Under the hood, it brings together a custom Java web server (`WebServer`, `Router`, `AuthController`, `PostController`, `Views`, `Html`, `Assets`), clean `Service` and `Repository` layers, `DataStore` and `Tsv` storage utilities, MySQL persistence (`schema.sql` + `mysql-connector-j-26.10.0.jar`), a console demo, test suites, and Docker deployment[cite: 1].

<details>
<summary><b>🎛️ Tap to Unfold — Core Capabilities & Playable Modes</b></summary>

<br>

* **Identity, Roles & Sessions:** Distinguish `RegularUser` and `AdminUser` (`Role`), protect credentials with `PasswordHasher`, guard inputs with `Validator`, and track active users via `Session` and `SessionManager`
* **Expressive Social Loop:** Connect `Post`, `Category`, `Feeling`, `Comment`, and `Reaction` (`ReactionType`) for lively community interactions
* **Multi-Layer Java Architecture:** Cleanly separated `model`, `repository`, `service`, `web`, `storage`, and `exception` packages plus JDBC database connectivity (`DatabaseConnection`)
* **Run It Your Way:** Launch via `start-yapspace.bat`, `Main.java`, `ConsoleDemo.java`, or `Dockerfile`, and verify components using `TestDatabase`, `TestUserRegistration`, `TestUserLogin`, `TestUserRepository`, and `TestPostRepository`[cite: 1]

</details>

---

## 🖼️ Visual Tour

> *Four snapshots from the YapSpace experience—from first impression to posting your next big thought.*[cite: 2]

| 🌅 Landing Page | 🔐 Login Page |
| :---: | :---: |
| <kbd>![Landing Page](screenshots/landing-page.png)</kbd> | <kbd>![Login Page](screenshots/login-page.png)</kbd> |
| **First Look & Welcome Gateway** | **Account Sign-In & Session Entry** |

| 💬 Community Feed | ✍️ Create Post |
| :---: | :---: |
| <kbd>![Community Feed](screenshots/community-feed.png)</kbd> | <kbd>![Create Post](screenshots/create-post.png)</kbd> |
| **Threads, Feelings, Comments & Reactions** | **Crafting & Publishing New Yaps** |

<details>
<summary><b>🔍 Zoom Mode — Open Full-Width Gallery</b></summary>

<br>

### 🌅 Landing Page
<kbd>![Landing Page](screenshots/landing-page.png)</kbd>

### 🔐 Login Page
<kbd>![Login Page](screenshots/login-page.png)</kbd>

### 💬 Community Feed
<kbd>![Community Feed](screenshots/community-feed.png)</kbd>

### ✍️ Create Post
<kbd>![Create Post](screenshots/create-post.png)</kbd>[cite: 2]

</details>

---

## 🖥️ Sample Output

<details>
<summary><b>⚡ Click to Inspect — Sample Startup & Feed Activity Output</b></summary>

<br>

```text
╔══════════════════════════════════════════════════════════════╗
║                 💬 YAPSPACE ENGINE ONLINE                    ║
╚══════════════════════════════════════════════════════════════╝
  [DB]      MySQL connection pool ready (schema verified)
  [SESSION] SessionManager initialized & active
  [ROUTER]  Routes bound -> /, /login, /register, /feed, /post/new
  [HTTP]    YapSpace WebServer listening and ready for requests!

┌──────────────────────────────────────────────────────────────┐
│  📌 SAMPLE THREAD PREVIEW                                    │
│  Author   : @ronabel  [RegularUser]                          │
│  Category : Campus Life   |   Feeling : 😄 Hyped             │
│  Post     : "Our OOP classes finally connected cleanly!"     │
│  Stats    : 💬 2 Comments   |   🔥 6 Reactions               │
└──────────────────────────────────────────────────────────────┘
```

*(Swap in your live terminal output anytime from `ConsoleDemo`, `Main`, or your `Test*.java` runs[cite: 1].)*

</details>

---

## 🧠 How We Wove OOP Into YapSpace

Rather than dumping everything into a single script, we structured **YapSpace** around Object-Oriented principles so every class has a clear identity, responsibility, and relationship[cite: 1].

### 🔒 Encapsulation — *Protecting State & Sensitive Logic*
* **Where we applied it:** Domain models (`BaseEntity`, `User`, `RegularUser`, `AdminUser`, `Post`, `Comment`, `Reaction`, `Category`, `Feeling`), security & validation classes (`PasswordHasher`, `Validator`), and web/session components (`Session`, `SessionManager`, `WebRequest`, `WebResponse`)
* **How we applied it:** We keep internal fields, session states, hashing routines, and validation checks tucked inside their respective classes and service boundaries instead of exposing raw internals—so `PasswordHasher` handles password hashing, `Validator` enforces input rules, and models/sessions guard their own state safely[cite: 1]

### 🧬 Inheritance — *Sharing Foundations & Specializing Types*
* **Where we applied it:**
  * `BaseEntity` $\longrightarrow$ core domain entities (`User`, `Post`, `Comment`, etc.)
  * `User` $\longrightarrow$ `RegularUser` and `AdminUser` (working alongside `Role`)
  * `YapException` $\longrightarrow$ `AuthenticationException`, `ValidationException`, `PermissionException`, and `NotFoundException`
* **How we applied it:** `BaseEntity` holds shared entity traits to avoid repetitive boilerplate, `RegularUser` and `AdminUser` build specialized user types on top of `User`, and our custom exception subclasses extend `YapException` so specific errors carry clear meaning while sharing a unified base exception type[cite: 1]

### 🎭 Polymorphism — *One Contract, Many Behaviors*
* **Where we applied it:** `Handler` and `Router` inside `yapspace.web`, user role handling (`User`, `RegularUser`, `AdminUser`, `Role`), and interactions across services and repositories
* **How we applied it:** `Router` routes incoming requests through `Handler` implementations uniformly, letting distinct route handlers run through a common contract without hardcoding every endpoint's behavior directly inside the router[cite: 1]

### 🧩 Abstraction — *Hiding Complexity Behind Clean Layers*
* **Where we applied it:** `Handler`, `BaseEntity`, `YapException`, web controllers (`AuthController`, `PostController`), business services (`UserService`, `PostService`), data repositories (`UserRepository`, `PostRepository`, `CommentRepository`, `ReactionRepository`), storage utilities (`DataStore`, `Tsv`), and `DatabaseConnection`
* **How we applied it:** `AuthController` and `PostController` orchestrate user actions and posts through services and repositories without getting tangled in raw SQL queries, connection setup, hashing internals, or file/TSV storage mechanics[cite: 1]

<details>
<summary><b>🎯 Bonus Design Highlights — Custom Exceptions & Layered Flow</b></summary>

<br>

* **Meaningful Error Types:** `AuthenticationException`, `ValidationException`, `PermissionException`, and `NotFoundException` make failures predictable and descriptive instead of relying on generic errors
* **Clean Flow (`Web / Controller` $\rightarrow$ `Service` $\rightarrow$ `Repository` $\rightarrow$ `Database / Storage`):** Keeps HTTP handling, business logic, and persistence cleanly decoupled and easier to maintain[cite: 1]

</details>

---

## 🗂️ Codebase Blueprint

```text
YapSpace-main/
├── 📸 screenshots/                      # Landing, login, feed & create-post images
├── 🐳 Dockerfile & start-yapspace.bat     # Container build & one-click Windows start
├── 🗄️ database/schema.sql               # Relational MySQL schema
├── 📦 lib/mysql-connector-j-26.10.0.jar # MySQL JDBC driver
├── 🖼️ diagram (1).png                   # Visual architecture / flow diagram
└── src/
    ├── 🧪 Test*.java                    # DB, registration, login & repo test runners
    ├── database/DatabaseConnection.java # JDBC connection provider
    └── yapspace/
        ├── Main.java & ConsoleDemo.java # Main & console entry points
        ├── model/                     # Entities, enums & user roles
        ├── repository/                # Data access repositories
        ├── service/                   # Validation, hashing & business logic
        ├── web/                       # Server, router, controllers, views & assets
        ├── storage/                   # DataStore & TSV utilities
        └── exception/                 # Custom exception hierarchy
```[cite: 1, 2]

<details>
<summary><b>📂 Click to Inspect Every Package & Key File</b></summary>

<br>

| Package / Folder | Files Included | Purpose |
| :--- | :--- | :--- |
| `yapspace.model` | `BaseEntity`, `User`, `RegularUser`, `AdminUser`, `Role`, `Post`, `Comment`, `Reaction`, `ReactionType`, `Category`, `Feeling` | Models users, privileges, posts, comments, reactions, categories, and feelings |
| `yapspace.repository` | `UserRepository`, `PostRepository`, `CommentRepository`, `ReactionRepository` | Handles storing and fetching entities |
| `yapspace.service` | `UserService`, `PostService`, `Validator`, `PasswordHasher` | Applies business logic, checks inputs, and hashes passwords |
| `yapspace.web` | `WebServer`, `Router`, `Handler`, `WebRequest`, `WebResponse`, `AuthController`, `PostController`, `Session`, `SessionManager`, `Views`, `Html`, `Assets` | Runs the web server, routes requests, manages sessions, and renders views/assets |
| `yapspace.storage` | `DataStore`, `Tsv` | Provides local data store and TSV serialization support |
| `yapspace.exception` | `YapException`, `AuthenticationException`, `ValidationException`, `PermissionException`, `NotFoundException` | Defines custom domain exceptions |
| `database` & `lib` | `schema.sql`, `DatabaseConnection.java`, `mysql-connector-j-26.10.0.jar` | Sets up tables and connects Java to MySQL[cite: 1]

</details>

---

## 🚀 Launchpad

<details>
<summary><b>💻 Run Locally (MySQL + Java / start-yapspace.bat)</b></summary>

<br>

1. **Load the Schema:** Run `database/schema.sql` in MySQL and configure your credentials in `src/database/DatabaseConnection.java` (`lib/mysql-connector-j-26.10.0.jar` is ready in `lib/`)
2. **Start YapSpace:** Execute `start-yapspace.bat` from the project root
3. **Compile & Run Entry Points or Tests:** Compile `src/` with `lib/mysql-connector-j-26.10.0.jar` on the classpath and run `yapspace.Main`, `yapspace.ConsoleDemo`, or any test class (`TestDatabase`, `TestUserRegistration`, `TestUserLogin`, `TestUserRepository`, `TestPostRepository`)[cite: 1]

</details>

<details>
<summary><b>🐳 Run With Docker</b></summary>

<br>

```bash
docker build -t yapspace .
docker run -p 8080:8080 yapspace
```

*(Update the exposed port if your `WebServer` listens on a different port[cite: 1].)*

</details>

---

## 💖 Meet the YapSpace Crew

<div align="center">

| ✨ Member | 🎖️ Role |
| :--- | :--- |
| **Doliente, Ronabel E.** | **Team Leader** |
| **Ebora, Rodalyn R.** | **Lead Programmer** |
| **Panganiban, Kristelle Mhae B.** | **UI Designer** |

</div>

---

## 🙏 Acknowledgements

> *"Great projects aren't built by code alone—they're built by grace, guidance, patience, and people who care."*

* **✨ To God Almighty:** Above all, we offer our deepest thanks to God for His continuous guidance, strength, and grace, and for blessing us with wisdom, clarity, and knowledge throughout every stage of creating **YapSpace**.
* **💐 To Our Professor, Ms. Fatima Marie Agdon:** From the bottom of our hearts, thank you, Ma'am **Fatima Marie Agdon**, for your patience, dedication, and inspiring lessons in Object-Oriented Programming. Your encouragement kept us going through tough bugs and helped us appreciate clean, thoughtful code. The warmth and care you bring to your teaching truly stay with us.
* **🤝 To Our YapSpace Co-Crew:** Building **YapSpace** together meant late nights, shared laughs, tricky bugs, and big smiles whenever something finally worked. Thank you for having each other's backs, staying patient, and turning an idea into a project we can all look back on with pride—this repo holds a piece of all of us.

---

<div align="center">
  <br>
  <b>💬 YapSpace</b> • <i>Crafted with ☕, Java OOP, and heart.</i>
  <br><br>
</div>


<!-- ========== ANIMATED HEADER ========== -->

<p align="center">
  <img
    src="assets/yapspace-animated-banner.gif"
    alt="YapSpace Animated Banner"
    width="100%"
  />
</p>

<h1 align="center">YapSpace</h1>

<p align="center">
  <strong>Your thoughts have a place here.</strong>
  <br />
  Share a little. Connect a lot.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Project-YapSpace-1e293b?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Language-Java-orange?style=for-the-badge&logo=java" />
  <img src="https://img.shields.io/badge/Status-Academic%20Project-bb6b4b?style=for-the-badge" />
</p>

---

<!-- ========== CLICKABLE NAVIGATION ========== -->

<p align="center">
  <a href="#-about-yapspace">About</a> •
  <a href="#-features">Features</a> •
  <a href="#-screenshots">Screenshots</a> •
  <a href="#-object-oriented-programming">OOP Concepts</a> •
  <a href="#-technologies-used">Technologies</a> •
  <a href="#-meet-the-team">Team</a>
</p>

---

## 💬 About YapSpace

YapSpace is a community-based social platform where users can share their thoughts, express themselves, and connect with others.

Designed with a clean and welcoming interface, YapSpace gives every user a space to speak, share, and interact.

> Every thought deserves a place. Every voice deserves to be heard.

## ✨ Features

- 👤 **User Registration** – Create an account.
- 🔐 **User Login** – Access your account securely.
- 🏠 **Community Feed** – Explore posts shared by users.
- ✍️ **Create a Post** – Share your thoughts with the community.
- 📝 **Manage Posts** – Edit or delete your own posts.
- 💭 **Comments** – Interact with shared posts.
- ❤️ **Reactions** – Support, Relate, and Encourage posts.
- 📂 **My Posts** – View your own published posts.
- 🚪 **Logout** – End your current session.

## 📸 Screenshots

<details>
<summary>🏠 View Landing Page</summary>

<p align="center">
  <img src="screenshots/landing-page.png" alt="YapSpace Landing Page" width="90%" />
</p>
</details>

<details>
<summary>🔐 View Login Page</summary>

<p align="center">
  <img src="screenshots/login-page.png" alt="YapSpace Login Page" width="90%" />
</p>
</details>

<details>
<summary>💬 View Community Feed</summary>

<p align="center">
  <img src="screenshots/community-feed.png" alt="YapSpace Community Feed" width="90%" />
</p>
</details>

<details>
<summary>✍️ View Create a Post Page</summary>

<p align="center">
  <img src="screenshots/create-post.png" alt="YapSpace Create a Post Page" width="90%" />
</p>
</details>

## 🧠 Object-Oriented Programming

YapSpace applies the four fundamental principles of Object-Oriented Programming.

<details>
<summary>1. 🔒 Encapsulation</summary>

Encapsulation keeps data and the methods that work with it together inside a class. It also helps control access to an object's data.

**Application in YapSpace:** User and post-related data are organized within their respective classes.
</details>

<details>
<summary>2. 🧬 Inheritance</summary>

Inheritance allows one class to acquire properties and methods from another class.

**Application in YapSpace:** Related classes can reuse shared properties and behaviors through inheritance where implemented.
</details>

<details>
<summary>3. 🔄 Polymorphism</summary>

Polymorphism allows the same method or operation to behave differently depending on the object using it.

**Application in YapSpace:** Different objects can provide their own implementations of shared behaviors where applicable.
</details>

<details>
<summary>4. 🎭 Abstraction</summary>

Abstraction hides unnecessary implementation details and presents only the essential functionality.

**Application in YapSpace:** The application organizes its internal operations into components so users can interact with features without needing to understand their internal code.
</details>

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java | Main programming language |
| HTML | Web page structure |
| CSS | Interface styling |
| TSV Files | Local data storage |
| Git and GitHub | Version control and collaboration |
| Visual Studio Code | Development environment |

## 🚀 How to Run

**1. Clone the repository**

```bash
git clone https://github.com/dolienteronabels-gif/YapSpace.git
```

**2. Open the project folder**

```bash
cd YapSpace
```

**3. Compile the Java files (PowerShell)**

```powershell
New-Item -ItemType Directory -Force out
$files = Get-ChildItem -Recurse src -Filter *.java | ForEach-Object { $_.FullName }
javac -cp "lib\mysql-connector-j-26.10.0.jar" -d out $files
```

**4. Run the application**

```powershell
java -cp "out;lib\mysql-connector-j-26.10.0.jar" yapspace.Main
```

**5. Open YapSpace in your browser**

```text
http://localhost:8080
```

## 👥 Meet the Team

**Team 4 — Ro Ro Row Your Code**

| Member | Role |
|---|---|
| Doliente, Ronabel E. | Team Leader |
| Ebora, Rodalyn R. | Lead Programmer |
| Panganiban, Kristelle Mhae B. | UI Designer |

**Institution:** Batangas State University – Alangilan Campus  
**Course:** Bachelor of Science in Information Technology  
**Instructor:** Ms. Fatima Marie P. Agdon

## 🙌 Acknowledgment

This project is presented to our instructor as part of our academic requirements. We sincerely appreciate the guidance, knowledge, and support that helped us develop YapSpace.

---

<p align="center">
  <strong>YapSpace</strong>
  <br />
  Your thoughts have a place here.
  <br /><br />
  <sub>Made with creativity, collaboration, and code. ❤️</sub>
</p>

<div align="center">

<img src="assets/yapspace-animated-banner.gif" width="100%" alt="YapSpace Animated Banner"/>

<br/>

# 🌈 YapSpace

### YOUR THOUGHTS. YOUR SPACE. YOUR COMMUNITY.

**Share a little. Connect a lot.**

<img src="https://img.shields.io/badge/💜_EXPRESS-8B5CF6?style=for-the-badge" />
<img src="https://img.shields.io/badge/💙_CONNECT-3B82F6?style=for-the-badge" />
<img src="https://img.shields.io/badge/🧡_SHARE-F97316?style=for-the-badge" />
<img src="https://img.shields.io/badge/💚_CREATE-10B981?style=for-the-badge" />

<br/>

[✨ ABOUT](#-welcome-to-yapspace) ·
[🚀 FEATURES](#-what-can-you-do) ·
[📸 GALLERY](#-take-a-look-around) ·
[🧠 OOP](#-the-brains-behind-yapspace) ·
[👥 TEAM](#-meet-the-creators)

</div>

---

<div align="center">

# 🎉 WELCOME TO YAPSPACE!

### A little space for BIG thoughts.

</div>

YapSpace is a community-based social platform where users can express themselves, share experiences, and connect with others.

Think of it as your digital hangout: create a post, share your feelings, react to someone's thoughts, and join the conversation!

<div align="center">

💜 **BE YOURSELF.**

💙 **SPEAK YOUR MIND.**

🧡 **CONNECT WITH OTHERS.**

</div>

---

# 🚀 WHAT CAN YOU DO?

Discover the features that make YapSpace a space for everyone!

| 🎨 FEATURE | 💬 WHAT IT DOES |
|:---|:---|
| 👤 **Register** | Create your own account. |
| 🔐 **Login** | Enter your personal account. |
| 🏠 **Community Feed** | Explore posts from the community. |
| ✍️ **Create a Post** | Share your thoughts and experiences. |
| 📝 **Edit & Delete** | Manage your own posts. |
| 💬 **Comments** | Join conversations. |
| ❤️ **Reactions** | Support, Relate, and Encourage posts. |
| 📂 **My Posts** | View your own published posts. |
| 🚪 **Logout** | Securely end your session. |

<div align="center">

### 💗 THREE WAYS TO SPREAD GOOD VIBES

| ❤️ SUPPORT | 💬 RELATE | ✨ ENCOURAGE |
|:---:|:---:|:---:|
| Show appreciation | Show understanding | Give motivation |

</div>

---

# 📸 TAKE A LOOK AROUND!

*Don't just read about it. Explore it!*

<details>
<summary>🌟 01 — LANDING PAGE</summary>

<div align="center">

### YOUR STORY STARTS HERE.

![Landing Page](screenshots/landing-page.png)

</div>

</details>

<details>
<summary>🔐 02 — LOGIN PAGE</summary>

<div align="center">

### WELCOME BACK!

![Login Page](screenshots/login-page.png)

</div>

</details>

<details>
<summary>💬 03 — COMMUNITY FEED</summary>

<div align="center">

### WHERE EVERYONE HAS SOMETHING TO SAY.

![Community Feed](screenshots/community-feed.png)

</div>

</details>

<details>
<summary>✍️ 04 — CREATE A POST</summary>

<div align="center">

### YOUR THOUGHTS DESERVE TO BE SHARED.

![Create a Post](screenshots/create-post.png)

</div>

</details>

---

# 🧠 THE BRAINS BEHIND YAPSPACE

### Four OOP principles. One awesome application.

<details>
<summary>💜 01 — ENCAPSULATION</summary>

**Keep related data and behaviors together!**

Encapsulation combines data and methods inside a class and controls access to that data.

**In YapSpace:** User and post information are organized within their respective classes.

</details>

<details>
<summary>💙 02 — INHERITANCE</summary>

**Reuse code. Build smarter!**

Inheritance allows a class to acquire properties and methods from another class.

**In YapSpace:** Related classes can reuse common properties and behaviors through inheritance where implemented.

</details>

<details>
<summary>🧡 03 — POLYMORPHISM</summary>

**One interface. Different behaviors!**

Polymorphism allows methods to behave differently depending on the object or implementation.

**In YapSpace:** Shared methods can have different implementations where polymorphism is used in the Java code.

</details>

<details>
<summary>💚 04 — ABSTRACTION</summary>

**Hide the complexity. Show what matters!**

Abstraction hides unnecessary implementation details while exposing essential functionality.

**In YapSpace:** Application components organize internal operations so users can access features without understanding all the underlying code.

</details>

---

# 🛠️ OUR TECH TOOLBOX

| 💻 TECHNOLOGY | 🎯 PURPOSE |
|:---|:---|
| ☕ Java | Main programming language |
| 🌐 HTML | Web page structure |
| 🎨 CSS | Interface styling |
| 📁 TSV Files | Local data storage |
| 🐙 Git & GitHub | Version control |
| 💡 Visual Studio Code | Development environment |

---

# 📂 PROJECT STRUCTURE

```text
🌈 YapSpace/
│
├── 🎨 assets/
│   └── yapspace-animated-banner.gif
│
├── 📸 screenshots/
│   ├── landing-page.png
│   ├── login-page.png
│   ├── community-feed.png
│   └── create-post.png
│
├── 📦 lib/
│   └── mysql-connector-j-26.10.0.jar
│
├── 💻 src/
│   └── yapspace/
│       ├── exception/
│       ├── model/
│       ├── repository/
│       ├── service/
│       ├── storage/
│       ├── web/
│       └── Main.java
│
└── README.md
```

---

# 🚀 LET'S GET YAPSPACE RUNNING!

### Follow these steps to launch your application.

<details>
<summary>💻 STEP 01 — Clone the repository</summary>

```bash
git clone https://github.com/dolienteronabels-gif/YapSpace.git
cd YapSpace
```

</details>

<details>
<summary>⚙️ STEP 02 — Compile the Java files</summary>

Run in PowerShell:

```powershell
New-Item -ItemType Directory -Force out

$files = Get-ChildItem -Recurse src -Filter *.java | ForEach-Object { $_.FullName }

javac -cp "lib\mysql-connector-j-26.10.0.jar" -d out $files
```

</details>

<details>
<summary>▶️ STEP 03 — Run the application</summary>

```powershell
java -cp "out;lib\mysql-connector-j-26.10.0.jar" yapspace.Main
```

</details>

<details>
<summary>🌐 STEP 04 — Open YapSpace</summary>

Visit this address in your browser:

**http://localhost:8080**

</details>

<div align="center">

### 🎊 YOU'RE READY TO YAP!

</div>

---

# ⚠️ A LITTLE NOTE ABOUT THE CURRENT VERSION

- Application data is stored locally using TSV files.
- Data is not automatically synchronized across different computers.
- Private messaging is not currently available.
- Image uploads in posts are not currently supported.
- Post searching and reporting are not currently available.

The MySQL connector library is included in the project, but the current runtime uses local `DataStore` storage.

---

# 🧑‍🎨 MEET THE CREATORS

<div align="center">

## 💖 TEAM 04

# RO RO ROW YOUR CODE

*Three teammates. One creative journey.*

</div>

| 🌟 MEMBER | 🎯 ROLE |
|:---|:---|
| **Doliente, Ronabel E.** | 👑 Team Leader |
| **Ebora, Rodalyn R.** | 💻 Lead Programmer |
| **Panganiban, Kristelle Mhae B.** | 🎨 UI Designer |

### 🎓 ACADEMIC DETAILS

**Institution:** Batangas State University – Alangilan Campus

**Program:** Bachelor of Science in Information Technology

**Instructor:** Ms. Fatima Marie P. Agdon

---

# 🙏 SPECIAL THANKS

We sincerely thank **Ms. Fatima Marie P. Agdon** for her guidance, encouragement, and valuable knowledge throughout the development of YapSpace.

We also appreciate the teamwork, dedication, creativity, and effort of every member of Team 04.

Every line of code, every design decision, and every challenge helped us grow as aspiring IT professionals.

---

<div align="center">

<img src="screenshots/landing-page.png" width="100%" alt="YapSpace"/>

<br/>

# 🌈 THIS IS YAPSPACE.

### YOUR THOUGHTS. YOUR SPACE. YOUR COMMUNITY.

💜 Share a little.

💙 Connect a lot.

🧡 Be part of something.

<br/>

**MADE WITH ❤️ BY TEAM 04**

*Ro Ro Row Your Code*

<br/>

[⬆️ BACK TO THE TOP](#-yapspace)

</div>

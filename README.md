#  🚀 DevOps Git Workflow Project – CI/CD with GitHub Actions & Docker

Welcome to **DevOps Git Workflow**, a structured Node.js app designed to demonstrate **best practices in Git-based DevOps workflows**. This project was created to complete **Task 4: Build a Version-Controlled DevOps Project with Git** by showcasing GitFlow strategy, CI/CD automation and detailed task documentation.

---

## 🎯 Project Objective

**TASK 4 Goal:**  
> Manage a DevOps project using Git best practices, including version control, branching, CI/CD, tagging, and documentation.

---

## 🛠️ Tools & Technologies Used

- **Git & GitHub** – Version control & collaboration
- **GitHub Actions** – CI/CD automation
- **Docker** – Containerization
- **Node.js + Express** – Simple web server with API
- **Jest + Supertest** – Automated testing
- **Markdown** – Documentation


## 📁 Project Structure

```bash
.
├── .github/workflows/          # CI/CD workflows
│   └── main.yml
│   └── PULL_REQUEST_TEMPLATE.md
│   └── dev-ci.yml
├── public/                     # Static website
│   └── index.html
├── test/                       # Jest API test
│   └── app.test.js
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── index.js
├── package.json
├── README.md                   # This file
└── tasks.md                    # Task tracking (Markdown)

```
---

## 🌐 Live Screenshots

### 🖼️ Main Webpage
![Main Page Screenshot](images/main-page.png)

### 🖼️ API Endpoint - `/api/hello`
![API Screenshot](images/api-page.png)

---

## 🧪 How to Run the App Locally

```bash
# 1. Install dependencies
npm install

# 2. Start the app
npm start

# 3. Run tests
npm test

# 4. Open your browser
http://localhost:3000

```

## 🐳 Docker Guide

### 🔨 Build Docker Image Locally

```bash
docker build -t my-node-app .
```

▶️ Run Docker Container Locally
```bash
docker run -p 3000:3000 my-node-app
```

# 🔄 Git Workflow Strategy

This project follows a structured **GitFlow model** to manage development, testing, and deployment in a clean and reliable manner.

---

## 📌 Branch Structure

| Branch        | Purpose                          |
|---------------|----------------------------------|
| `main`        | Production-ready code only       |
| `test`        | QA / Staging environment         |
| `dev`         | Integration of all features      |
| `feature/*`   | Feature branches (short-lived)   |
| `hotfix/*`    | Emergency fix branches           |

---

## 🧪 Branch Flow

```plaintext
✅ Developers work on feature/* or hotfix/*
🔁 Merge into dev via pull requests
✅ dev → test PR triggers GitHub Actions
🔄 If tests pass, test auto-merges → main
☁️ Production deploy runs on main
```

---- 
## ⚙️ CI/CD Pipeline

> Workflow file: `.github/workflows/main.yml`

```plaintext
✅ Checkout source code

✅ Install dependencies with npm ci

✅ Run tests using Jest

🔁 Auto-merge test → main if tests pass
```

## 🧪 Pull Request CI – `dev-ci.yml`

This GitHub Actions workflow ensures that any code merged into the `dev` branch passes basic CI checks.

**File Location:** `.github/workflows/dev-ci.yml`

----

## 🧾 Documentation & Commit Hygiene

- 🗂️ All tasks are documented in [`tasks.md`](./tasks.md)
- 🧠 Followed **semantic commit messages**:
  - `feat:` – New features
  - `fix:` – Bug fixes
  - `chore:` – Non-functional changes (docs, configs, etc.)
- 🏷️ Used **GitHub Tags** to version important releases

### 🏷️ Example Git Tag

```bash
git tag -a v1.0.0 -m "Initial Dockerized release"
git push origin v1.0.0
```

## ✅ How This Repo Satisfies Task 4

This repository fulfills all the requirements of **Task 4: Build a Version-Controlled DevOps Project with Git**.

| Requirement                             | Completed |
|----------------------------------------|-----------|
| Initialize Git & push to GitHub        | ✅        |
| Create `dev`, `feature`, `main` branches | ✅        |
| Use pull requests to merge             | ✅        |
| Add a complete `README.md`             | ✅        |
| Use `.gitignore` and tags              | ✅        |
| Document tasks in Markdown (`tasks.md`) | ✅        |

----

> Made with ❤️ by Dhanush Nadar to fulfill DevOps Git Workflow – Task 4

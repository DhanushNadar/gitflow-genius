# 📋 DevOps Git Workflow – Task Documentation

This file tracks the progress and execution of **Task 4: Build a Version-Controlled DevOps Project with Git**. It logs the steps, decisions, and actions taken throughout the development and DevOps setup process.

---

## 🎯 Task Objective

> Manage a DevOps project using Git best practices  
> Tools: Git, GitHub  
> Deliverables: Project repo with proper commits, branching

---

## ✅ Task Checklist

| Task Item                          | Status | Notes |
|-----------------------------------|--------|-------|
| Initialize Git repository         | ✅     | Used `git init` and pushed to GitHub |
| Create `main`, `dev`, `feature` branches | ✅ | Followed GitFlow convention |
| Use pull requests for merging     | ✅     | All merges done via PR |
| Add a proper `README.md`          | ✅     | Explained project, CI/CD, flow |
| Use `.gitignore`                  | ✅     | Excludes `node_modules`, `.env`, etc |
| Use Git tags                      | ✅     | Tagged production-ready commits |
| Document tasks in markdown        | ✅     | This file 😊 |

---

## 🛠️ Implementation Log

### 📅 2025-04-11 – Full DevOps Workflow Execution

- Initialized local Git repo and created `.gitignore`
- Pushed first commit to GitHub

**Branch Setup**
- Created `main`, `dev`, and `feature/setupdocker` branches

**Feature Work**
- Developed `Dockerfile` and `docker-compose.yml`
- Built and tested Docker image locally
- Added basic API tests using Jest
- Committed all changes to `feature/setupdocker`

**Pull Requests & CI**
- Opened PR from `feature/setupdocker` → `dev`
- Added GitHub Actions workflow (`dev-ci.yml`) to run tests on PR
- Tests passed successfully

**Staging Workflow**
- Merged `dev` → `test` via PR
- CI/CD pipeline (`main.yml`) triggered on `test` push
  - Ran tests
  - Built Docker image
  - (Optional) Pushed to DockerHub
  - Automatically merged `test` → `main`

**Version Tagging**
- Created Git tag `v1.0.0` to mark first successful release

---

## 🔄 Git Branch Strategy Used

```plaintext
feature/* → dev → test → main
```
# IAConsult Git Workflow Standard

This document defines the official Git workflow for all IAConsult projects.

---

## 1️⃣ Branch Structure

- main      → Production-ready code
- dev       → Integration branch
- feature/* → New features
- hotfix/*  → Urgent production fixes

---

## 2️⃣ Branch Rules

main:
- Always stable
- Always deployable
- Protected branch
- No direct push allowed

dev:
- Receives merged features
- Tested before going to main

feature branches:
- Created from dev
- Named as:
  - feature/payment-mobile
  - feature/ai-report
  - feature/user-dashboard

hotfix branches:
- Created from main
- Merged back into main and dev

---

## 3️⃣ Pull Request Policy

Every change must:

- Be reviewed (even if self-reviewed)
- Pass CI checks
- Have clear commit message
- Describe purpose in PR

Recommended merge strategy:
- Squash and merge

---

## 4️⃣ Commit Message Convention

Use clear and structured messages:

- feat: add payment integration
- fix: resolve login bug
- refactor: improve auth middleware
- docs: update architecture documentation

---

## 5️⃣ Deployment Flow

feature → dev → main → production

Production deployment triggered from main only.

---

## 6️⃣ Discipline Rules

- Never commit secrets
- Never push broken builds
- Never bypass branch protection
- Keep commits clean and atomic

---

Professional workflow builds professional products.

Maintained by IAConsult Engineering

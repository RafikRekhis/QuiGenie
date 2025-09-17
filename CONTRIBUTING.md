# Contributing — QuiGenie

QuiGenie is developed as a solo project (Windows-first), but this guide documents conventions so the workflow remains clean and consistent.  

---

## Branching Model

- **Default branch:** `main` (protected)
- **Work happens in short-lived branches**:
  - Features → `feat/<scope>-<short-desc>`  
    e.g., `feat/auth-login-endpoint`
  - Fixes → `fix/<scope>-<short-desc>`  
    e.g., `fix/quiz-timer-off-by-one`
  - Chores → `chore/<topic>-<short-desc>`  
    e.g., `chore/spotless-plugin`

**Rules:**
1. Branches are **small and focused** (1–3 commits max).
2. Always create a **Pull Request into `main`** (no direct pushes).
3. Rebase/fast-forward before merging to keep history clean.
4. **PR titles must follow Conventional Commits**.

---

## Conventional Commits

Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/) style:  

- `feat: ...` → new feature  
- `fix: ...` → bug fix  
- `docs: ...` → documentation only  
- `chore: ...` → maintenance / tooling  
- `refactor: ...` → code change not adding a feature or fix  
- `test: ...` → test-related changes  
- `ci: ...` → CI/CD changes  
- `build: ...` → build system or dependencies  

Example:

feat(auth): add login endpoint with JWT

---

## Pull Requests

Every change must go through a Pull Request:  

- Use the PR template (`.github/PULL_REQUEST_TEMPLATE.md`).
- Provide a short description of **what** and **why**.
- Document **how to test** locally (steps, screenshots if UI).
- Use the **checklist** before merging.

---

## Documentation

- Internal notes, ADRs, and sprint planning live in `/docs` locally.  
  This folder is **gitignored** and must never be committed.  
- Public repo docs are only:
  - `README.md` (project overview)
  - `CONTRIBUTING.md` (this file)
  - `.github/*` (PR/Issue templates, CODEOWNERS)

---

## Summary

- Trunk-based workflow with `main` protected.  
- Short-lived feature/fix/chore branches.  
- PR required for every change.  
- Commits follow Conventional Commits.  
- Local docs stay in `/docs`, never pushed.

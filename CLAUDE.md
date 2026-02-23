# CLAUDE.md

This file defines how Claude should behave when working in this repository.
Claude reads this file automatically when invoked via Claude Code or GitHub Actions.

---

## Project Overview

> **TODO:** Replace this section with a description of your project.
> - What does this project do?
> - Who is it for?
> - What problem does it solve?

Example:
> This is a REST API service for managing user accounts and authentication.
> Built with Node.js / Python / Go / etc.

---

## Architecture

> **TODO:** Briefly describe the folder structure and key components.

```
/
├── src/           # Main source code
├── tests/         # Test files
├── scripts/       # Utility/automation scripts
├── docs/          # Documentation
└── .github/       # GitHub Actions workflows
```

---

## Development Commands

> **TODO:** Fill in your actual commands.

```bash
# Install dependencies
npm install          # or: pip install -r requirements.txt

# Run the project locally
npm run dev          # or: python main.py

# Run tests
npm test             # or: pytest

# Lint / format
npm run lint         # or: ruff check .

# Build
npm run build
```

---

## Coding Standards

- **Language:** TypeScript / Python / Go / etc. *(update this)*
- **Style guide:** Follow existing patterns in the codebase
- **Tests:** All new features should include tests
- **Commits:** Use conventional commits (`feat:`, `fix:`, `docs:`, `chore:`)
- **PRs:** Keep PRs small and focused on a single change

### Naming Conventions
- Files: `kebab-case`
- Functions: `camelCase` (JS/TS) or `snake_case` (Python)
- Classes: `PascalCase`
- Constants: `UPPER_SNAKE_CASE`

---

## What Claude Should Do

When invoked via `@claude` in a PR or issue:

- ✅ Review code for bugs, logic errors, and security issues
- ✅ Suggest improvements and refactors
- ✅ Write or fix tests
- ✅ Implement small features described in issue/PR comments
- ✅ Fix failing CI checks
- ✅ Update documentation

### What Claude Should NOT Do

- ❌ Push directly to `main` or `master` branch
- ❌ Delete files without explicit instruction
- ❌ Change environment variables or secrets
- ❌ Modify CI/CD pipeline configuration without review

---

## Environment & Secrets

> **TODO:** List any environment variables needed (never put actual values here).

```
DATABASE_URL=         # PostgreSQL connection string
API_KEY=              # External service API key
SECRET_KEY=           # App secret key
```

---

## Known Issues / Context

> **TODO:** Add any context Claude should know about:
> - Known tech debt areas
> - Files to avoid touching
> - Ongoing refactors
> - Special edge cases

---

## Reviewers & Owners

> **TODO:** Add codeowners info if relevant.

- **Backend:** @your-handle
- **Frontend:** @your-handle
- **DevOps:** @your-handle

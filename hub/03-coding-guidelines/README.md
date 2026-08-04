# Coding Guidelines & Standards

This directory outlines the mandatory coding standards, linting rules, formatting configurations, and naming conventions for all repositories across the organization.

---

## 🧹 Core Principles

1. **Clean Code:** Write readable, maintainable, and self-documenting code. Avoid complex, over-engineered solutions.
2. **Consistent Formatting:** All projects must use automated linters and formatters (e.g., ESLint/Prettier for Node.js, Black/Flake8 for Python) to maintain uniform code style.
3. **Meaningful Naming:** Use descriptive names for variables, functions, classes, and files. Avoid single-letter variables except for standard loop counters.
4. **Error Handling:** Never swallow exceptions. Always catch specific errors, log them appropriately, and return standardized error responses to clients.

---

## 📝 Naming Conventions

* **Files & Directories:** Use kebab-case (e.g., `user-auth-service`, `data-parser.py`).
* **Variables & Functions:** Use camelCase in JavaScript/Node.js and snake_case in Python.
* **Classes:** Use PascalCase in both languages (e.g., `UserService`, `DatabaseConnector`).
* **Constants:** Use UPPER_SNAKE_CASE (e.g., `MAX_RETRIES`, `DEFAULT_TIMEOUT`).


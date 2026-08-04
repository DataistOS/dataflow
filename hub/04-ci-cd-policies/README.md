# CI/CD Policies & Automation Standards

This directory defines the continuous integration and continuous deployment (CI/CD) policies, pipeline structures, and automation rules required for all organization repositories.

---

## 🚀 Core CI/CD Pipelines

Every repository must implement automated workflows (e.g., GitHub Actions, GitLab CI) covering the following stages:

1. **Linting & Code Formatting:**
    * Automatically check code style on every Pull Request.
    * Reject PRs that fail linting rules (ESLint, Flake8, Prettier, etc.).

2. **Automated Testing:**
    * Run unit and integration tests (`pytest`, `jest`, etc.) in an isolated container environment.
    * Maintain a minimum code coverage threshold (e.g., 80%).

3. **Security Scanning:**
    * Scan dependencies for known vulnerabilities (e.g., `npm audit`, `safety`, Snyk).
    * Ensure no secrets or API keys are hardcoded in the repository.

4. **Automated Deployment:**
    * Build container images upon merging into the `main` or `production` branch.
    * Push images to the organization container registry and trigger staging/production deployments.

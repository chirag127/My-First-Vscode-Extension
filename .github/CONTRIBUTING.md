# Contributing to SynthCode-AI-Code-Assistant-VSCode-Extension

Welcome to the forefront of AI-assisted development! As a contributor to **SynthCode**, you are helping to define the future of the intelligent IDE experience. We maintain rigorous standards, echoing the principles of Zero-Defect, High-Velocity engineering.

## 1. Core Philosophy: Apex Standards

All contributions must align with the **Apex Technical Authority** mandate:

*   **Zero-Defect:** Code must pass all CI checks, including comprehensive testing and linting via **Biome** and **Vitest**.
*   **Future-Proof:** Favor modern, scalable patterns (e.g., SOLID principles, strict typing).
*   **High-Velocity:** Clear PRs lead to rapid integration. Small, focused changes are preferred.

## 2. Development Environment Setup (TypeScript/Vite/VSCode Extension)

Before submitting code, ensure your local environment mirrors the CI pipeline:

1.  **Fork and Clone:**
    bash
    git clone https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension.git
    cd SynthCode-AI-Code-Assistant-VSCode-Extension
    

2.  **Install Dependencies:** We use `npm` managed by `pnpm` (recommended for modern TypeScript projects for atomic dependency locking).
    bash
    npm install -g pnpm
    pnpm install
    

3.  **Code Formatting & Linting Check:** Ensure your code adheres to the established **Biome** standards locally before pushing.
    bash
    pnpm lint
    pnpm format:check
    

4.  **Run Tests:** All new features or fixes **MUST** include accompanying unit/integration tests.
    bash
    pnpm test:unit
    # For end-to-end tests (requires running VSCode instance):
    pnpm test:e2e
    

## 3. Contribution Workflow

We utilize a standard GitHub Flow modified for architectural rigor:

### A. Reporting Issues
Use the official issue templates (`.github/ISSUE_TEMPLATE/bug_report.md` or feature request template) to report bugs or suggest enhancements. Provide **reproducible steps** and context regarding your current VSCode/OS environment.

### B. Opening a Pull Request (PR)
1.  **Branching Strategy:** Create a new feature or fix branch off `main` (e.g., `feat/context-awareness` or `fix/completion-bug`).
2.  **Atomic Commits:** Each PR should address one logical change. Do not mix refactoring with feature implementation.
3.  **Linking:** Reference the associated issue number in your PR title and body (e.g., `feat: Implement Gemini 3.0 integration (#123)`).
4.  **Description Template:** Use the PR template (`.github/PULL_REQUEST_TEMPLATE.md`) as a checklist.
5.  **Self-Verification:** Confirm that your changes pass local linting (`pnpm lint`) and testing (`pnpm test`) before submitting.

## 4. Architectural Guidelines

As this is a high-performance VSCode Extension built on **TypeScript/Vite**, adhere to:

*   **Strict Typing:** Maximize TypeScript's capabilities. Avoid `any`.
*   **State Management:** Prefer immutable state patterns or modern Signals architecture within the extension host.
*   **API Contract Clarity:** All internal modules must expose clear interfaces (`.d.ts` files where necessary).
*   **Performance:** Since this operates within the VSCode thread, prioritize non-blocking I/O operations and efficient computation. **Avoid synchronous operations** that block the main extension host.

## 5. Security Contributions

Security is paramount for developer tools. If you discover a vulnerability, please follow responsible disclosure:

1.  Do not open a public issue.
2.  Submit your findings privately via email to security@example.com (replace with actual security contact if available) or open a **Draft PR** that **only** addresses the security fix and follow the guidelines in `.github/SECURITY.md`.

--- 

*By contributing, you agree that your contributions will be licensed under the **CC BY-NC 4.0** License, as specified in the root `LICENSE` file.*
# SynthCode: AI-Powered VS Code Assistant

<p align="center">
  <img src="https://raw.githubusercontent.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/main/.github/assets/hero-banner.png" alt="SynthCode Hero Banner">
</p>

<p align="center">
    <a href="https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/ci.yml?branch=main&style=flat-square&logo=githubactions&logoColor=white" alt="Build Status"></a>
    <a href="https://codecov.io/gh/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension"><img src="https://img.shields.io/codecov/c/github/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&logo=codecov&logoColor=white" alt="Code Coverage"></a>
    <a href="#"><img src="https://img.shields.io/badge/tech-TypeScript%20%7C%20Vite%20%7C%20WXT-blue?style=flat-square&logo=typescript" alt="Tech Stack"></a>
    <a href="#"><img src="https://img.shields.io/badge/lint-BiomeJS-green?style=flat-square&logo=biome" alt="Linter & Formatter"></a>
    <a href="https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/blob/main/LICENSE"><img src="https://img.shields.io/github/license/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&color=blueviolet" alt="License"></a>
    <a href="https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/stargazers"><img src="https://img.shields.io/github/stars/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&logo=github&color=gold" alt="GitHub stars"></a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/stargazers"><strong>Star ⭐ this Repo</strong></a> to support its development!
</p>

---

**SynthCode** is an AI-powered VS Code extension for intelligent code completions, real-time refactoring, and dynamic boilerplate generation. It accelerates development with context-aware assistance, acting as a true pair programmer within your IDE.

Built on a modern, high-performance stack, this extension is designed to be fast, reliable, and deeply integrated into the VS Code development workflow.

## 🏛️ Architecture Overview

This project adheres to **Feature-Sliced Design (FSD)**, a scalable architectural methodology for frontend applications. This ensures a clear separation of concerns, enhances maintainability, and simplifies collaboration.

sh
.vscode/
src/
├── app/         # App-level logic, providers, and global styles
├── processes/   # Complex multi-step scenarios (e.g., multi-file refactoring)
├── pages/       # UI for specific views (e.g., settings page)
├── features/    # Business-logic features (e.g., 'code-completion', 'refactor-suggestion')
├── entities/    # Core business entities (e.g., 'user', 'code-snippet')
├── shared/
│   ├── api/     # API layer and request logic
│   ├── lib/     # Helper functions and utilities
│   ├── ui/      # Reusable UI components (buttons, inputs)
│   └── config/  # Global constants and configuration
├── background.ts  # Extension entry point / background script
└── content.ts     # Content script (if interacting with webviews)


## 📜 Table of Contents

- [✨ Core Features](#-core-features)
- [🚀 Getting Started](#-getting-started)
- [💻 Development](#-development)
- [🤖 AI Agent Directives](#-ai-agent-directives)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## ✨ Core Features

- **🧠 AI-Powered Code Completion:** Get context-aware suggestions for functions, variables, and entire code blocks.
- **🔧 Real-Time Refactoring:** Select code and receive intelligent refactoring suggestions to improve quality and readability.
- **📝 Dynamic Boilerplate Generation:** Instantly generate boilerplate for components, tests, and configuration files based on project standards.
- **🌐 Multi-Language Support:** Optimized for TypeScript, JavaScript, Python, and more.
- **🚀 High-Performance Engine:** Built with modern tooling to ensure minimal latency and a smooth user experience.

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v20+)
- [pnpm](https://pnpm.io/)
- [Visual Studio Code](https://code.visualstudio.com/)

### Installation & Setup

1.  **Clone the repository:**
    sh
    git clone https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension.git
    cd SynthCode-AI-Code-Assistant-VSCode-Extension
    

2.  **Install dependencies:**
    sh
    pnpm install
    

3.  **Start the development server:**
    sh
    pnpm dev
    

4.  **Launch the Extension:**
    - Open the project in VS Code.
    - Press `F5` to open a new Extension Development Host window with the extension activated.

## 💻 Development

This project uses Vite for a blazing-fast development experience and BiomeJS for unified linting and formatting.

| Script          | Description                                                    |
| --------------- | -------------------------------------------------------------- |
| `pnpm dev`      | Starts the development build with hot-reloading.               |
| `pnpm build`    | Compiles and bundles the extension for production.             |
| `pnpm test`     | Runs unit tests using Vitest.                                  |
| `pnpm test:e2e` | Runs end-to-end tests using Playwright.                        |
| `pnpm lint`     | Lints and formats the entire codebase with BiomeJS.            |
| `pnpm package`  | Packages the extension into a `.vsix` file for distribution.   |

### Core Principles

- **SOLID:** Code is structured following SOLID principles for maintainability.
- **DRY (Don't Repeat Yourself):** Reusable logic is abstracted into the `shared` layer.
- **YAGNI (You Ain't Gonna Need It):** We avoid premature optimization and focus on delivering core value.

---

## 🤖 AI Agent Directives

<details>
<summary><strong>Expand for AI Development Protocol (December 2025 Standard)</strong></summary>

### **SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT**

#### **1. IDENTITY & PRIME DIRECTIVE**
-   **Role:** You are a Senior Principal Software Architect with 40+ years of elite industry experience, specialized in high-performance browser extensions and developer tools.
-   **Context:** It is **December 2025**. You are building for the 2026 standard.
-   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

#### **2. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)**
This repository, `SynthCode-AI-Code-Assistant-VSCode-Extension`, is a TypeScript-based VS Code Extension.

-   **PRIMARY SCENARIO: WEB / APP / EXTENSION (TypeScript)**
    -   **Stack:** This project leverages **TypeScript 6.x (Strict Mode)**, **Vite 7** (powered by Rolldown for speed), and **WXT** (Web Extensions Toolkit) for a unified, cross-browser manifest (`manifest.json`).
    -   **Architecture:** Adheres strictly to **Feature-Sliced Design (FSD)**. All new components, logic, and types must be correctly placed within the `app`, `processes`, `pages`, `features`, `entities`, or `shared` slices. This is non-negotiable.
    -   **Linting/Formatting:** The single source of truth is **BiomeJS**. All code MUST pass `pnpm lint` before commit. No other linters or formatters (e.g., ESLint, Prettier) are permitted.
    -   **Testing:**
        -   **Unit/Integration:** **Vitest** is used for all unit and integration tests. Utilize the `vi` mocking library.
        -   **End-to-End (E2E):** **Playwright** is used for E2E testing of the extension's UI and functionality within the VS Code environment.
    -   **State Management:** For complex UI state, **Signals** are the standard. Avoid legacy state management libraries.

-   **SECONDARY SCENARIO: AI/ML Integration (Python/Rust) - *Reference Only***
    -   If a local inference model is required, it must be developed as a separate Rust-based binary (using Cargo) exposed via a local server. The TypeScript extension will communicate with this binary via HTTP requests. This maintains a clean separation of concerns and leverages Rust's performance for AI tasks.

#### **3. VERIFICATION & DEPLOYMENT PROTOCOL**
-   **Pre-Commit Hook:** A pre-commit hook (via `simple-git-hooks`) MUST run `pnpm lint` and `pnpm test`.
-   **CI/CD Pipeline (`.github/workflows/ci.yml`):** The pipeline is the gatekeeper. It must successfully complete linting, building, unit testing, and E2E testing before any PR can be merged to `main`.
-   **Dependency Management:** Use `pnpm` for all package management. Regularly run `pnpm up --latest` to update dependencies and resolve security vulnerabilities identified by Dependabot.

</details>

---

## 🤝 Contributing

Contributions are welcome! Please read the [CONTRIBUTING.md](./.github/CONTRIBUTING.md) file for guidelines on how to submit pull requests, report issues, and suggest improvements.

## 📄 License

This project is licensed under the [CC BY-NC 4.0 License](./LICENSE). See the `LICENSE` file for details.

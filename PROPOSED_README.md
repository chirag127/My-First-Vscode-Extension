# SynthCode-AI-Code-Assistant-VSCode-Extension

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/ci.yml?label=Build&style=flat-square)](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?label=Coverage&style=flat-square)](https://codecov.io/gh/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension)
[![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?style=flat-square)](https://www.typescriptlang.org/)
[![Frameworks](https://img.shields.io/badge/Vite%20%7C%20Biome%20%7C%20Playwright-Core%20Stack-F9A825?style=flat-square)](https://vitejs.dev/)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square)](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension)

### 🌟 Star ⭐ this Repo to Support Future Development!

--- 

**SynthCode** is an advanced, context-aware VS Code Extension designed to synthesize complex development tasks into rapid execution. It delivers intelligent code completions, on-demand refactoring suggestions, and dynamic boilerplate generation directly within the editor, optimizing developer flow state.

---

## 🧠 AI Agent Directives (The Apex Protocol)

<details>
<summary>Click to expand: Core Architectural Alignment & Verification</summary>

### 1. Identity & Context
**Role:** Senior Principal Software Architect / Master Technical Copywriter (40+ Years Experience).
**Context:** December 2025 Standard (Future-Proofing).
**Goal:** Maintain Zero-Defect, High-Velocity delivery for this TypeScript/VS Code Extension environment.

### 2. Apex Toolchain & Stack Enforcement
This project adheres to **SCENARIO A: WEB / APP / GUI (Modern Frontend)** standards:
*   **Language:** TypeScript (Strict Mode Enforced).
*   **Bundler/Runner:** Vite 7.x.
*   **Styling:** TailwindCSS v4 (or equivalent utility-first approach).
*   **Testing Suite:** Vitest (Unit/Integration) & Playwright (End-to-End).
*   **Linter/Formatter:** Biome (Unified Speed and Simplicity).
*   **Architecture Pattern:** Feature-Sliced Design (FSD) for superior module boundaries and scalability.

### 3. Architectural Principles
All generated code and proposed fixes must adhere rigorously to:
*   **SOLID Principles:** Especially Single Responsibility (SRP) for extension components and Dependency Inversion (DIP) for AI service abstraction.
*   **DRY:** Eliminate all duplicate logic, relying on shared utility functions within the `shared` or `utils` layer of the FSD structure.
*   **YAGNI:** Only implement features explicitly requested or immediately necessary to meet the core value proposition (Completion, Refactoring, Generation).

### 4. Verification & Deployment Commands
To ensure compliance and operational readiness, utilize these commands:

| Task | Command | Purpose |
| :--- | :--- | :--- |
| **Format Check** | `npx @biomejs/biome check --apply ./src` | Apply formatting and lint fixes automatically. |
| **Unit Testing** | `npm run test:unit` | Execute Vitest suite across all feature modules. |
| **E2E Testing** | `npx playwright test` | Validate extension functionality in a headless browser context. |
| **Build Extension** | `npm run build` | Compile TypeScript and bundle assets for VS Code packaging. |

</details>

## 2. Architecture Visualization (FSD Example)

mermaid
graph TD
    subgraph SynthCode Extension Layer
        A[UI: VSCode Views/Commands] --> B(Features/Completion);
        A --> C(Features/Refactoring);
        A --> D(Features/Generation);
    end

    B --> E(Entities: CodeAST/Context);
    C --> E;
    D --> E;

    E --> F(Shared: Types/Interfaces);
    B --> G(Shared: AI-Service-Adapter);
    C --> G;
    D --> G;

    G --> H[External: AI API Gateway];

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style H fill:#ccf,stroke:#333,stroke-width:2px


## 3. Table of Contents

1.  [AI Agent Directives](#-ai-agent-directives-the-apex-protocol)
2.  [Architecture Visualization (FSD Example)](#-architecture-visualization-fsd-example)
3.  [Table of Contents](#-table-of-contents)
4.  [Core Features](#-core-features)
5.  [Development Workflow](#-development-workflow)
    *   [Prerequisites](#-prerequisites)
    *   [Setup & Installation](#-setup--installation)
    *   [Execution Scripts](#-execution-scripts)
6.  [Contributing Guidelines](#-contributing-guidelines)
7.  [Security & Licensing](#-security--licensing)

## 4. Core Features

*   **Intelligent Contextual Completion:** Leverages the language server protocol awareness combined with external AI models to suggest syntactically and semantically correct code blocks.
*   **Real-Time Refactoring:** Analyze selected code blocks and propose idiomatic, optimized refactoring paths (e.g., extracting methods, simplifying conditionals).
*   **Dynamic Boilerplate Generation:** Generate complex file structures, configuration scaffolding (e.g., `tsconfig.json`, complex hooks), or test stubs based on natural language prompts.
*   **Strict Typing Enforcement:** Built entirely on TypeScript, ensuring all internal logic and external API interactions are rigorously type-checked by the compiler.

## 5. Development Workflow

### Prerequisites

*   Node.js (v18.x or higher)
*   Git
*   VS Code

### Setup & Installation

Follow these steps to clone the repository and prepare the development environment according to Apex standards:

bash
# 1. Clone the repository
git clone https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension.git
cd SynthCode-AI-Code-Assistant-VSCode-Extension

# 2. Use uv (or npm/yarn for frontend ecosystem) for dependency resolution and installation
npm install

# 3. Ensure all code conforms to Biome standards
npx @biomejs/biome check --apply


### Execution Scripts

All development commands are managed via `package.json` scripts, optimized for CI/CD integration:

| Script | Command | Description |
| :--- | :--- | :--- |
| `build` | `npm run build` | Compiles TypeScript using Vite into production assets. |
| `watch` | `npm run dev` | Runs the development server for hot-reloading during extension development. |
| `test:unit` | `npm run test:unit` | Runs Vitest unit and integration tests. |
| `test:e2e` | `npx playwright test` | Executes Playwright end-to-end functional validation. |
| `lint:fix` | `npx @biomejs/biome check --apply` | Formats and fixes code style issues globally. |

## 6. Contributing Guidelines

We welcome contributions that uphold the **Zero-Defect, High-Velocity** standard. Please review the comprehensive guidelines located at **`.github/CONTRIBUTING.md`** before submitting Pull Requests. All contributions must pass automated checks enforced by `.github/workflows/ci.yml`.

## 7. Security & Licensing

**Security:** Refer to **`.github/SECURITY.md`** for vulnerability disclosure procedures. We prioritize secure coding practices, especially around external API key handling.

**License:** This project is licensed under the **CC BY-NC 4.0 License**. See the **LICENSE** file for details. Commercial use without express permission is prohibited.
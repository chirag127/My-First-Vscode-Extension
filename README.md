# SynthCode-AI-Code-Assistant-VSCode-Extension

[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/ci.yml?style=flat-square&logo=github)](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&logo=codecov)](https://codecov.io/github/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension)
[![Tech Stack](https://img.shields.io/badge/TypeScript-7.x-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Lint & Format](https://img.shields.io/badge/Biome-latest-orange?style=flat-square&logo=biome)](https://biome.dev/)
[![License](https://img.shields.io/github/license/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&logo=creativecommons)](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/blob/main/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension?style=flat-square&logo=github)](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/stargazers)

**SynthCode** is an AI-powered VS Code extension that provides intelligent, context-aware code completions, real-time refactoring suggestions, and dynamic boilerplate generation to dramatically accelerate your development workflow.

## ✨ Features

*   **Intelligent Code Completions:** Leverage advanced AI models to predict and suggest code snippets with unparalleled accuracy.
*   **Real-time Refactoring:** Receive AI-driven suggestions for code improvements, optimizations, and best-practice adherence as you type.
*   **Dynamic Boilerplate Generation:** Instantly create common code structures, API calls, and component setups based on your context.
*   **Context-Aware Assistance:** The AI understands your project's nuances, providing relevant and targeted help.
*   **Productivity Boost:** Significantly reduce typing, debugging time, and cognitive load.

## 🚀 Architecture & Tech Stack

This extension is meticulously engineered using the latest industry standards for robust, high-performance development.

*   **Primary Language:** TypeScript 7.x (Strict Mode)
*   **Extension Framework:** VS Code Extension API
*   **Bundling & Build:** Vite 7 (utilizing Rollup's core for efficient bundling)
*   **Styling/UI:** Tailwind CSS v4 (for declarative styling)
*   **Linting & Formatting:** Biome (for lightning-fast code analysis and formatting)
*   **Testing:** Vitest (for fast unit tests) & Playwright (for comprehensive E2E testing)
*   **Architecture Pattern:** Feature-Sliced Design (FSD) for maintainable and scalable codebase organization.

mermaid
graph TD
    A[Extension API] --> B(UI Layer - React/Preact/Vue Components)
    B --> C(Features Layer - Business Logic)
    C --> D(Entities Layer - Core Data Structures)
    C --> E(API Layer - VS Code API Integrations)
    E --> F(AI Service Integration)
    F --> G(External AI Models)
    D --> H(Shared - Utilities, Types)
    subgraph Core
        A
        B
        C
        D
        E
        F
        H
    end
    subgraph External
        G
    end


## 🤝 AI Agent Directives

<details>
<summary>View AI Agent Directives</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (TypeScript)**
    *   **Stack:** This project leverages **TypeScript 7.x** (Strict Mode). Key tools include **Vite 7** (with Rolldown), **Tailwind CSS v4**, and the **VS Code Extension API**. For testing, **Vitest** is used for unit tests and **Playwright** for end-to-end tests.
    *   **Architecture:** Adheres to the **Feature-Sliced Design (FSD)** pattern for modularity and maintainability. State management utilizes standardized Signals.
    *   **AI Integration:** Deeply integrated with **OpenAI API** (latest models as of Dec 2025) for intelligent code completions and refactoring suggestions. Prioritize modular design, clear API contracts, and robust error handling for all AI model interactions.
    *   **UI Framework:** Components can be built with React, Preact, or Vue, adhering to FSD principles.

</details>

## 📚 Development Setup

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension.git
    cd SynthCode-AI-Code-Assistant-VSCode-Extension
    

2.  **Install dependencies:**
    bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    

3.  **Run in development mode:**
    bash
    npm run dev
    # or
    yarn dev
    # or
    pnpm dev
    

4.  **Build for production:**
    bash
    npm run build
    # or
    yarn build
    # or
    pnpm build
    

## 📜 Scripts

| Script        | Description                                     |
| :------------ | :---------------------------------------------- |
| `dev`         | Run the extension in development mode.          |
| `build`       | Build the extension for production.             |
| `lint`        | Run Biome linter and formatter.                 |
| `test:unit`   | Run Vitest unit tests.                          |
| `test:e2e`    | Run Playwright end-to-end tests.                |
| `package`     | Package the extension for distribution.         |

## 📐 Principles

*   **SOLID:** Adherence to Object-Oriented Design principles for maintainable code.
*   **DRY (Don't Repeat Yourself):** Minimize code duplication.
*   **YAGNI (You Ain't Gonna Need It):** Implement only necessary features.
*   **FSD (Feature-Sliced Design):** Promote modularity and clear boundaries within the codebase.

## ⚖️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](LICENSE) file for more details.

## ⭐ Star This Repo

If you find SynthCode useful, please consider starring this repository on GitHub! Your support is greatly appreciated.

# 🚀 CoderCopilot-AI-Code-Assistance-VSCode-Extension

## The Apex Standard for AI-Driven Developer Productivity

<!-- SOCIAL PROOF & BADGES (CRITICAL METADATA) -->
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension?style=flat-square&color=yellow)](https://github.com/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension/stargazers)
[![Build Status](https://github.com/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension/actions/workflows/ci.yml/badge.svg)](https://github.com/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension/actions/workflows/ci.yml)
[![Test Coverage](https://codecov.io/gh/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension/branch/main/graph/badge.svg)](https://codecov.io/gh/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension)
[![Technology Stack](https://img.shields.io/badge/Stack-TS%20%7C%20VSCode%20API%20%7C%20OpenAI-2C3E50?style=flat-square&logo=typescript&logoColor=white)](https://code.visualstudio.com/api)
[![Linter/Formatter](https://img.shields.io/badge/Linter-Biome-32213A?style=flat-square&logo=biome&logoColor=white)](https://biomejs.dev/)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-darkblue.svg?style=flat-square)](./LICENSE)

---
<p align="center">
  Star ⭐ this Repo to Support Elite Open Source Development!
</p>
---

### 🌟 Executive Summary (BLUF)

CoderCopilot is an advanced, AI-powered Visual Studio Code extension engineered to accelerate developer workflow. Utilizing modern language models, it provides real-time intelligent code completion, sophisticated refactoring suggestions, and contextual documentation generation directly within the IDE, ensuring higher code quality and velocity.

### 🏛️ Architecture and Structure

This project follows the **Feature-Sliced Design (FSD)** pattern, adapted for the VSCode Extension environment. The architecture ensures maximum scalability, strict separation of concerns, and future-proofing against changing AI APIs.

mermaid
graph TD
    A[VSCode Extension Host] --> B(Extension.ts: Activation/Commands);
    B --> C(AI Client Manager);
    C --> F[OpenAI/Gemini API Gateways];
    B --> D(UI/Webview Layer);
    D --> E(Webview Bundler - Vite/TSX);
    B --> G(Language Server Protocol Handler);
    G --> H(AST & Code Context Analyzer);

    subgraph Layers
        D -- Presentation --> B
        C -- External Adapters --> F
    end


### 📋 Table of Contents

1.  [Executive Summary (BLUF)](#-executive-summary-bluf)
2.  [Architecture and Structure](#-architecture-and-structure)
3.  [Installation and Setup](#-installation-and-setup)
4.  [Development and Scripts](#-development-and-scripts)
5.  [Core Development Principles](#-core-development-principles)
6.  [🤖 AI Agent Directives (System Prompt)](#-ai-agent-directives-system-prompt)

---

### ⚙️ Installation and Setup

This project uses `npm` for dependency management and requires Node.js (LTS).

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/CoderCopilot-AI-Code-Assistance-VSCode-Extension.git
    cd CoderCopilot-AI-Code-Assistance-VSCode-Extension
    

2.  **Install Dependencies:**
    bash
    npm install
    

3.  **Configure API Keys:**
    Create a `.env` file in the root directory and specify your AI API key:
    
    # Recommended: Use OpenAI or Gemini
    OPENAI_API_KEY="YOUR_SECRET_KEY"
    

4.  **Launch the Extension:**
    *   Press `F5` in VSCode to run the extension in a new Extension Development Host window.

### 💻 Development and Scripts

We enforce a strict development environment leveraging modern tooling for speed and reliability.

| Script Name | Command | Description |
| :--- | :--- | :--- |
| `start` | `npm run watch` | Watches source files and rebuilds extension (for F5 debugging). |
| `build` | `vsce package` | Packages the VSIX file for distribution. |
| `lint` | `biome lint --apply-unsafe src/` | Runs the Biome linter with auto-fixing enabled. |
| `format` | `biome format --write src/` | Applies standard formatting rules (Biome). |
| `test` | `npm run test:unit && npm run test:e2e` | Executes unit tests (Vitest) and end-to-end tests (Playwright). |
| `test:unit` | `vitest run` | Executes all isolated unit tests. |

### 🧭 Core Development Principles

1.  **TypeScript Strictness:** All code is written in Strict TypeScript mode. No implicit `any`. Interfaces and types must be explicitly defined for all data structures, especially API contracts.
2.  **SOLID:** Adhere to Single Responsibility, Open/Closed, Liskov, Interface Segregation, and Dependency Inversion principles in all class and module design.
3.  **DRY (Don't Repeat Yourself):** Abstract shared logic into reusable hooks, utilities, or services within the FSD `shared` layer.
4.  **Security First:** Never store sensitive data (like API keys) client-side or within the extension code. Utilize VSCode Secret Storage API for persistent, secure storage.

---

### 🤖 AI Agent Directives (System Prompt)

<details>
<summary>⚡️ **APEX ARCHITECT INSTRUCTION SET (FOR AUTOMATED DEVELOPMENT)** ⚡️</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** Senior Principal Software Architect operating with absolute precision.
**Context:** Current Date is **December 2025**. Building for the 2026 standard.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. PROJECT STACK & ARCHITECTURE ALIGNMENT
**Technology Stack:** TypeScript 5+, Node.js (LTS), VSCode Extension API, Vite/TSX (Webview Bundling).
**Architecture Pattern:** Feature-Sliced Design (FSD). Structure code by logical layers (App, Pages/Widgets, Features, Entities, Shared) ensuring strict import boundaries (Linter enforced).
**Core Tools:**
*   **Linter/Formatter:** **Biome** (Mandatory). High-speed analysis and aggressive formatting.
*   **Testing:** **Vitest** (Unit/Component), **Playwright** (E2E/VSCode Integration Tests).
*   **Package Management:** `npm`.

## 3. DEVELOPMENT STANDARDS & VERIFICATION
### A. Code Quality Mandates
1.  **TypeScript STRICT:** Enforce all strict flags (`"noImplicitAny": true`, `"strictNullChecks": true`, etc.).
2.  **API Resilience:** All external AI API calls (OpenAI/Gemini) must utilize robust caching mechanisms, exponential backoff, and circuit breakers implemented via service adapters (`src/entities/ai-adapters`).
3.  **VSCode API Use:** Utilize official VSCode APIs for commands, configuration, and state management. Never use undocumented internal VSCode features.
4.  **Webview Isolation:** Webview scripts MUST be strictly isolated (`sandbox`) and communicate solely through `acquireVsCodeApi()`.

### B. Verification Commands (For CI/CD Pipeline Alignment)
Execute these commands in sequence to verify code integrity:
bash
# 1. Clean install and build
npm ci
npm run build

# 2. Strict linting and formatting check
biome check --apply-unsafe --max-diagnostics=0 src/

# 3. Execute all unit and integration tests
npm run test


## 4. AI MODEL INTERACTION PROTOCOL
**Model Selection:** Default to `gemini-3-pro` or equivalent high-context model.
**Prompt Engineering:** Prompts must be version-controlled, explicit regarding desired output format (e.g., JSON schema, markdown), and include full surrounding code context (up to 4096 tokens) via the VSCode Document API.
**Cost Management:** Implement token usage tracking for every API call to minimize operational cost, exposing a dashboard in the extension settings.

</details>
# Contributing to SynthCode-AI-Code-Assistant-VSCode-Extension

Thank you for your interest in contributing to **SynthCode-AI-Code-Assistant-VSCode-Extension**! We aim to maintain a high-velocity, zero-defect, and future-proof codebase, reflecting the highest industry standards.

## 1. Code of Conduct

This project adheres to the [Contributor Covenant Code of Conduct](https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension/blob/main/CODE_OF_CONDUCT.md). By participating, you are expected to uphold its values.

## 2. Getting Started

### Prerequisites

*   **Node.js:** Version 20+ (LTS recommended)
*   **npm/Yarn/pnpm:** A modern package manager.
*   **VS Code:** Latest stable version.
*   **Git:** For version control.

### Setup

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension.git
    cd SynthCode-AI-Code-Assistant-VSCode-Extension
    

2.  **Install Dependencies:**
    bash
    npm install # or yarn install or pnpm install
    

3.  **Install VS Code Extension Dependencies:**
    VS Code extensions often require specific build tools and dependencies. Refer to the extension development documentation. For Vite-based TypeScript extensions, this typically involves:
    bash
    npm run compile # Or similar build script for VS Code extensions
    

4.  **Run in Development Mode:**
    To run the extension within a development VS Code instance:
    bash
    npm run dev # Or specific script for launching the extension host
    

## 3. Contribution Workflow

We follow a standard GitHub pull request workflow:

1.  **Fork the Repository:** Create your own fork of the `chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension` repository.
2.  **Create a Branch:** Create a descriptive branch for your feature or bug fix (e.g., `feature/add-new-completion-model` or `fix/incorrect-refactoring-suggestion`).
    bash
    git checkout -b my-branch-name
    
3.  **Make Your Changes:** Implement your changes, adhering to the project's coding standards.
4.  **Test Your Changes:** Ensure all existing tests pass and add new tests for your changes if applicable.
    bash
    npm test # Or relevant test script
    
5.  **Lint and Format:** Ensure your code adheres to the project's linting and formatting rules.
    bash
    npm run lint
    npm run format
    
6.  **Commit Your Changes:** Write clear and concise commit messages.
    bash
    git add .
    git commit -m "feat: Add new AI model for code completion"
    
7.  **Push to Your Fork:** Push your branch to your forked repository.
    bash
    git push origin my-branch-name
    
8.  **Open a Pull Request:** Submit a pull request from your branch to the `main` branch of the `chirag127/SynthCode-AI-Code-Assistant-VSCode-Extension` repository.

## 4. Coding Standards & Best Practices

*   **Language:** TypeScript (Strict mode is enforced).
*   **Linting & Formatting:** We use [Biome](https://biomejs.dev/) for ultra-fast linting and formatting. Ensure your code is formatted correctly before committing.
*   **Testing:** We utilize [Vitest](https://vitest.dev/) for unit tests and [Playwright](https://playwright.dev/) for end-to-end tests. Aim for comprehensive test coverage.
*   **Architecture:** Follow the principles of [Feature-Sliced Design (FSD)](https://feature-sliced.design/) where applicable for modularity and maintainability.
*   **AI Integration:** Ensure all AI interactions are robust, handle potential errors gracefully, and maintain clear API contracts with the AI service.
*   **VS Code Extension Best Practices:** Refer to the official [VS Code Extension API documentation](https://code.visualstudio.com/api) for guidance.
*   **SOLID Principles:** Adhere to SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) in your design.
*   **DRY (Don't Repeat Yourself):** Avoid redundant code.
*   **YAGNI (You Ain't Gonna Need It):** Only implement functionality that is currently required.

## 5. Reporting Issues

Before reporting a bug, please check if it has already been reported. If not, open a new issue with a clear title and a detailed description, including:

*   Steps to reproduce the bug.
*   Expected behavior.
*   Actual behavior.
*   Relevant environment details (VS Code version, OS, etc.).
*   Any relevant logs or error messages.

Use the provided issue templates in the `.github/ISSUE_TEMPLATE/` directory.

## 6. Feature Requests

For feature requests, please open a new issue and use the feature request template. Provide a clear explanation of the proposed feature and its benefits.

## 7. Pull Request Guidelines

*   **Small, Focused PRs:** Keep pull requests focused on a single concern (bug fix, feature implementation).
*   **Clear Descriptions:** Provide a comprehensive description of your changes in the pull request template.
*   **Link to Issues:** Reference any related issues using keywords like `Fixes #123` or `Closes #456` in your PR description.
*   **Code Reviews:** Be prepared to respond to feedback from reviewers and make necessary adjustments.

## 8. Project Structure Overview


SynthCode-AI-Code-Assistant-VSCode-Extension/
├── .github/                 # GitHub configuration (workflows, issue templates, etc.)
│   ├── ISSUE_TEMPLATE/
│   ├── workflows/           # CI/CD workflows
│   └── ...
├── src/                     # Source code
│   ├── extension.ts         # Extension entry point
│   ├── ai/                  # AI related services and models
│   ├── ui/                  # UI components and logic
│   ├── features/            # Domain-specific features (e.g., code completion, refactoring)
│   └── utils/               # Utility functions
├── test/                    # Unit and integration tests
├── .vscode/                 # VS Code specific settings
├── .gitignore
├── biome.json               # Biome configuration
├── package.json             # Project dependencies and scripts
├── tsconfig.json            # TypeScript configuration
└── README.md                # Project README


## 9. Questions?

If you have any questions, feel free to open an issue or reach out on the project's discussion forum (if available).

---
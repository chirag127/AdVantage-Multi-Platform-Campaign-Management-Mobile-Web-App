# AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App

AdVantage is a comprehensive, multi-platform mobile & web application for creating, managing, and tracking advertising campaigns across major social media and ad networks. It offers centralized dashboards, real-time analytics, and lead management for optimized marketing performance.

---

![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/ci.yml?style=flat-square)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square)
![Tech Stack](https://img.shields.io/badge/Tech%20Stack-React%2FRN%2C%20Node.js%2C%20MongoDB-blue?style=flat-square)
![Lint/Format](https://img.shields.io/badge/Lint%2FFormat-Biome-purple?style=flat-square)
![License](https://img.shields.io/github/license/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square)

---

## ✨ Features

*   **Cross-Platform Campaign Management:** Create, edit, and deploy campaigns on multiple ad networks from a single interface.
*   **Centralized Dashboard:** Monitor performance, budget, and key metrics across all your campaigns in real-time.
*   **Real-Time Analytics:** Access in-depth performance data with customizable reports and visualizations.
*   **Lead Management:** Track and manage leads generated from your campaigns directly within the app.
*   **JWT Authentication:** Secure user access and data management.
*   **API Integrations:** Seamlessly connect with major social media and ad platforms.

---

## 🚀 Architecture Overview

AdVantage employs a robust **Full-Stack JavaScript architecture**, leveraging modern frameworks and libraries to ensure scalability, maintainability, and a seamless user experience across both mobile and web platforms.

mermaid
graph TD
    A[Client (React Native / React Web)] --> B(API Gateway / Backend - Express.js);
    B --> C{Database - MongoDB};
    B --> D[Third-Party Ad Networks APIs];
    B --> E[Authentication Service - JWT];
    A -- JWT Token --> B;
    D -- Campaign Data --> B;
    B -- Analytics Data --> A;
    C -- Campaign & User Data --> B;


---

## 📚 Table of Contents

*   [Features](#features)
*   [Architecture Overview](#architecture-overview)
*   [AI Agent Directives](#_1-ai-agent-directives)
*   [Development Setup](#development-setup)
*   [Project Structure](#project-structure)
*   [Contributing](#contributing)
*   [License](#license)

---

<details>
  <summary>🤖 AI Agent Directives (December 2025 Edition)</summary>

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
**Directives:** Detect the project type (`package.json` for JavaScript/TypeScript) and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (JavaScript/TypeScript)**
    *   **Stack:** This project leverages **TypeScript 6.x** with **Strict Mode** enabled. The build tooling is handled by **Vite 7 (Rolldown)**. For native desktop applications, **Tauri v2.x** is the standard. For browser extensions, **WXT (Web Extension Tooling)** is employed. State management adheres to **Signals (Standardized)**.
    *   **Linting & Formatting:** **Biome** is the mandated tool for ultra-fast, unified linting and code formatting.
    *   **Testing:** **Vitest** is the standard for unit and component testing, integrated seamlessly with Vite. **Playwright** is utilized for end-to-end (E2E) testing.
    *   **Architecture:** Adheres to the **Feature-Sliced Design (FSD)** principles for modularity and maintainability, ensuring clear separation of concerns and promoting reusability.

*   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go) - *Not applicable for this project's primary function.***
    *   **Stack:** Rust (Cargo) or Go (Modules).
    *   **Lint:** Clippy / GolangCI-Lint.
    *   **Architecture:** Hexagonal Architecture (Ports & Adapters).

*   **TERTIARY SCENARIO C: DATA / AI / SCRIPTS (Python) - *Not applicable for this project's primary function.***
    *   **Stack:** uv (Manager), Ruff (Linter), Pytest (Test).
    *   **Architecture:** Modular Monolith or Microservices.

---

## 4. CODE INTEGRITY & VERIFICATION
*   **BUILD PROCESS:** All code must compile successfully using `npm run build` (or `yarn build`).
*   **TESTING PROTOCOL:**
    *   **Unit Tests:** Execute `npm test` (or `yarn test`) to run all Vitest unit tests. Aim for **90%+ code coverage**.
    *   **E2E Tests:** Execute `npm run test:e2e` (or `yarn test:e2e`) to run all Playwright end-to-end tests.
*   **LINTING & FORMATTING:**
    *   Run `npm run lint` (or `yarn lint`) to check for linting errors.
    *   Run `npm run format` (or `yarn format`) to automatically format code using Biome.
    *   **All code MUST pass linting and formatting checks before commit.**

---

## 5. COMMUNICATION & COLLABORATION
*   **PULL REQUESTS (PRs):**
    *   **Mandatory:** Use the `.github/PULL_REQUEST_TEMPLATE.md` for PR creation.
    *   **Policy:** All PRs require at least one approval from a core team member.
    *   **CI/CD:** Ensure all CI checks pass (see `.github/workflows/ci.yml`).
*   **ISSUES:**
    *   **Mandatory:** Use the `.github/ISSUE_TEMPLATE/bug_report.md` for bug reports.
    *   **Clarity:** All issues must be clearly defined with steps to reproduce, expected vs. actual results.

---

## 6. SECURITY & COMPLIANCE
*   **VULNERABILITY SCANNING:** Regular scans using `npm audit` or equivalent.
*   **SECRET MANAGEMENT:** **NEVER** commit secrets (API keys, passwords) directly to the repository. Use environment variables or secure secret management tools.
*   **DEPENDENCY MANAGEMENT:** Keep dependencies updated to their latest stable versions.
*   **LICENSE:** This project is licensed under **CC BY-NC 4.0**. See `LICENSE` file.
*   **SECURITY POLICY:** Review `.github/SECURITY.md` for detailed security guidelines.

---

## 7. ARCHITECTURAL PRINCIPLES
*   **SOLID:** Apply Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY:** Don't Repeat Yourself. Abstract common logic into reusable components or functions.
*   **YAGNI:** You Ain't Gonna Need It. Implement only necessary features; avoid premature optimization or over-engineering.
*   **FSD:** Adhere to Feature-Sliced Design for modularity and scalable architecture.

---

## 8. DEPLOYMENT & ENVIRONMENT
*   **STAGING:** Connected to a staging database and external services.
*   **PRODUCTION:** Connected to the live production database and external services.
*   **ENVIRONMENT VARIABLES:** Utilize `.env` files for local development and environment-specific configurations. DO NOT commit `.env` files.

---

## 9. TECHNOLOGY STACK DETAILS
*   **Frontend (Web):** React 19+, Vite 7, TypeScript 6.x, TailwindCSS v4
*   **Frontend (Mobile):** React Native 0.7x+, Vite 7, TypeScript 6.x
*   **Backend:** Node.js 20.x, Express.js 5.x
*   **Database:** MongoDB 7.x
*   **Authentication:** JWT
*   **Linting/Formatting:** Biome
*   **Testing:** Vitest (Unit), Playwright (E2E)
*   **CI/CD:** GitHub Actions

---

## 10. APEX COMMITMENT
As an Apex-level architect, you are committed to upholding these standards. Any deviation requires explicit justification and approval. The goal is Zero-Defect, High-Velocity, Future-Proof software delivery.

</details>

---

## 🛠️ Development Setup

### Prerequisites

*   Node.js (v18.x or later recommended)
*   npm (v9.x or later) or Yarn
*   MongoDB installed and running

### Installation

1.  **Clone the repository:**
    bash
    git clone git@github.com:chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App.git
    cd AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App
    

2.  **Install Node.js dependencies:**
    bash
    npm install
    # OR
    yarn install
    

3.  **Configure Environment Variables:**
    Create a `.env` file in the root directory based on the provided `.env.example` and fill in your specific credentials for MongoDB, JWT secrets, and any third-party API keys.
    bash
    cp .env.example .env
    # Edit .env file
    

---

## 📜 Scripts

| Script           | Description                                       |
| :--------------- | :------------------------------------------------ | 
| `npm run dev`    | Starts the development server (Web & Mobile)      |
| `npm run build`  | Builds the production-ready application           |
| `npm run lint`   | Runs Biome linter                                 |
| `npm run format` | Formats code with Biome                           |
| `npm test`       | Runs Vitest unit and integration tests            |
| `npm run test:e2e` | Runs Playwright end-to-end tests                  |

---

## 📁 Project Structure

AdVantage follows the Feature-Sliced Design (FSD) methodology for a clean and scalable architecture.


AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── PULL_REQUEST_TEMPLATE.md
│   ├── ci.yml
│   ├── CONTRIBUTING.md
│   └── SECURITY.md
├── .env.example
├── .gitignore
├── AGENTS.md
├── LICENSE
├── README.md
├── PROPOSED_README.md
├── badges.yml
├── biome.json
├── package.json
├── tsconfig.json
├── vite.config.ts
├── src/
│   ├── app/
│   │   ├── store/
│   │   ├── main.tsx
│   │   └── routes.tsx
│   ├── entities/
│   │   └── ... # Core business logic entities
│   ├── features/
│   │   └── ... # Independent features (e.g., Campaign Creation, Analytics Dashboard)
│   ├── pages/
│   │   └── ... # Page-level components
│   ├── processes/
│   │   └── ... # Cross-feature processes (e.g., User Onboarding)
│   ├── shared/
│   │   ├── ui/
│   │   ├── lib/
│   │   └── ... # Shared UI components, hooks, utilities
│   └── widgets/
│       └── ... # Structural widgets (e.g., Header, Sidebar)
├── mobile/
│   ├── App.tsx
│   ├── index.js
│   └── ... # React Native specific configurations
├── web/
│   ├── index.html
│   └── ... # Web specific configurations
└── ...


---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and ensure they adhere to the project's coding standards (linting, formatting, testing).
4.  Submit a Pull Request.

Please refer to `.github/CONTRIBUTING.md` for detailed guidelines.

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

See the `LICENSE` file for more details.

---

✨ **Star ⭐ this Repo if you find it useful!**
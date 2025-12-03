# AdVantage - Multi-Platform Campaign Management - SaaS Platform

[![GitHub Badge](https://img.shields.io/badge/Star%20%E2%AD%90-chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App-blue?style=flat-square&logo=github)](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App)

| Build Status | Code Coverage | Tech Stack | License |
| :---: | :---: | :---: | :---: |
| [![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/ci.yml?style=flat-square)](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/actions/workflows/ci.yml) | [![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square)](https://codecov.io/gh/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App) | [![JS](https://img.shields.io/badge/Language-JavaScript-E5A228?style=flat-square&logo=javascript)](https://www.javascript.com) | [![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](LICENSE) |

---

**AdVantage** is the unified, full-stack SaaS platform designed for enterprise-grade management of multi-channel advertising campaigns, providing real-time analytics and centralized lead tracking across web interfaces and native mobile applications.

This repository enforces **FAANG-level standards** for maintainability, performance, and scalability, leveraging a cohesive JavaScript ecosystem.

## 🏛️ Architecture Overview (2026 Standard)

The system follows a decoupled, service-oriented approach utilizing React/React Native for the frontend layers and Node.js/Express for the core API and business logic.

mermaid
graph TD
    subgraph Presentation Layer
        A[React Web Client] -->|REST/GraphQL| C
        B[React Native Mobile App] -->|REST/GraphQL| C
    end

    subgraph Backend (Node.js/Express)
        C(API Gateway / Auth Layer) --> D{Business Logic Services}
        D --> E[MongoDB Data Layer]
        D --> F[External Ad Network APIs]
    end

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#f9f,stroke:#333,stroke-width:2px
    style D fill:#ccf,stroke:#333,stroke-width:2px

    subgraph Integration
        F
    end


## 🗂️ Table of Contents
1. [AdVantage - Multi-Platform Campaign Management - SaaS Platform](#advantage---multi-platform-campaign-management---saas-platform)
2. [Architecture Overview (2026 Standard)](#-architecture-overview-2026-standard)
3. [Table of Contents](#-table-of-contents)
4. [Core Capabilities](#-core-capabilities)
5. [🤖 AI Agent Directives (Apex Protocol Adherence)](#-ai-agent-directives-apex-protocol-adherence)
6. [Development & Contribution Standards](#-development--contribution-standards)
    * [Prerequisites](#prerequisites)
    * [Setup Guide](#setup-guide)
    * [Execution Scripts](#execution-scripts)
7. [Security & Compliance](#security--compliance)

## ✨ Core Capabilities

*   **Unified Dashboard:** Single pane of glass for visualizing KPIs across Google Ads, Meta, etc.
*   **Real-Time Analytics:** Low-latency data streaming and aggregation powered by optimized MongoDB queries.
*   **Lead Tracking & Attribution:** Comprehensive lifecycle tracking from impression to conversion.
*   **Secure Access:** JWT-based authentication ensuring data integrity across all platforms.
*   **Cross-Platform UI:** Consistent experience delivered via React for web and React Native for mobile.

## 🤖 AI Agent Directives (Apex Protocol Adherence)

<details>
<summary>⚡ **Execute Apex Protocol v12.1 (JavaScript/Node.js Stack)**</summary>

This section mandates the operational parameters for any AI agent interacting with or modifying this repository.

### 1. Contextual Alignment
*   **Project Focus:** Full-Stack MarTech / AdTech SaaS Platform.
*   **Primary Languages:** JavaScript (ES2023+), TypeScript (for potential future tooling).
*   **Architecture Enforcement:** All new components **MUST** adhere to **Feature-Sliced Design (FSD)** principles within the frontend and **SOLID** principles (specifically Single Responsibility and Dependency Inversion) within the Node.js backend.
*   **Performance Mandate:** Prioritize non-blocking I/O patterns. All asynchronous operations must utilize modern `async/await` or Promises. **YAGNI** applies strictly to unnecessary abstractions.

### 2. Toolchain & Verification (Late 2025 Standard)
*   **Linting/Formatting:** Use **Biome** (`biome check`, `biome format`) exclusively for all JS/JSON artifacts to ensure speed and unified code style.
*   **Testing Frameworks:** **Vitest** for rapid unit testing; **Playwright** for robust E2E testing of the Web Client and critical API endpoints.
*   **Dependency Management:** npm/yarn with a strict lockfile policy enforced via CI.
*   **API Contracts:** Verify all interactions with external Ad Network APIs against established JSON Schemas defined in `/src/shared/contracts`.

### 3. Security Directives
*   **Authentication:** Validate all requests against the existing JWT middleware pattern (`/src/modules/auth`). Do not introduce direct credential storage.
*   **Injection Prevention:** Ensure input sanitization (using libraries like `dompurify` on the client side, or appropriate middleware on Express) before rendering or storing user-provided data.
*   **Data Handling:** All MongoDB interactions must be mediated through the official Mongoose layer to prevent Mongoose Denial of Service (DoS) vectors.

### 4. Verification Commands
To ensure compliance before submitting a change:
bash
# 1. Run Linter/Formatter Check
bio check --error-on-warnings

# 2. Run Unit Tests
npm test:unit

# 3. Run E2E Sanity Checks (Playwright)
npm test:e2e

</details>

## ⚙️ Development & Contribution Standards

### Prerequisites

Ensure you have the following tools installed globally:

1.  **Node.js:** Version 20.0+ (LTS recommended).
2.  **Git:** Version 2.30+.
3.  **Yarn/npm:** (Modern package manager).

### Setup Guide

Follow these steps to establish the local environment and synchronize the repository structure.

bash
# 1. Clone the repository
git clone https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App.git
cd AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App

# 2. Install dependencies (Monorepo structure assumed, adjust if necessary)
yarn install

# 3. Run initial Biome check to set up tooling
yarn lint

# 4. Start the Web Application development server
yarn dev:web


### Execution Scripts

| Script | Description | Target Platform |
| :--- | :--- | :--- |
| `yarn dev:web` | Starts the React Web development server. | Web |
| `yarn dev:mobile` | Builds and runs the React Native application (requires native tooling). | Mobile |
| `yarn start:api` | Launches the Node.js Express backend server. | Backend |
| `yarn test:unit` | Executes all Vitest unit tests across shared and feature modules. | All |
| `yarn test:e2e` | Runs end-to-end scenarios using Playwright against running services. | Web/API |
| `yarn build:prod` | Creates optimized, production-ready bundles for web and API. | Production |

## 🛡️ Security & Compliance

This project is governed by strict operational guidelines documented in the following files:

*   [SECURITY.md](./.github/SECURITY.md): Disclosure and vulnerability reporting policies.
*   [CONTRIBUTING.md](./.github/CONTRIBUTING.md): Code contribution requirements and PR workflow.
*   **License:** All contributions are governed by the **CC BY-NC 4.0 License** (Commercial use prohibited).

*We commit to maintaining a security-first posture in all MarTech integrations.*
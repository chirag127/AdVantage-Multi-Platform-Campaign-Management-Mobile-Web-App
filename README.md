# AdVantage: Multi-Platform Campaign Management Suite

[![Build Status](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/actions/workflows/ci.yml/badge.svg)](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/actions/workflows/ci.yml)
[![Code Coverage](https://codecov.io/gh/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/branch/main/graph/badge.svg)](https://codecov.io/gh/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App)
[![Language](https://img.shields.io/github/languages/top/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square&logo=javascript)](https://www.javascript.com/)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue?style=flat-square)](./LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App?style=flat-square&logo=github)](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/stargazers)

<a href="https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/stargazers"><img src="https://img.shields.io/badge/⭐-Star%20This%20Repo-blue?style=social&logo=star" alt="Star This Repo"></a>

AdVantage provides centralized control for omnichannel advertising, enabling marketers to seamlessly create, deploy, and track performance metrics for campaigns across mobile and web platforms from a unified dashboard. This full-stack application guarantees optimized marketing ROI through real-time insights and streamlined lead management.

## Architectural Blueprint

This system adheres to a robust Model-View-Controller (MVC) structure layered with modern API standards for separation of concerns between the React Native/React frontend and the scalable Express.js backend.

mermaid
graph TD
    subgraph Presentation Layer
        A[React Native Mobile] --> C(API Gateway: Express.js/REST)
        B[React Web Client] --> C
    end

    subgraph Application Layer
        C --> D{Business Logic / JWT Auth}
        D --> E[Campaign Service]
        D --> F[Analytics Service]
    end

    subgraph Data Layer
        E --> G[(MongoDB Cluster)]
        F --> G
        D --> H{External Ad Network APIs}
    end

    style C fill:#f9f,stroke:#333,stroke-width:2px
    style G fill:#ccf,stroke:#333,stroke-width:2px


## Table of Contents

1. [Architectural Blueprint](#architectural-blueprint)
2. [Features](#features)
3. [Apex Agent Directives](#-ai-agent-directives)
4. [Development Standards](#development-standards)
5. [Getting Started](#getting-started)
6. [License](#license)

## Features

*   **Unified Campaign Creation:** Single interface to configure ads for Facebook, Google Ads, and internal mobile channels.
*   **Real-Time Analytics Dashboard:** Aggregate performance metrics (CTR, CPL, Impressions) with dynamic charting.
*   **JWT Secure Authentication:** Robust, token-based security ensuring data integrity.
*   **Lead Management CRM:** Integrated module for tracking and qualifying leads generated from campaigns.
*   **Multi-Platform Delivery:** Simultaneous deployment targets for iOS/Android (via RN) and Desktop/Web (via React).

<details>
<summary><strong>🤖 AI Agent Directives (System Configuration)</strong></summary>

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
    *   **No Guessing:** Do not hallucinate APIs. Do not assume libraries.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends** (Focusing on React/React Native performance optimization).
    *   **Validation:** Use `docfork` to verify *every* external API signature (especially external Ad Network integrations).
    *   **Reasoning:** Engage `clear-thought-two` to architect complex state flows (e.g., async campaign synchronization) *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / MOBILE (Modern Frontend/Full-Stack)**
    *   **Stack:** This project leverages **TypeScript (Strict)** across the stack (Node.js backend, React Native/React frontend). Key tools include **Vite 7** (Frontend Bundling), **Biome** (Linter/Formatter), **Vitest** (Unit Testing), and **Playwright** (E2E Testing). The backend utilizes **Express.js** and **Mongoose/MongoDB**.
    *   **Architecture:** Adheres to **Feature-Sliced Design (FSD)** principles for frontend modularity and **SOLID** principles for backend service separation (Campaign, Analytics, User).
    *   **State Management:** Prioritize modern **Signals** patterns or ZUSTAND for predictable state flow. Minimize reliance on complex Redux patterns.
    *   **Security Focus:** Mandate strict input validation (Joi/Zod) for all API endpoints and ensure modern JWT refresh token strategies are implemented.

---

## 4. DEVELOPMENT & VERIFICATION
*   **GOAL:** Achieve Zero-Defect deployment for the next iteration.
*   **LINT/FORMAT:** All new/modified code must pass **Biome** checks without error. Enforce maximum strictness.
*   **UNIT TESTING:** Achieve minimum **85% code coverage** using **Vitest** for backend logic and critical frontend components.
*   **INTEGRATION TESTING:** Critical user journeys (Login, Campaign Creation, Analytics Load) must be covered by **Playwright** E2E tests.

</details>

## Development Standards

### Setup
bash
# 1. Clone Repository
git clone https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App.git
cd AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App

# 2. Initialize Dependencies (Backend/Web Root)
# Assuming npm/yarn/pnpm is used for the JS ecosystem
npm install

# 3. Database Setup (Requires local/cloud MongoDB instance)
# Refer to .github/SECURITY.md for secure connection string handling.

# 4. Start Backend API Server
npm run dev:server

# 5. Start Frontend (Mobile/Web will use proxy to connect)
npm run dev:web 
# Or for mobile development:
npm run dev:mobile


### Scripts
| Command | Target | Description |
| :--- | :--- | :--- |
| `npm run lint` | All | Run Biome analysis across the entire codebase. |
| `npm run test:unit` | All | Run Vitest unit tests. |
| `npm run test:e2e` | Web/Mobile | Execute Playwright integration tests for critical flows. |
| `npm run build:web` | Web | Production build for the web client. |
| `npm run build:mobile` | Mobile | Production build artifacts for React Native. |

### Core Principles
This project is built upon the principles of:
*   **SOLID:** Ensuring maintainable and adaptable object-oriented structure in the backend services.
*   **DRY (Don't Repeat Yourself):** Maximizing reusable components and shared logic, especially between web and mobile interfaces.
*   **YAGNI (You Aren't Gonna Need It):** Avoiding over-engineering by only implementing features required by the immediate business specification.

## License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License**. See the [LICENSE](./LICENSE) file for full details.

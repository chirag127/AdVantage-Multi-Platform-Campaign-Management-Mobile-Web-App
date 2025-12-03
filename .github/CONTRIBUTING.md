# Contributing to AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App

Thank you for considering contributing to **AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App**! We strive for a high-velocity, zero-defect, and future-proof development process.

## 1. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. Please ensure your contributions are respectful and inclusive.

## 2. Getting Started

To contribute, you'll need to set up your development environment.

### 2.1. Prerequisites

*   **Node.js:** Version 20.x or higher.
*   **npm:** Version 10.x or higher.
*   **Git:** Latest stable version.

### 2.2. Local Setup

1.  **Fork the Repository:** Click the "Fork" button on the repository page: [https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App](https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App)
2.  **Clone Your Fork:**
    bash
    git clone https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App.git
    cd AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App
    
3.  **Set Upstream Remote:** Link your fork to the original repository to fetch updates.
    bash
    git remote add upstream https://github.com/chirag127/AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App.git
    
4.  **Install Dependencies:**
    bash
    npm install
    

## 3. Development Workflow

We follow a standard Gitflow-like workflow:

1.  **Create a Branch:** Always create a new feature branch for your changes from the `main` branch.
    bash
    git checkout -b feat/your-feature-name main
    
    *(Use prefixes like `feat/`, `fix/`, `chore/`, `docs/`)*
2.  **Make Changes:** Implement your feature or fix.
3.  **Run Linters & Formatters:** Ensure your code adheres to our standards.
    bash
    npm run lint
    npm run format
    
    *Note: Our chosen stack uses Biome for linting and formatting. Refer to `.biome.json` for configuration.* Alternatively, if using older versions of the stack, `npm run lint` might trigger ESLint/Prettier.
4.  **Run Tests:** All tests must pass.
    bash
    npm run test
    
    *Note: Our chosen stack uses Vitest for unit tests and Playwright for E2E tests. Refer to `vitest.config.ts` and Playwright configuration.* Alternatively, if using older versions, `npm test` might trigger Jest.
5.  **Commit Changes:** Write clear and concise commit messages.
    bash
    git add .
    git commit -m "feat: Add user authentication module"
    
6.  **Push Changes:** Push your branch to your fork.
    bash
    git push origin feat/your-feature-name
    
7.  **Open a Pull Request:** Create a Pull Request from your feature branch to the `main` branch of the original repository.

## 4. Contributing Guidelines

*   **Code Quality:** Adhere to the principles of SOLID, DRY, and YAGNI. Write clean, maintainable, and well-documented code.
*   **TypeScript:** Use TypeScript with strict type checking enabled.
*   **Styling:** Utilize Tailwind CSS for styling. Ensure consistency and adherence to design patterns.
*   **Architecture:** Follow the Feature-Sliced Design (FSD) principles where applicable for frontend modules.
*   **Testing:** Write comprehensive unit and end-to-end tests for all new features and bug fixes.
*   **Documentation:** Update relevant documentation (e.g., README, component docs) as needed.

## 5. AI Agent Directives

This project integrates with AI agents for development assistance and code generation. Contributions should respect these directives:

*   **Agile Development:** Follow the core principles outlined in `.github/AGENTS.md`.
*   **Toolchain Alignment:** Ensure changes are compatible with the defined Apex Toolchain (TypeScript, Vite, TailwindCSS v4, Tauri v2, Biome, Vitest, Playwright).
*   **Verification:** Automated checks (CI pipeline) will verify adherence to these standards. Address any failures promptly.

## 6. Reporting Issues

Before reporting an issue, please check if it already exists. If not, open a new issue using the provided templates (`bug_report.md`). Provide detailed steps to reproduce the issue, expected behavior, and actual behavior.

## 7. Pull Request Process

All pull requests must:

*   Target the `main` branch.
*   Pass all CI checks.
*   Include a clear description of the changes.
*   Reference any related issues.

We aim for a quick review process. Automated checks will run on every PR.

## 8. Project Structure (High-Level Overview)

ascii
AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App/
├── public/
├── src/
│   ├── main/
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   └── [...] (Core app logic, routing)
│   ├── pages/
│   │   └── [...] (Page components)
│   ├── widgets/
│   │   └── [...] (Reusable UI widgets)
│   ├── features/
│   │   └── [...] (User-facing features, e.g., auth, campaign list)
│   ├── entities/
│   │   └── [...] (Core business logic, data models)
│   ├── shared/
│   │   ├── ui/ (Shared UI components)
│   │   ├── api/ (API client configuration)
│   │   └── lib/ (Utility functions)
│   └── [...] (Other FSD layers as needed)
├── vite.config.ts
├── tsconfig.json
├── package.json
├── .gitignore
├── README.md
└── [...] (Configuration files)


This structure encourages modularity and maintainability.

## 9. License

This project is licensed under the **CC BY-NC 4.0** license. See the `LICENSE` file for more details.


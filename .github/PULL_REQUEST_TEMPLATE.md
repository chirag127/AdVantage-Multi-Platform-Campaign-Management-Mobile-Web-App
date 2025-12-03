# 🚀 Pull Request Checklist & Review Guide

This template ensures all contributions adhere to Apex Technical Authority standards (Zero-Defect, High-Velocity, Future-Proof).

**Repository:** `AdVantage-Multi-Platform-Campaign-Management-Mobile-Web-App`
**New Name/Context:** This PR pertains to the unified AdTech platform for Web/Mobile.

---

## 🎯 Summary of Changes

<!-- Briefly describe the core purpose of this PR. What feature/fix does it address? Link to the relevant issue using `Fixes #XXX` or `Relates to #YYY`. -->

## ✅ Pre-flight Checklist (Self-Review)

Before submitting, ensure you have verified the following:

### Code Quality & Architecture

- [ ] **SOLID Principles:** Is the code adhering to Single Responsibility and Open/Closed principles?
- [ ] **DRY:** Have duplicate logic blocks been refactored into shared components/utilities?
- [ ] **Type Safety:** (If applicable to React/TSX files) Are all interfaces and types rigorously defined and utilized? (For this JS/React context, are JSDoc/TS-like annotations used for clarity?)
- [ ] **YAGNI Check:** Have you avoided over-engineering for hypothetical future requirements?
- [ ] **Security Review:** Were any new dependencies added? If so, were they vetted against current industry standards (via `linkup`)? Are JWT/API keys handled securely (no hardcoding)?

### Testing & Verification

- [ ] **Unit Tests:** Have new features been covered by unit tests (Vitest/Jest equivalent)? (Target >85% coverage)
- [ ] **Integration Tests:** Are critical data flows (e.g., API handshake, Auth) covered by integration tests?
- [ ] **Manual Verification:** Have you manually tested the feature end-to-end on both simulated **Web (React)** and **Mobile (React Native)** contexts?

### Documentation & Metadata

- [ ] **README Updated:** If this introduces a major feature or changes the stack, is `README.md` updated?
- [ ] **Badges:** If build or coverage is affected, is the status likely to pass?
- [ ] **Dependencies:** Are `package.json` / lock files updated correctly?

---

## 📝 Detailed Changes

<!-- Use this section to detail complex changes, architectural shifts, or specific integration points (e.g., new Ad Network API integration). -->

### Frontend / UI Changes (React/React Native)

- 

### Backend / API Changes (Node.js/Express)

- 

### Data Layer Changes (MongoDB)

- 

---

## 🧑‍💻 Reviewer Focus Areas

<!-- Guide the reviewer to the most critical or complex parts of the change. -->

1.  **Performance Bottlenecks:** Please scrutinize the `AnalyticsService.js` logic for potential N+1 query issues in MongoDB aggregation.
2.  **State Management:** Review the hook usage in `CampaignEditor.tsx` for correct lifecycle management.

---

**By submitting this PR, I affirm that this contribution meets the standards outlined by the Apex Technical Authority.**
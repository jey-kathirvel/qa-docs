# Sprint Test Plan

## 1. Sprint Overview

- **Sprint:** Sprint 21  
- **Duration:** 2026‑05‑18 → 2026‑06‑01  
- **Team:** Jeyendran (QA), Dev Team, Scrum Master, Product Owner  
- **Objective:**  
  Validate all user stories, bug fixes, and performance improvements planned for this sprint against defined acceptance criteria and non‑functional requirements.

---

## 2. Scope of Testing

### 2.1 In Scope

- New user stories developed in this sprint (refer to Jira: `Sprint 21`).  
- Regression of core flows impacted by new changes (e.g., login, checkout, profile update).  
- API and UI regressions on supported browsers/devices.  
- Critical bug fixes labeled “P0” / “P1”.

### 2.2 Out of Scope

- Features not committed to this sprint.  
- Non‑critical UI polish items not linked to acceptance criteria.  
- Performance/load testing beyond smoke‑level throughput checks.

---

## 3. Test Approach

- **Manual Testing:**  
  - Functional test cases mapped to each user story.  
  - Regression suites executed via manual scripts.  
- **Automation:**  
  - Smoke tests executed nightly / pre‑deploy.  
  - Regression automation runs triggered on `develop` and `release` branches.
- **Exploratory Testing:**  
  - 1–2 hours per tester allocated for exploratory testing of high‑risk areas.  
- **Security/Compatibility:**  
  - Security‑related checks (e.g., auth, input validation) included in all test cycles.  
  - Browser/device matrix: Chrome, Firefox, Safari, Edge (latest); mobile: Android / iOS via emulators or real devices.

---

## 4. Test Environment & Data

- **Staging Environment:**  
  - URL: `https://staging.example.com`  
  - DB: Snapshot refreshed weekly from production‑anonymized data.  
- **Test Data:**  
  - Pre‑seeded accounts for different user roles (admin, user, guest).  
  - Synthetic datasets for edge‑case scenarios (empty cart, invalid promo codes, etc.).  
- **Dependencies:**  
  - Third‑party APIs mocked where needed using feature toggles or stubs.

---

## 5. Test Design & Execution

### 5.1 Test Types

| Test Type        | Purpose |
|------------------|---------|
| Smoke            | Verify basic functionality post‑deploy. |
| Functional       | Validate each story against acceptance criteria. |
| Regression       | Ensure existing features still work. |
| Integration      | Validate API‑to‑service & service‑to‑service flows. |
| Compatibility    | Cross‑browser / cross‑device checks. |

### 5.2 Test Case Structure

Each test case includes:

- **Title:** Clear description of the scenario.  
- **Pre‑conditions:** What must be true before execution.  
- **Steps:** Numbered actions.  
- **Expected Result:** What the system should do.  
- **Priority:** P0 (critical), P1 (high), P2 (medium), P3 (low).  

Example (inline table):

| # | Test Type   | User Story Key | Description |
|---|------------|----------------|-------------|
| 1 | Functional | US‑123         | Login with valid credentials redirects to dashboard. |
| 2 | Regression | US‑456         | Existing cart items persist after logout → login. |

---

## 6. Roles & Responsibilities

| Role            | Responsibilities |
|-----------------|------------------|
| QA Lead         | Define test strategy, review test cases, track coverage and defects. |
| Testers         | Execute test cases, log defects, update test results. |
| Developers      | Fix bugs, provide repro steps, confirm fixes. |
| Product Owner   | Clarify acceptance criteria and priorities. |
| Scrum Master    | Unblock impediments related to test environment or data. |

---

## 7. Entry & Exit Criteria

### 7.1 Entry Criteria

- All planned stories are marked “Ready for Testing” in Jira.  
- Build is deployed to the staging environment.  
- Smoke tests pass on the latest build.

### 7.2 Exit Criteria

- All P0 and P1 test cases pass or have approved waivers.  
- No unresolved P0/P1 defects in Jira.  
- Regression coverage ≥ 90% of impacted features.  
- Test summary report shared with stakeholders.

---

## 8. Schedule & Milestones

| Milestone                  | Date Range       |
|----------------------------|------------------|
| Test Planning              | 2026‑05‑18–19    |
| Test Design & Scripting    | 2026‑05‑20–22    |
| Test Execution (Phase 1)   | 2026‑05‑23–26    |
| Bugs Triage & Retest       | 2026‑05‑27–28    |
| Sign‑off & Report Ready    | 2026‑05‑31       |
| Sprint Review & Demo       | 2026‑06‑01       |

---

## 9. Defect Management

- **Tool:** Jira (Project `QA‑INFRA`).  
- **Fields:** Priority (P0–P3), Severity, Module, Environment, Steps to Reproduce, Screenshots/Logs.  
- **Triage:**  
  - Daily stand‑up triage for critical defects.  
  - P0/P1 defects must be confirmed within 2 hours and fixed before next build.  
- **Re‑testing:**  
  - QA re‑tests each defect in the same environment where it was reported.

---

## 10. Risks & Mitigation

| Risk                                | Mitigation |
|-------------------------------------|------------|
| Delay in build availability         | Communicate early with Dev; parallelize test‑case review. |
| Unstable test environment           | Maintain a backup staging instance; escalate to infra. |
| Insufficient test data              | Coordinate with PO/Dev to pre‑seed data before sprint start. |
| High volume of P0/P1 defects        | Adjust scope with PO; log only validated issues. |

---

## 11. Deliverables

- Test plan document (this file).  
- Test case repository (Markdown or Test‑management tool).  
- Test execution report (XLS/CSV or dashboard).  
- Defect summary slide for sprint review.

---

## 12. Notes & References

- Jira Board: `https://your‑jira.com/projects/PROJ/boards/1`  
- Test Cases Repo: `https://github.com/your‑org/test‑cases`  
- Confluence: `https://your‑wiki.com/spaces/TEST/pages/212345`

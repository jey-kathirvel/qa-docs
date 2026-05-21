# Regression Testing Checklist

Use this checklist to verify that existing functionality still works after new changes or bug fixes.

---

## 1. Planning & Scope

- [ ] Identify impacted modules based on code changes (impact analysis). [web:160][web:165]  
- [ ] Define scope: critical paths, high‑risk areas, and recently modified flows. [web:162][web:165]  
- [ ] Decide which tests will be automated vs manual (e.g., automate critical paths). [web:165][web:166]  
- [ ] List required test data and environments (staging, UAT, production‑like). [web:159][web:165]  

---

## 2. Test Case Preparation

- [ ] Identify and select test cases for regression (smoke, core flows, integration points). [web:162][web:163]  
- [ ] Prioritize test cases: critical flows first, then high‑risk, then low‑risk. [web:160][web:165]  
- [ ] Update or remove obsolete test cases (deprecated features, removed flows). [web:163][web:165]  
- [ ] Add new test cases for recently introduced features that are now part of baseline. [web:160][web:165]  

---

## 3. Data & Environment Setup

- [ ] Prepare or refresh test data for key flows (e.g., user accounts, products, orders). [web:159][web:161]  
- [ ] Ensure environments are stable and match production configuration. [web:159][web:165]  
- [ ] Verify databases, caches, and 3rd‑party services are ready before test execution. [web:159][web:166]  
- [ ] Check that configuration flags and feature toggles are set correctly. [web:160][web:165]  

---

## 4. Execution Strategy

- [ ] Run **smoke / sanity tests** first to confirm basic health of the build. [web:162][web:165]  
- [ ] Execute **critical‑path tests** (e.g., login, search, checkout, payment) before niche flows. [web:160][web:164]  
- [ ] Run **automated regression packs** (e.g., nightly / pre‑deploy suites). [web:165][web:166]  
- [ ] Perform **manual exploratory checks** around recently changed areas. [web:163][web:166]  

---

## 5. Functional Regression Checks

- [ ] Core business flows still work end‑to‑end without errors. [web:161][web:164]  
- [ ] Integration points (e.g., REST APIs, 3rd‑party services) still behave as expected. [web:161][web:166]  
- [ ] Database changes do not break referential integrity or data consistency. [web:159][web:167]  
- [ ] Reports, exports, and search filters return correct data counts and values. [web:161][web:164]  

---

## 6. Cross‑Quality Checks

- [ ] UI/UX has not regressed (no broken layouts, missing icons, or confusing text). [web:159][web:162]  
- [ ] Performance and loading times are within acceptable limits after changes. [web:162][web:165]  
- [ ] Cross‑browser / cross‑device behavior is consistent. [web:161][web:164]  
- [ ] Security and access controls still work (no unauthorized access or privilege escalation). [web:162][web:165]  

---

## 7. Results, Defects & Retest

- [ ] 100% of planned regression tests have been executed. [web:159][web:162]  
- [ ] All test results (pass/fail) are recorded in the test‑management tool. [web:162][web:166]  
- [ ] Open critical / high‑severity defects are logged and prioritized. [web:159][web:165]  
- [ ] Retest fixed defects thoroughly and confirm they do not introduce new issues. [web:163][web:165]  

---

## 8. Closure & Reporting

- [ ] Verify that all acceptance criteria for the release are met. [web:165][web:166]  
- [ ] Prepare a regression test summary report (scope, coverage, pass/fail, open issues). [web:161][web:165]  
- [ ] Share sign‑off status with stakeholders (Ready / Not Ready for release). [web:165][web:166]  
- [ ] Review and refine the regression test suite for future sprints. [web:163][web:165]  

---

## 9. Regression Testing Status Table (Optional)

Example table to track per module:

| Module / Feature        | Test Case Count | Executed | Passed | Failed | Notes |
|-------------------------|-----------------|----------|--------|--------|-------|
| Login & Auth            | 15              | 15       | 14     | 1      | [e.g., “P1 bug logged; retest planned”] |
| Product Search          | 20              | 

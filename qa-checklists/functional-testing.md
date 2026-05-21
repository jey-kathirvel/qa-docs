# Functional Testing Checklist

Use this checklist during functional test execution for each feature / module.

---

## 1. Requirements & Acceptance Criteria

- [ ] Verified against user story / requirement document.  
- [ ] Acceptance criteria are fully implemented and testable.  
- [ ] No assumptions are made; unclear points are clarified with PO / BA.  

---

## 2. Basic UI & Navigation

- [ ] All links, buttons, icons, and menus open the correct page / flow.  
- [ ] Navigation (back/forward, breadcrumbs, side menu) works as expected.  
- [ ] Active page / section is visually distinguishable (e.g., selected tab highlight).  

---

## 3. Form & Field Validation

- [ ] Mandatory fields are clearly marked.  
- [ ] Empty mandatory fields show appropriate error messages.  
- [ ] Fields accept only valid data types (e.g., digits in phone, email format).  
- [ ] Length limits, character constraints, and formatting are enforced.  
- [ ] Error messages are clear, specific, and user‑friendly.  

---

## 4. Happy‑Path Scenarios

- [ ] Main success flow completes end‑to‑end without errors.  
- [ ] Success confirmation (message, page, status change) is shown.  
- [ ] Data is correctly saved / updated in the backend.  
- [ ] UI reflects the latest state after the action.  

---

## 5. Edge & Negative Cases

- [ ] Boundary values are tested (e.g., min / max, empty, null).  
- [ ] Invalid inputs are handled with proper validation / UI feedback.  
- [ ] API / backend errors are gracefully shown to the user.  
- [ ] Timeouts, rate limits, and session expirations behave as expected.  

---

## 6. Search, Sort, Filter & Pagination

- [ ] Search returns correct results for different keywords.  
- [ ] Filters apply accurately and update the result list.  
- [ ] Sorting (ascending / descending) works on key columns.  
- [ ] Pagination: Next / Previous / Page number navigation works correctly.  

---

## 7. File Upload / Download

- [ ] File upload shows progress / status.  
- [ ] File type and size limits are enforced with clear messages.  
- [ ] Invalid files (wrong type / size) are rejected.  
- [ ] Download links open the correct file / trigger download as expected.  

---

## 8. Session, Login & Security Basics

- [ ] Login / logout works correctly with valid and invalid credentials.  
- [ ] Session timeout redirects to login / shows message when expired.  
- [ ] Protected pages redirect or block un‑authorized access.  
- [ ] Sensitive data (password, tokens) is not exposed in UI / logs.  

---

## 9. Integration & API Backing UI

- [ ] UI calls correct APIs and handles 2xx, 4xx, 5xx responses.  
- [ ] Data shown in UI matches what is returned by the API.  
- [ ] Loading states / spinners are shown during API calls.  
- [ ] UI recovers gracefully after failed or slow API responses.  

---

## 10. Regression & Cross‑Flow Checks

- [ ] Existing, related features still work after new changes.  
- [ ] Critical user journeys (e.g., signup → login → use core feature) are verified.  
- [ ] Data consistency is maintained across pages and workflows.  

---

## 11. Defect Logging & Status

- [ ] Each defect includes clear steps, expected vs actual behavior.  
- [ ] Environment, browser / device, and build version are documented.  
- [ ] Screenshots / screen recordings are attached where helpful.  
- [ ] Priority (P0–P3) and impact are correctly set.  

---

## 12. Checklist Status per Feature

Example table to track coverage per module:

| Feature              | Happy Path | Edge Cases | Validation | Regression | Notes |
|----------------------|-----------|-----------|-----------|-----------|-------|
| User Registration    | ✅        | ✅        | ✅        | ✅        | [e.g., “All flows pass”] |
| Product Search       | ✅        | ⏳        | ✅        | ✅        | [e.g., “Edge case not yet covered”] |
| Checkout Flow        | ✅        | ✅        | ✅        | ✅        | [e.g., “Production‑ready”] |


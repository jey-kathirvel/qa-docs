# User Story Validation Checklist

This checklist helps QA and the team verify that a user story is clear, testable, and ready for implementation.

---

## 1. Story Format

- [ ] Follows the **“As a… I want… so that…”** format. [web:51][web:56]  
- [ ] Title is short and descriptive (fits on an index card / Jira issue). [web:51][web:59]  
- [ ] Description is non‑technical and written from the **user’s perspective**. [web:51][web:56]  

---

## 2. Scope & Size

- [ ] Scope is **small enough** to fit in one sprint (INVEST: Independent, Negotiable, Valuable, Estimable, Small, Testable). [web:51][web:55]  
- [ ] If too large, it is **split into smaller stories** with clear boundaries. [web:51][web:58]  
- [ ] The story does **not mix multiple unrelated features**. [web:55][web:58]  

---

## 3. Value & Context

- [ ] It clearly states **who** the user is (role, persona). [web:51][web:56]  
- [ ] It explains **what** they want and **why** (business value / benefit). [web:51][web:55]  
- [ ] The value is **measurable or observable** (e.g., “reduce errors”, “improve conversion”). [web:55][web:60]  

---

## 4. Acceptance Criteria

- [ ] Acceptance criteria are **listed explicitly** (not only in comments). [web:52][web:55]  
- [ ] Each criterion is **clear, specific, and testable**. [web:52][web:55]  
- [ ] Includes **happy path**, **edge cases**, and **error scenarios**. [web:52][web:58]  
- [ ] Criteria cover **validations, constraints, and business rules** (e.g., required fields, error messages). [web:51][web:58]  

---

## 5. Testability & Confirmation

- [ ] QA can **design concrete test cases** from the acceptance criteria. [web:52][web:55]  
- [ ] Expected behavior and outputs are **specified** (e.g., “show success toast”, “log event”). [web:52][web:56]  
- [ ] Performance or non‑functional expectations are noted if relevant (e.g., “response < 2s under normal load”). [web:55][web:60]  

---

## 6. Dependencies & Environment

- [ ] All **dependencies** (other stories, APIs, teams) are identified. [web:51][web:55]  
- [ ] Target **environment / channel** is specified (e.g., web, mobile app, admin panel). [web:56][web:59]  
- [ ] Any **test‑data requirements** are mentioned (e.g., “user must have an active subscription”). [web:55][web:60]  

---

## 7. Overall “Ready” Status

Use this table to mark if the story is ready for implementation:

| Item | Status |
|------|--------|
| Format correct (As‑a‑I‑want‑so‑that) | ✅ / ❌ |
| Clear value and user role | ✅ / ❌ |
| Small enough for one sprint | ✅ / ❌ |
| Acceptance criteria defined and testable | ✅ / ❌ |
| Dependencies and data documented | ✅ / ❌ |
| **Overall** | ✅ (**Story is Ready**) / ❌ (Needs refinement) |

---

## 8. Notes

- Keep this checklist visible during **Backlog Refinement** and **Sprint Planning**.  
- Adapt it to your **product type** (web, mobile, API) and **QA workflow** (manual vs automation focus).  

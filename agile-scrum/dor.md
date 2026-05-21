# Definition of Ready (DoR)

## 1. What is Definition of Ready?

- The **Definition of Ready (DoR)** is a checklist that defines when a **backlog item** (e.g., user story, bug, task) is clear enough to be **pulled into a sprint** and worked on. [web:31][web:32]  
- It acts as an **“entry gate”** before implementation begins, while the Definition of Done (DoD) is the **“exit gate.”** [web:34][web:38]  

---

## 2. Purpose

- Prevents starting work on **vague or incomplete** items. [web:31][web:40]  
- Reduces mid‑sprint surprises and rework by ensuring shared understanding before commitment. [web:32][web:40]  

---

## 3. Sample DoR Checklist (User Story)

A backlog item is considered **Ready** only if all the following criteria are met. [web:31][web:32][web:33]

- [ ] User story has clear **title and description**.  
- [ ] User story clearly states **who** it is for and **what value** it delivers.  
- [ ] User story is **small enough to fit within one sprint** (or is broken into smaller slices).  
- [ ] User story is **well estimated** by the delivery team (e.g., story points or time).  
- [ ] **Acceptance criteria** are written, clear, and testable.  
- [ ] Expected **inputs, outputs, and edge cases** are described (where relevant).  
- [ ] **Dependencies** on other stories, teams, or systems are identified and planned.  
- [ ] **UX/UI mocks or wireframes** are available and linked (if applicable).  
- [ ] **Performance or non‑functional criteria** are defined (if relevant, e.g., response time, load).  
- [ ] **Person who will accept** the story (PO / stakeholder) is known.  
- [ ] Story is **prioritized** in the backlog and assigned to the target sprint.  

---

## 4. Example DoR Table

| Criterion                                   | Status |
|--------------------------------------------|--------|
| Clear title and description                | ✅     |
| Business value explained                   | ✅     |
| Small enough for one sprint                | ✅     |
| Estimated by team                          | ✅     |
| Acceptance criteria defined and testable   | ✅     |
| Dependencies identified                    | ✅     |
| UX mock / wireframe linked                 | ✅     |
| **Overall**                                | ✅ (**Story is Ready** / ❌ Not Ready) |

---

## 5. DoR for Bugs / Tasks

For **bugs or technical tasks**, consider adding: [web:33][web:40]

- [ ] Clear **repro steps** and environment details.  
- [ ] **Expected vs actual behavior** described.  
- [ ] **Priority and severity** set (e.g., P0, P1).  
- [ ] Any **related user stories** or technical components documented.  

---

## 6. How to Use the DoR

- During **Backlog Refinement** and **Sprint Planning**, the team verifies that each item meets the DoR. [web:32][web:38]  
- If an item is **not Ready**, it is **kept in the backlog** for further refinement and not pulled into the sprint. [web:31][web:40]  
- The DoR can be **updated** by the team in Retrospectives as processes mature.  

---

## 7. Notes

- Adapt this checklist to your **product type** (web, mobile, API, internal tools) and **team size / workflow**.  
- Keep it visible in Jira, Confluence, or your Scrum board so the PO and team can refer to it before sprint planning.  

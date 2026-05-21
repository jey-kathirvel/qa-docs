# Definition of Done (DoD)

## 1. What is Definition of Done?

- The **Definition of Done (DoD)** is a shared checklist that defines what it means for a backlog item (e.g., user story, task) to be truly **complete** and ready as part of a potentially shippable product increment. [web:23][web:27]  
- It is agreed upon by the **entire Scrum / Agile team** (Dev, QA, PO, etc.) and applied consistently to every item. [web:27][web:29]  

---

## 2. Purpose

- Avoid ambiguity between “done coding” and “done delivering.” [web:27][web:30]  
- Ensure that only **truly finished** work is counted in velocity or released to users. [web:23][web:29]  

---

## 3. Generic DoD Checklist

A typical DoD for a software team might include: [web:23][web:29][web:30]

- [ ] Code is written and merged to the main / release branch.  
- [ ] Code has been peer‑reviewed (pull request / merge request approved).  
- [ ] All unit tests pass with sufficient coverage.  
- [ ] All automated integration tests pass.  
- [ ] Smoke / regression automated tests pass.  
- [ ] Manual testing is complete for the feature and impacted areas.  
- [ ] No known **P0 / P1 defects** linked to this item.  
- [ ] UI / UX changes are validated across supported browsers or devices.  
- [ ] API contracts (if any) are updated and documented.  
- [ ] User‑facing documentation or release notes are updated.  
- [ ] The feature is deployable to a production‑like environment.  

---

## 4. How to use the DoD

- At the end of development, the team **checks each item against the DoD**.  
- If any criterion is **not met**, the item is **not considered “Done”** and should not be included in the sprint’s delivered scope. [web:23][web:27]  
- The DoD evolves over time; the team can refine it during **Sprint Retrospectives**. [web:29][web:30]  

---

## 5. Example per User Story

| Item | Done? |
|------|-------|
| Code implemented | ✅ |
| PR approved | ✅ |
| Unit tests pass | ✅ |
| Manual test execution passed | ✅ |
| No P0/P1 defects | ✅ |
| **Overall** | ✅ (Story is Done) |

---

## 6. Notes

- Customize this checklist for your **product type** (web, mobile, API, etc.) and **team workflow**.  
- Keep it visible in your Scrum board, Jira, or Confluence so everyone can refer to it daily.

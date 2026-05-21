# Sprint Retrospective – QA Notes

## 1. Sprint Overview

- **Project:** [Project Name]  
- **Sprint:** [Sprint 21]  
- **Dates:** [2026‑05‑18 → 2026‑06‑01]  
- **QA Facilitator:** Jeyendran  
- **Attendees:** [QA, Dev, PO, Scrum Master, etc.]

---

## 2. What Went Well (QA)

- All critical user stories were tested before the last day of the sprint.  
- Smoke tests on staging passed after each deployment, reducing last‑minute surprises.  
- Defect triage was quick; P0/P1 issues were clearly labeled and prioritized.  
- Exploratory testing uncovered edge‑case issues before UAT.  
- Test cases were updated and documented in the shared repo.

---

## 3. What Could Be Improved (QA)

- Some stories were marked “Ready for Testing” but were still incomplete or unstable.  
- Late builds delayed full regression execution in the second half of the sprint.  
- A few test environments were unstable or lacked required test data.  
- Manual test coverage was limited for some low‑priority but high‑impact flows.  
- Defects were sometimes logged with incomplete steps or screenshots.

---

## 4. Action Items (QA Focus)

| Action Item                                                | Owner     | Target Date | Status |
|-----------------------------------------------------------|-----------|-------------|--------|
| Add a “QA Ready” checklist in Jira (acceptance criteria, test data, env details). | QA + PO   | [Next sprint planning] | ✅ / ⏳ |
| Coordinate with Dev to ensure builds are stable by mid‑sprint for full regression. | QA Lead   | [Next sprint] | ✅ / ⏳ |
| Document and share a test‑data setup guide for each module. | QA        | [2026‑05‑25] | ✅ / ⏳ |
| Review and improve defect logging guidelines (steps, screenshots, environment). | QA Lead   | [Ongoing] | ✅ / ⏳ |
| Define a minimal critical‑flow regression suite to run in every sprint. | Dev + QA  | [Next sprint] | ✅ / ⏳ |

---

## 5. Open Questions / Puzzles

- How can QA get more visibility into mid‑sprint changes that impact existing flows?  
- Can we automate at least 70% of our smoke tests by the next release?  
- Should we introduce a short QA / Dev sync after story completion (not just before testing)?

---

## 6. Shoutouts

- [Name] for consistently providing clear repro steps and logs.  
- [Name] for helping stabilize the staging environment.  
- [Name] for adding QA feedback directly in PRs during code review.

---

## 7. Notes & References

- Jira Board: [Link]  
- Test Cases Repo: [Link]  
- Previous Sprint Retrospective: [Link]

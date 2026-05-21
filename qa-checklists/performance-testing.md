# Performance Testing Checklist

Use this checklist to plan, run, and analyze performance/load/stress tests.

---

## 1. Planning & Scope

- [ ] Define clear goals (e.g., max response time, throughput, concurrency). [web:151][web:156]  
- [ ] Identify critical user journeys and high‑traffic paths (e.g., login, search, checkout). [web:151][web:158]  
- [ ] Decide on test types: load, stress, endurance, spike, and volume testing. [web:151][web:153]  
- [ ] Document expected KPIs (e.g., 95% response time < 2s, 1000 RPS). [web:149][web:151]  

---

## 2. Environment & Data

- [ ] Test environment mirrors production as closely as possible (hardware, OS, network). [web:149][web:152]  
- [ ] Test data size and distribution match production (e.g., user count, records in DB). [web:149][web:156]  
- [ ] All services (web, app, DB, caches, 3rd‑party APIs) are up and stable before the test. [web:149][web:155]  
- [ ] Test scripts and data files (e.g., CSV) are prepared and version‑controlled. [web:155][web:158]  

---

## 3. Script & Scenario Design

- [ ] Scripts model real user behavior (think time, navigation patterns, pause between steps). [web:151][web:158]  
- [ ] All critical business flows (e.g., login → browse → add to cart → checkout) are scripted. [web:151][web:156]  
- [ ] Dynamic values (tokens, session IDs, form keys) are properly extracted and correlated. [web:155][web:158]  
- [ ] Scripts include assertions to validate correct responses (e.g., status 200, success text). [web:155][web:158]  

---

## 4. Test Execution

- [ ] Run a **baseline** test with low load to confirm script and environment stability. [web:151][web:155]  
- [ ] Gradually increase virtual users (ramp‑up) to avoid overloading the system too fast. [web:149][web:151]  
- [ ] Run tests for multiple load levels (normal, peak, above‑peak, stress). [web:151][web:153]  
- [ ] Capture logs, metrics, and screenshots for any failures or errors. [web:152][web:154]  

---

## 5. Metrics & Monitoring

- [ ] Monitor key performance metrics:  
  - Response time (avg, 90th, 95th percentiles).  
  - Throughput (requests/transactions per second).  
  - Error rate (%) and failed transactions. [web:149][web:154]  
- [ ] Monitor server‑level KPIs: CPU, memory, disk I/O, network bandwidth. [web:149][web:154]  
- [ ] Monitor application and database metrics (e.g., DB connections, query performance). [web:154][web:156]  
- [ ] Check for bottlenecks (e.g., slow queries, thread‑pool exhaustion, GC pressure). [web:154][web:151]  

---

## 6. Post‑Execution Analysis

- [ ] Compare results against defined KPIs and acceptance criteria. [web:151][web:158]  
- [ ] Identify root causes of slow responses (e.g., DB, caching, 3rd‑party API). [web:154][web:156]  
- [ ] Check for memory leaks, resource exhaustion, or configuration issues. [web:149][web:152]  
- [ ] Document findings, including graphs, logs, and recommended optimizations. [web:151][web:158]  

---

## 7. Performance Testing Status Table (Optional)

Example table to track coverage:

| Test Type      | Scope / Flow              | Target Users | Success Criteria Met | Notes |
|----------------|---------------------------|--------------|----------------------|-------|
| Load Test      | Login & Checkout          | 500          | ✅                   | [e.g., “All KPIs within limits”] |
| Stress Test    | High‑load search          | 2000         | ❌                   | [e.g., “DB CPU maxing out; need tuning”] |
| Spike Test     | Flash‑sale event          | 1000 → 3000  | ⏳                   | [e.g., “In analysis phase”] |

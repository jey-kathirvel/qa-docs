# Database Testing Checklist

Use this checklist to validate data integrity, schema, constraints, and behavior during database‑related testing.

---

## 1. Data Integrity & Correctness

- [ ] Data entered via UI / API is correctly saved in the right table and field. [web:121][web:124]  
- [ ] Null constraints are respected; columns marked `NOT NULL` reject nulls with proper validation.  
- [ ] Data is not truncated when saved (length in DB matches UI validation). [web:124][web:129]  
- [ ] Foreign‑key relationships are maintained; child records cannot exist without valid parent records. [web:121][web:124]  

---

## 2. Schema & Field Validation

- [ ] Data types and lengths match the design / data dictionary (e.g., `varchar(50)`, `decimal(10,2)`). [web:121][web:124]  
- [ ] Primary keys are defined and do not allow duplicates. [web:124][web:127]  
- [ ] Default values, check constraints, and allowed ranges work as expected (e.g., status in `['A','I','D']`). [web:121][web:124]  
- [ ] Audit columns (e.g., `created_by`, `updated_date`, `is_deleted`) are populated correctly. [web:124][web:128]  

---

## 3. Indexes, Procedures & Triggers

- [ ] Required indexes are created and performance‑critical queries use them. [web:121][web:124]  
- [ ] Stored procedures execute correctly and return expected results and side effects. [web:121][web:124]  
- [ ] Triggers fire on the correct DML events (INSERT / UPDATE / DELETE) and update data as required. [web:121][web:124]  
- [ ] Transactions handle rollback correctly when an operation fails. [web:121][web:124]  

---

## 4. CRUD & Business Logic

- [ ] Create, Read, Update, Delete operations work correctly and update the database state as expected. [web:121][web:124]  
- [ ] Business rules (e.g., “user cannot have duplicate email”) are enforced in the database or application layer. [web:121][web:128]  
- [ ] Search, filter, and report outputs match data in the database (counts, sums, filters). [web:123][web:126]  
- [ ] Edge‑case data (empty, negative, max‑length, special characters) is handled without corruption. [web:124][web:126]  

---

## 5. Performance & Locking

- [ ] Key queries run within acceptable time on realistic‑size datasets. [web:121][web:127]  
- [ ] Bulk inserts / updates do not cause excessive locking or timeouts. [web:121][web:124]  
- [ ] Concurrency tests (multiple users updating same record) do not corrupt data or lose updates. [web:121][web:127]  
- [ ] Paginated queries return correct page‑wise data and counts. [web:123][web:126]  

---

## 6. Security & Data Quality

- [ ] Sensitive data (passwords, tokens, PII) is encrypted or masked where appropriate. [web:121][web:128]  
- [ ] Database accounts and roles have least‑privilege permissions. [web:121][web:127]  
- [ ] Data migration scripts preserve referential integrity and constraints. [web:121][web:128]  
- [ ] Data quality rules (completeness, consistency, accuracy) are enforced as per requirements. [web:126][web:128]  

---

## 7. Backup, Recovery & Logging

- [ ] Backups can be restored and data remains consistent. [web:121][web:127]  
- [ ] Log tables (e.g., audit logs, error logs) are populated correctly on key operations. [web:124][web:128]  
- [ ] Invalid or failed operations are logged without exposing sensitive data. [web:121][web:127]  

---

## 8. Database Testing Status Table (Optional)

Example table to track coverage per module:

| Module / Feature        | Data Integrity | Constraints | Procedures / Triggers | Performance | Notes |
|-------------------------|----------------|-------------|------------------------|-------------|-------|
| User Registration       | ✅             | ✅          | ✅                     | ✅          | [e.g., “All good”] |
| Order Management        | ✅             | ✅          | ⏳                     | ⏳          | [e.g., “Trigger to update status under review”] |
| Report Generation       | ✅             | ✅          | ✅                     | ✅          | [e.g., “No performance issues on small datasets”] |

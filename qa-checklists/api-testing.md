# API Testing Checklist

Use this checklist to validate functionality, reliability, security, and performance of your APIs.

---

## 1. Basic Functionality

- [ ] Each endpoint returns the correct HTTP status code for success (200/201) and failures (4xx/5xx). [web:131][web:134]  
- [ ] Request methods (`GET`, `POST`, `PUT`, `DELETE`, `PATCH`) work as documented. [web:131][web:134]  
- [ ] Required and optional parameters are documented and behave correctly. [web:134][web:136]  
- [ ] Default values and optional query/path params are handled gracefully. [web:131][web:134]  

---

## 2. Request & Response Validation

- [ ] Request body schema (JSON/XML) is validated; invalid payloads are rejected with clear errors. [web:134][web:136]  
- [ ] Response bodies are well‑structured and match the documented schema. [web:131][web:134]  
- [ ] All fields in the response have correct types, formats, and constraints (e.g., date formats). [web:131][web:134]  
- [ ] Sensitive data (e.g., passwords, tokens) is not exposed in responses. [web:130][web:135]  

---

## 3. Error Handling & Edge Cases

- [ ] API returns meaningful error messages and status codes for invalid inputs. [web:131][web:134]  
- [ ] Missing / extra fields, invalid datatypes, and malformed JSON are handled properly. [web:134][web:136]  
- [ ] Edge‑case inputs (empty, max‑length, special characters, negative numbers) do not cause crashes or wrong behavior. [web:131][web:134]  
- [ ] 4xx and 5xx responses include enough context to debug without exposing sensitive internals. [web:130][web:138]  

---

## 4. Authentication & Authorization

- [ ] Auth tokens (JWT, OAuth, API keys) are required and validated for secured endpoints. [web:130][web:135]  
- [ ] Unauthorized / forbidden requests return `401` / `403` with no data access. [web:131][web:136]  
- [ ] Token expiry, refresh, and revocation work as expected. [web:130][web:138]  
- [ ] Role‑based access control (RBAC) restricts users to permitted operations. [web:135][web:138]  

---

## 5. Security

- [ ] Input validation and sanitization prevent injection attacks (SQLi, No‑SQLi, command injection). [web:130][web:132]  
- [ ] Sensitive headers (e.g., tokens, cookies) are transmitted over HTTPS only. [web:130][web:138]  
- [ ] Rate limiting / quotas are enforced to prevent abuse. [web:130][web:135]  
- [ ] API adheres to common security best practices (e.g., OWASP API Top 10 items). [web:130][web:135]  

---

## 6. Headers, Content & Versioning

- [ ] Required headers are enforced (e.g., `Content-Type`, `Authorization`, custom headers). [web:131][web:134]  
- [ ] API versioning is consistent (e.g., `/v1/users`) and documented. [web:134][web:136]  
- [ ] Content‑type negotiation and `Accept` headers behave correctly. [web:131][web:134]  
- [ ] Etag / `If‑Modified‑Since` / `If‑None‑Match` (if any) work as intended. [web:131][web:134]  

---

## 7. Performance & Reliability

- [ ] API responds within acceptable time under normal load for key endpoints. [web:131][web:134]  
- [ ] Bulk / batch operations (e.g., bulk insert, search, export) complete successfully. [web:134][web:136]  
- [ ] API is resilient to retries; idempotent operations behave correctly (e.g., `PUT`, `DELETE`). [web:131][web:134]  
- [ ] API returns predictable results across multiple identical calls (where applicable). [web:131][web:134]  

---

## 8. Documentation & Contracts

- [ ] API documentation (Swagger/OpenAPI, Postman, etc.) matches the actual behavior. [web:131][web:139]  
- [ ] All endpoints, parameters, and sample requests/responses are documented. [web:131][web:139]  
- [ ] Schema definitions (request/response models) are up to date. [web:131][web:136]  
- [ ] Deprecation and breaking changes are clearly communicated. [web:134][web:139]  

---

## 9. API Testing Status Table (Optional)

Example table to track coverage per endpoint group:

| Module / Endpoint Group | Functionality | Auth / Authz | Security | Performance | Notes |
|-------------------------|--------------|--------------|----------|-------------|-------|
| User Endpoints          | ✅           | ✅           | ✅       | ✅          | [e.g., “All good”] |
| Order / Payment APIs    | ✅           | ✅           | ⏳       | ✅          | [e.g., “Rate‑limiting config under review”] |
| Report / Export APIs    | ✅           | ✅           | ✅       | ⏳          | [e.g., “Large export timing out; optimize query”] |

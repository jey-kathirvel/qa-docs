# Security Testing Checklist

Use this checklist during functional, penetration, and QA‑style security testing of your application.

---

## 1. Authentication & Session Management

- [ ] Strong password rules and multi‑factor‑authentication (MFA) are enforced where applicable. [web:146][web:148]  
- [ ] Login and logout flows invalidate sessions serverside and destroy tokens. [web:146][web:144]  
- [ ] Session tokens are randomly generated, non‑guessable, and updated on login. [web:146][web:145]  
- [ ] Session tokens are transmitted only over HTTPS and use `Secure`, `HttpOnly`, and `SameSite` cookie flags. [web:146][web:144]  
- [ ] Session timeout and idle‑expiry are configured. [web:146][web:145]  

---

## 2. Authorization & Access Control

- [ ] Users can only access data and functions allowed by their role (horizontal and vertical escalation checked). [web:146][web:145]  
- [ ] Admin / privileged endpoints are restricted and not exposed to non‑admins. [web:146][web:148]  
- [ ] Direct‑object‑reference (IDOR) and parameter‑tampering tests pass. [web:140][web:144]  
- [ ] Multi‑stage flows (e.g., checkout, approval) enforce access control on each step. [web:146][web:145]  

---

## 3. Input Validation & Injection

- [ ] All user inputs (forms, APIs, query params) are validated and sanitized. [web:140][web:146]  
- [ ] Test for SQL / No‑SQL injection using parameterized queries and no direct user‑input concatenation. [web:140][web:144]  
- [ ] Test for OS command injection, path traversal, and file‑inclusion vulnerabilities. [web:140][web:144]  
- [ ] Test for LDAP, XPath, XML, and other injection vectors where applicable. [web:140][web:144]  

---

## 4. Cross‑Site Scripting (XSS) & CSRF

- [ ] All user‑supplied data is properly encoded when output in HTML, JS, URLs, or CSS. [web:146][web:145]  
- [ ] Test for reflected, stored, and DOM‑based XSS. [web:140][web:144]  
- [ ] Cross‑Site Request Forgery (CSRF) tokens are present and validated on state‑changing requests. [web:146][web:145]  
- [ ] Same‑origin / CORS‑style checks are enforced where needed. [web:144][web:148]  

---

## 5. Data Protection & Privacy

- [ ] Sensitive data (passwords, tokens, PII, payment info) is not logged in plain text. [web:146][web:148]  
- [ ] Encryption in‑transit is enforced via HTTPS (TLS) on all endpoints. [web:146][web:144]  
- [ ] Critical data at rest (e.g., passwords, tokens, secrets) is encrypted or hashed (salted). [web:146][web:145]  
- [ ] Default / hardcoded credentials are removed from configuration and code. [web:140][web:144]  

---

## 6. API & Business‑Logic Security

- [ ] API endpoints require proper authentication and authorization. [web:146][web:147]  
- [ ] Rate limiting / quota is enforced to prevent abuse. [web:146][web:147]  
- [ ] Test for business‑logic flaws (e.g., price manipulation, duplicate transactions, forced browsing). [web:140][web:145]  
- [ ] Verify that redirects and URL‑parameters do not allow open redirects or SSRF. [web:140][web:144]  

---

## 7. Configuration & Infrastructure

- [ ] Error messages do not leak stack traces or internal details (generic / sanitized). [web:144][web:148]  
- [ ] Default or example pages and test components are removed from production. [web:140][web:144]  
- [ ] Web server / application server is up to date with security patches. [web:144][web:145]  
- [ ] Web server restricts dangerous HTTP methods (e.g., `PUT`, `DELETE`) where not needed. [web:144][web:146]  

---

## 8. Security Testing Status Table (Optional)

Example table to track coverage:

| Area                         | XSS / CSRF | Input / Injection | Auth / Session | API / Data | Notes |
|------------------------------|-----------|-------------------|----------------|------------|-------|
| Login / Registration         | ✅        | ✅                | ✅             | ✅         | [e.g., “All basic checks passed”] |
| User Profile & Settings      | ✅        | ✅                | ✅             | ✅         | [e.g., “No XSS found; MFA still TBD”] |
| Payment / Checkout Flow      | ✅        | ✅                | ✅             | ✅         | [e.g., “OWASP PCI‑style review scheduled”] |

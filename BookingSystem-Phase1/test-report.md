# 1️⃣ Introduction

**Tester(s):**  
- Name:  GAUTIER-GRALL Maxence / RUBAUD Ilan

**Purpose:**  
- Identify the vulnerabilities affecting the user registration flow and the general security configuration of the application.
- Assess the backend’s resistance to common attack vectors (SQL Injection, Path Traversal, CSRF, missing security headers, etc.).

**Scope:**  
- Tested components:
    - Home page (/)
    - Registration page (/register)
    - Static resources (/static/*.js, /static/*.css)
- Exclusions:
    - Login/authentication endpoint (not tested)
- Test approach:
    - Gray-box 

**Test environment & dates:**  
- Start:  20/11/2025
- End:  20/11/2025
- Test environment details
    - OS : Windows 11
    - runtime : Docker Desktop
    - DB : PostgreSQL
    - browsers: Edge + ZAP

**Assumptions & constraints:**  
    - Testing performed on a local development instance.
    - No authentication required; only the registration form was tested.
    - Full admin access to the local machine.

---

# 2️⃣ Executive Summary

**Short summary (1-2 sentences):**  
    - The ZAP scan found several serious security flaws, such as SQL Injection and Path Traversal, which make the application very vulnerable to attacks. On top of that, important security headers are missing, leaving the system even more exposed.

**Overall risk level:** 
   - High

**Top 5 immediate actions:**  
1.  Fix SQL Injection vulnerabilities
2.  Prevent Path Traversal
3.  Add CSRF protection
4.  Configure essential security headers
5.  Implement custom error

---

# 3️⃣ Severity scale & definitions

|  **Severity Level**  | **Description**                                                                                                              | **Recommended Action**           |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
|      🔴 **High**     | A serious vulnerability that can lead to full system compromise or data breach (e.g., SQL Injection, Remote Code Execution). | *Immediate fix required*         |
|     🟠 **Medium**    | A significant issue that may require specific conditions or user interaction (e.g., XSS, CSRF).                              | *Fix ASAP*                       |
|      🟡 **Low**      | A minor issue or configuration weakness (e.g., server version disclosure).                                                   | *Fix soon*                       |
| 🔵 **Info** | No direct risk, but useful for system hardening (e.g., missing security headers).                                            | *Monitor and fix in maintenance* |


---

# 4️⃣ Findings (filled with examples → replace)

> Fill in one row per finding. Focus on clarity and the most important issues.

| ID | Severity | Finding | Description | Evidence / Proof |
|------|-----------|----------|--------------|------------------|
| F-01 | 🔴 High | SQL Injection in registration | Username field allows boolean-based SQL injection | Screenshot or sqlmap result |
| F-02 | 🔴 High | Path Traversal | User can access files outside web root via ../ | Screenshot or sqlmap result |
| F-03 | 🟠 Medium | Absence of Anti-CSRF Tokens | Registration form has no CSRF protection | Burp log or response headers |
| F-04 | 🟠 Medium | Content Security Policy Missing | CSP header not set on / and /register | Burp log or response headers |
| F-05 | 🟡 Low | Weak password policy | Accepts passwords like "12345" | <img width="552" height="92" alt="image" src="https://github.com/user-attachments/assets/d8056159-c5b8-45cc-92ec-107b5ea3bb41" />
 |

---

> [!NOTE]
> Include up to 5 findings total.   
> Keep each description short and clear.

---

# 5️⃣ OWASP ZAP Test Report (Attachment)

**Purpose:**  
- Attach or link your OWASP ZAP scan results (Markdown format preferred).

---

**Instructions (CMD version):**
1. Run OWASP ZAP baseline scan:  
   ```bash
   zap-baseline.py -t https://example.com -r zap_report_round1.html -J zap_report.json
   ```
2. Export results to markdown:  
   ```bash
   zap-cli report -o zap_report_round1.md -f markdown
   ```
3. Save the report as `zap_report_round1.md` and link it below.

---
> [!NOTE]
> 📁 **Attach full report:** → `check itslearning` → **Add a link here**

---

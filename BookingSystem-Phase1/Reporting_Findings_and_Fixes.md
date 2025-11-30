# Reporting Findings and Fixes

Student : Maxence GAUTIER-GRALL / Ilan Rubaud

## Intro 
This repository contains all the work completed by Maxence GAUTIER-GRALL and Ilan Rubaud for Phase 1 – Part 2 of the cybersecurity project.
In this stage, we received an updated version of the website from the first part of the project in order to perform a second round of testing.

We first redeployed and ran the new version of the website, then performed a ZAP scan as well as manual analyses to verify and determine which issues had been fixed compared to those identified in Part 1.

This report therefore details the five issues we initially found in the first stage, along with the corresponding fixes that were applied (or not applied).


## Findings Verification Summary

This section provides a concise summary of the **Top 5 findings** originally reported in Part 1, and whether they were fixed in Part 2.

| Id | Finding | Description | Status |
|----|--------|-------------|--------|
| F1 | SQL Injection in registration | Username field allows boolean-based SQL injection | Fixed |
| F2 | Path Traversal  | User can access files outside web root via ../ | Fixed |
| F3 | Absence of Anti-CSRF Tokens  | Registration form has no CSRF protection | Not Fixed |
| F4 | Content Security Policy Missing | CSP header not set on / and /register | Fixed |
| F5 | Weak password policy | accepts passwords like "12345" | Fixed |

---

## Detailed Findings 

### Finding 1 – SQL Injection in registration
- **Original Issue:**

  The web page can be successfully manipulated using the boolean conditions like foo-bar@example.com AND 1=1 --  and foo-bar@example.com AND 1=2 --
- **How it was identified:**

  For this problem, we identified it by running a ZAP scan, which revealed the issue.
- **Verification steps:**

  To verify that this issue was resolved, we ran several different tests using OWASP ZAP, and none of them indicated that the problem was still present.
- **Status:**

  Fixed  
- **Evidence:**
  
   <img width="482" height="104" alt="image" src="https://github.com/user-attachments/assets/ccc93e0e-9aa0-440a-8c26-cbc543c0a9f6" />

---

### Finding 2 – Path Traversal
- Original Issue:

  User can access files outside web root via ../
- Identified by:

    To identify this issue, we ran a ZAP scan, which revealed the problem.
- Verification:

  To verify that this was resolved, we conducted several different tests using OWASP ZAP, and none of them showed that it was possible again.
- Status:

  Fixed
- Evidence:

  <img width="475" height="100" alt="image" src="https://github.com/user-attachments/assets/009873db-b765-412f-8dc1-03d8da8e516d" />


---

### Finding 3 – Absence of Anti-CSRF Tokens
- Original Issue:

  No known Anti-CSRF token was found in the following HTML form: [Form 1: "birthdate" "password" "username" ].
- Identified by:

  To identify this issue, we ran several tests using OWASP ZAP, which repeatedly showed that the problem persisted.
- Verification:

 The OWASP ZAP software repeatedly detected that this issue had not been resolved.
- Status:

  Not Fixed
- Evidence:

  <img width="465" height="218" alt="image" src="https://github.com/user-attachments/assets/e8963182-a86f-4856-adbd-cc5d4e616e9c" />


---

### Finding 4 – Content Security Policy Missing
- Original Issue:

  No header was found on the website  
- Identified by:

 To identify this issue, we ran a ZAP scan, which revealed the problem.
- Verification:

  To verify that this was resolved, we ran several different tests using OWASP ZAP, and none of them showed that a proper Content Security Policy was in place.
- Status:

  Fixed
- Evidence:

  <img width="472" height="143" alt="image" src="https://github.com/user-attachments/assets/60473cb4-1aee-4556-a6ea-630392547d69" />


---

### Finding 5 – Weak password policy
- Original Issue:

  On the old website we were able to set password like "12345"
- Identified by:
  
  To identify this, we tested the website by trying to set a weak password such as "12345," and the website prevented us from using a password with fewer than 8 characters.
- Verification:

  The website no longer accepts passwords with fewer than 8 characters.
- Status:

  Fixed
- Evidence:

  <img width="574" height="115" alt="image" src="https://github.com/user-attachments/assets/be0f6a96-615b-4f52-96c5-2dff9633b081" />


---

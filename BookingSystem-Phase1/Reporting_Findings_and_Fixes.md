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
- **How it was identified:**  
- **Verification steps:**  
- **Status:** Fixed  
- **Evidence:**  
  - `/screenshots/finding1.png`

---

### Finding 2 – Path Traversal
- Original Issue:  
- Identified by:  
- Verification:  
- Status:  Fixed
- Evidence:

---

### Finding 3 – Absence of Anti-CSRF Tokens
- Original Issue:  
- Identified by:  
- Verification:  
- Status:   Not Fixed
- Evidence:

---

### Finding 4 – Content Security Policy Missing
- Original Issue:  
- Identified by:  
- Verification:  
- Status:  Fixed
- Evidence:

---

### Finding 5 – Weak password policy
- Original Issue:  
- Identified by:  
- Verification:  
- Status:  Fixed
- Evidence:

---

# 📥 How to Run the Updated Application (optional)

To allow future testers or teachers to reproduce the tests:

```bash
git clone [URL of your repo]
cd BookingSystem_Part2
npm install
npm start

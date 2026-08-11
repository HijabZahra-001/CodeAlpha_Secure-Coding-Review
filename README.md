# Secure Coding Review

A secure coding review of a sample Python Flask web application. It identifies vulnerabilities such as SQL injection, plaintext password storage, hardcoded secrets, and XSS through manual code inspection and static analysis (Bandit), then documents severity-rated findings alongside concrete remediation steps and corrected, secure code.

## Project Overview

| | |
|---|---|
| **Language** | Python 3 |
| **Framework** | Flask (with SQLite) |
| **Application** | Simple user registration, login, and search app |
| **File audited** | `app.py` |
| **Tools used** | Bandit (static analyzer) + manual inspection |

## What's Included

- `Task3_Secure_Coding_Review.docx` — Full report covering:
  - Application and language selected
  - Manual code review of vulnerabilities
  - Static analyzer (Bandit) scan results
  - Recommendations and secure coding best practices
  - Documented findings table with severity ratings
  - Remediated (fixed) source code

## Vulnerabilities Identified

| ID | Vulnerability | Severity |
|----|---------------|----------|
| F1 | SQL Injection | Critical |
| F2 | Plaintext Password Storage | Critical |
| F3 | Hardcoded Secret Key | High |
| F4 | Reflected XSS | High |
| F5 | Debug Mode Enabled in Production | Medium |
| F6 | Missing Input Validation | Medium |
| F7 | No Rate Limiting on Login | Medium |
| F8 | Verbose Error Messages | Low |

## Methodology

1. **Manual Review** — traced data flow from user input (form fields, query params) to sensitive sinks (database queries, HTML output, config).
2. **Static Analysis** — ran Bandit against the source to confirm and cross-check pattern-based issues.
3. **Remediation** — rewrote vulnerable routes using parameterized queries, hashed passwords, environment-based secrets, and disabled debug mode.

## How to Use This Report

Open `Task3_Secure_Coding_Review.docx` 

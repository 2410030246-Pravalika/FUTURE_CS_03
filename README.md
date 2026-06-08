# API Security Risk Analysis

## Overview
This repository contains a professional API Security Risk Analysis conducted on the [JSONPlaceholder](https://jsonplaceholder.typicode.com) test API. This audit was performed as part of a cybersecurity task to identify common security misconfigurations and data exposure risks in a read-only environment.

## Scope & Methodology
* **Target:** JSONPlaceholder (Public Test API)
* **Approach:** Non-invasive, read-only analysis focusing on request/response headers, metadata, and server-side input handling.
* **Ethical Stance:** This analysis is strictly for educational and professional development purposes.

## Tools Used
* **API Testing:** Postman: Used for sending requests, inspecting headers, and verifying endpoint responses.
* **Inspection:** Browser DevTools: Used for network traffic inspection.
* **Reporting:** PDF

## Repository Contents
* **API Security Risk Analysis Report.pdf:** The complete security audit document detailing findings, business impacts, and remediation steps.
* **/screenshots of postman testing:** Folder containing visual evidence of the Postman testing and API responses.

## Key Findings Summary
| Risk Finding | Severity | Business Impact |
| :--- | :--- | :--- |
| Information Disclosure | Low | Exposes internal technology stack (e.g., X-Powered-By: Express). |
| Lack of Input Validation | Medium | Allows malformed data injection. |
| Missing Security Headers | Medium | Susceptibility to Clickjacking/XSS. |
| Excessive Data Exposure | Medium | Exposes sensitive user PII by default. |

## Recommendations
To move toward an enterprise-grade secure architecture, the following measures are recommended:
* **Implement Comprehensive Server-Side Validation:** Enforce strict schema validation on all incoming data.
* **Enforce Hardened Security Headers:** Integrate CSP and HSTS headers.
* **Adopt Rigorous Data Filtering:** Apply field-level masking to prevent sensitive data exposure.
* **Strengthen Authentication:** Enforce granular, role-based access control (RBAC).

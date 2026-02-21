# Microsoft Credential Capture Simulation

## Overview
This project is a high-fidelity landing page designed for **authorized** social engineering simulations using the **Gophish** framework. It demonstrates how attackers can bypass traditional perimeter security by targeting human vulnerability through visually convincing authentication templates.

## Technical Details
* **Framework:** Gophish Open-Source Phishing Framework
* **Logic:** Stripped of production telemetry scripts to ensure reliable POST-method credential interception.
* **Redirection:** Configured to redirect users to legitimate services post-submission to maintain simulation continuity.

## Analysis & Findings
During testing, I successfully tracked the full attack chain:
1. **Email Sent:** (Verified in Gophish Dashboard)
2. **Email Opened:** (Verified via tracking pixel)
3. **Link Clicked:** (Confirmed 1 unique click)
4. **Data Submitted:** (Captured dummy credentials)

## Ethical Use
This repository is for educational purposes and authorized penetration testing only. Unauthorized use is strictly prohibited.

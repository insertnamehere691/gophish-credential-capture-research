# Microsoft Credential Capture Simulation

## Overview
This project is a high-fidelity landing page designed for **authorized** social engineering simulations using the **Gophish** framework. It demonstrates how attackers can bypass traditional perimeter security by targeting human vulnerability through visually convincing authentication templates.

## Technical Details
* **Framework:** Gophish Open-Source Phishing Framework
* **Logic:** Stripped of production telemetry scripts to ensure reliable POST-method credential interception.
* **Redirection:** Configured to redirect users to legitimate services post-submission to maintain simulation continuity.

## Analysis & Findings
During testing, I successfully tracked the full attack chain:
1. **Email Sent:** Verified in Gophish Dashboard.
2. **Email Opened:** Verified via tracking pixel.
3. **Link Clicked:** Confirmed 1 unique click.
4. **Data Submitted:** Successfully captured dummy credentials (Interception confirmed).

### Simulation Visuals

**User Interface:**
This is the high-fidelity landing page used to simulate a standard Microsoft authentication flow.
![Microsoft Login UI](Screenshot%202026-02-21%20132738.png)

**Campaign Metrics:**
The Gophish dashboard validates the successful capture of data and completion of the attack lifecycle.
![Gophish Dashboard](Screenshot%202026-02-21%20132812.png)

## Ethical Use
This repository is for educational purposes and authorized penetration testing only. Unauthorized use is strictly prohibited.

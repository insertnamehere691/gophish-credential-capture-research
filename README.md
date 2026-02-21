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
4. **Data Submitted:** Successfully captured dummy credentials (Interception confirmed via dashboard).

### Simulation Visuals

**User Interface:**
This is the high-fidelity landing page used to simulate a standard Microsoft authentication flow.
![Microsoft Login UI](Screenshot%202026-02-21%20132738.png)


**Campaign Metrics:**
The Gophish dashboard validates the successful capture of data and completion of the attack lifecycle.
![Gophish Dashboard](Screenshot%202026-02-21%20132812.png)

## Remediation & Defensive Strategies

To defend against this type of credential harvesting attack, organizations should implement a layered security approach (Defense in Depth):

### 1. Multi-Factor Authentication (MFA)
* **FIDO2 / WebAuthn:** Implementing hardware security keys (like YubiKeys) is the most effective defense, as they are resistant to the type of proxying/cloning used in this simulation.
* **App-Based Push:** Moving away from SMS-based MFA to authenticator apps reduces the risk of SIM swapping and basic interception.

### 2. Technical Controls
* **Email Filtering:** Utilizing SEGs (Secure Email Gateways) that perform link "sandboxing" and real-time URL rewriting can block known Gophish listener IPs.
* **Conditional Access:** Restricting logins based on geographic location, known device state (Intune/Compliance), or IP reputation.

### 3. User Awareness Training
* **URL Inspection:** Training users to verify the Top-Level Domain (TLD) before entering credentials (e.g., checking for `login.microsoftonline.com` vs a look-alike domain).
* **Reporting Culture:** Encouraging employees to use "Report Phish" buttons, which allows SOC teams to burn the attacker's infrastructure quickly.
  
## Ethical Use
This repository is for educational purposes and authorized penetration testing only. Unauthorized use is strictly prohibited.

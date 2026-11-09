# UGH Cybersecurity Playbook: Threat, Risk & Control Assessment

A GRC-focused threat and risk assessment for **UGH**, a fictional IT services company with 1,900 employees running a hybrid Microsoft 365 E5 and on-premises Active Directory environment. The playbook identifies eight threats, maps each one to MITRE ATT&CK, scores it on a 5×5 risk matrix, and recommends policy, tool and training controls traced to NIST SP 800-53 and NIST CSF 2.0.

📄 **[Read the full playbook (PDF)](UGH-Cybersecurity-Playbook.pdf)**: 17 pages

> Built as my capstone for SM6375 – Cyber Operations Capstone, Master of Security Management (Cybersecurity), University of Houston–Downtown, Spring 2026. Revised for this portfolio in November 2026. UGH is a fictional organization.

---

## Frameworks & Methods

| Area | Framework |
|---|---|
| Structure | NIST Cybersecurity Framework (CSF) 2.0: Govern, Identify, Protect, Detect, Respond, Recover |
| Threat modeling | MITRE ATT&CK Enterprise |
| Control mapping | NIST SP 800-53 Rev. 5 and CSF 2.0 subcategories |
| Risk scoring | 5×5 likelihood × impact matrix, with current and residual risk |
| Incident response | NIST SP 800-61 Rev. 3 |
| Identity assurance | NIST SP 800-63B |

## Threats Assessed

| ID | Threat | Current risk | Residual risk |
|---|---|---|---|
| T1 | Help desk social engineering (vishing) | 🟠 High (12) | 🟡 Medium (6) |
| T2 | Insider data exfiltration from Workday | 🟠 High (15) | 🟡 Medium (8) |
| T3 | Credential abuse: SharePoint data theft | 🟠 High (12) | 🟡 Medium (6) |
| T4 | Credential phishing with AiTM session theft | 🔴 Critical (20) | 🟡 Medium (9) |
| T5 | Exploitation of unpatched or end-of-life Windows servers | 🔴 Critical (20) | 🟡 Medium (8) |
| T6 | Firewall misconfiguration or rule exploitation | 🟠 High (15) | 🟡 Medium (8) |
| T7 | Compromise of the SolarWinds management platform | 🟡 Medium (10) | 🟢 Low (5) |
| T8 | Theft or loss of company laptops | 🟡 Medium (8) | 🟡 Medium (6) |

![Risk heat map](images/heat-map.png)

## Key Findings

1. **Migrate three Windows Server 2016 systems before January 12, 2027**, when Microsoft extended support ends, or approve a time-bound Extended Security Updates exception.
2. **Enforce phishing-resistant MFA through Conditional Access.** This one control reduces risk across three threats (T1, T3, T4).
3. **Replace security-question verification at the help desk** with callback verification and Temporary Access Passes, in line with NIST SP 800-63B.
4. **Close data exfiltration paths** with USB device control, Purview sensitivity labels and DLP.
5. **Retire an unsupported Cisco ASA 5520** and introduce quarterly firewall rule recertification.

Most of these controls use Microsoft 365 E5 features the company already licenses, so the main investment is configuration and process rather than new tooling.

![Risk register](images/risk-register.png)

## What's Inside

1. **Executive Summary**: risk profile and priority actions
2. **Scope & Methodology**: frameworks, likelihood and impact definitions, heat map
3. **Identify**: hardware, application and tooling inventory; data classification; roles and risk ownership
4. **Protect & Detect**: for each threat: scenario, risk scoring, ATT&CK mapping, controls with NIST references, and detection guidance (Entra ID, Defender XDR, Purview, Intune)
5. **Respond & Recover**: containment, recovery and escalation steps for four incident types
6. **Risk Register**: owners, priority controls, current and residual risk

## Skills Demonstrated

- **Risk assessment:** likelihood and impact scoring, inherent vs. residual risk, risk treatment and acceptance
- **Control mapping:** NIST SP 800-53 Rev. 5, NIST CSF 2.0, MITRE ATT&CK
- **Identity & Access Management:** MFA and Conditional Access design, help desk identity proofing, least privilege, access reviews, separation of duties
- **Data protection:** data classification, DLP, insider risk management
- **Vulnerability & third-party risk:** patch SLAs, end-of-life planning, supply-chain risk
- **Incident response planning:** NIST SP 800-61 lifecycle, escalation and notification
- **Microsoft security stack:** Entra ID, Defender XDR, Purview, Intune

## Files

| File | Description |
|---|---|
| [`UGH-Cybersecurity-Playbook.pdf`](UGH-Cybersecurity-Playbook.pdf) | Full playbook (recommended for viewing) |
| [`UGH-Cybersecurity-Playbook.docx`](UGH-Cybersecurity-Playbook.docx) | Editable source |
| `images/` | Heat map and risk register previews |

## About Me

**Adeola Oguntuga** · Senior Tax Technology Services Consultant moving into GRC and Identity & Access Management. M.S. Security Management (Cybersecurity), University of Houston–Downtown. 10+ years in IT operations and service desk leadership.

[LinkedIn](https://www.linkedin.com/in/oguntuga)

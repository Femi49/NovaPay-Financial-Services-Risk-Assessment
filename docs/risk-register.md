# 02 — Risk Register

This document summarises all ten risks. The source of truth is the workbook (`data/NOVAPAY_RISK_REGISTER.xlsx`).

All risks have **Status: OPEN**, **existing controls: NONE** and **control effectiveness: Weak**.

## 1. Scores side by side

The workbook scores each risk twice: once in Task 1 (`RISK SCORE REGISTER`) and once in the full register. The two passes use different likelihood and impact values for some risks.

| Risk | Task 1 (L x I = Score, Rating) | Full register (L x I = Score) |
|---|---|---|
| RISK-001 | 5 x 4 = 20, Critical | 5 x 5 = 25 |
| RISK-002 | 4 x 5 = 20, Critical | 3 x 5 = 15 |
| RISK-003 | 5 x 5 = 25, Critical | 5 x 5 = 25 |
| RISK-004 | 4 x 5 = 20, Critical | 4 x 5 = 20 |
| RISK-005 | 3 x 5 = 15, High | 3 x 5 = 15 |
| RISK-006 | 3 x 4 = 12, High | 3 x 4 = 12 |
| RISK-007 | 5 x 4 = 20, Critical | 5 x 4 = 20 |
| RISK-008 | 4 x 4 = 16, Critical | 4 x 4 = 16 |
| RISK-009 | 4 x 4 = 16, Critical | 4 x 4 = 16 |
| RISK-010 | 4 x 5 = 20, Critical | 4 x 5 = 20 |

Interpretation used in this documentation: Task 1 represents the initial scenario-based scoring, and the full register is the refined version. Reconciling the two is tracked as [OI-02](04-assumptions-and-open-items.md).

## 2. Risk details

### RISK-001 — Phishing attack exploits absence of MFA

| Field | Detail |
|---|---|
| Category | Data Privacy & Cybersecurity |
| Description | A threat actor sends a targeted phishing email to staff. With no MFA, a compromised mailbox can give access to the customer database, including BVN and NIN. |
| Threat source | Adversarial (external), organised crime group |
| Inherent score (full register) | 25, Critical |
| Weakness | W-01 |
| Treatment | Mitigate |
| Action | Deploy MFA on all Microsoft 365 and system accounts within 30 days; launch mandatory phishing simulation training for all staff and contractors within 60 days |
| Owner | IT Manager / CISO |
| Target residual | 8, Medium |
| Review | 30 days after MFA deployment is confirmed, then quarterly |

### RISK-002 — Malicious contractor mass BVN record export

| Field | Detail |
|---|---|
| Category | Data Protection & Third-Party Risk |
| Description | A remote or third-party contractor with unrestricted database access deliberately exports 480,000 customer BVN records, possibly colluding with external actors. |
| Threat source | Malicious insider, possibly colluding with external actors |
| Inherent score (full register) | 15, High |
| Weaknesses | W-02, W-09 |
| Treatment | Mitigate |
| Action | Role-based access control with least privilege for contractors; Data Loss Prevention policies to detect and block export of sensitive data |
| Owner | Compliance Team / DPO |
| Target residual | 5, Low |
| Review | 6 weeks after treatment implementation |

### RISK-003 — SQL injection on the mobile application

| Field | Detail |
|---|---|
| Category | Cybersecurity / Application Security / Data Protection |
| Description | The mobile banking app has not been penetration tested since 2021. Features added since then are untested. |
| Threat source | Adversarial, cybercriminals |
| Inherent score (full register) | 25, Critical |
| Weakness | W-03 |
| Treatment | Mitigate |
| Action | Full penetration test of the app; Web Application Firewall to filter SQL injection; quarterly vulnerability assessment cycle |
| Owner | Mobile App Security Engineer / Project Team |
| Target residual | 5, Low |
| Review | Every 6 months |

### RISK-004 — Failure to notify NDPC within 72 hours

| Field | Detail |
|---|---|
| Category | Data Protection & Regulatory Compliance |
| Description | A personal data breach occurs while NovaPay has no formal Incident Response Plan, no defined escalation procedure and no appointed Data Protection Officer. |
| Threat source | Internal governance failure, absence of process and accountability |
| Inherent score (full register) | 20, High |
| Weakness | W-04 |
| Treatment | Mitigate |
| Action | Appoint a DPO (internal or outsourced); develop a formal Incident Response Plan covering breach notification, severity classification, escalation, NDPC notification and customer communication |
| Owner | DPO / Chief Compliance Officer |
| Target residual | 5, Low |
| Review | Not yet set |

### RISK-005 — Ransomware on the Azure environment

| Field | Detail |
|---|---|
| Category | Cybersecurity / Business Continuity |
| Description | An attacker gains initial access through an unpatched vulnerability and deploys ransomware that propagates, taking all customer services offline. |
| Threat source | External attacker |
| Inherent score (full register) | 15, High |
| Weakness | W-05 |
| Treatment | Mitigate + Transfer |
| Action | Implement backups and test recovery procedures; purchase cyber insurance covering ransomware |
| Owner | CISO / Head of IT |
| Target residual | 6, Medium |
| Review | 30 days |

### RISK-006 — No DPIA conducted

| Field | Detail |
|---|---|
| Category | Regulatory Compliance / Privacy |
| Description | NovaPay processes sensitive financial data (BVN), identity documents and transaction records without having conducted a DPIA, which the workbook identifies as a breach of NDPA 2023. |
| Threat source | Internal governance gap |
| Inherent score (full register) | 12, High |
| Weakness | W-06 |
| Treatment | Mitigate |
| Action | Immediately conduct DPIAs for BVN processing and other high-risk activities (the treatment sheet adds credit scoring and remittances); embed privacy by design in product development; engage a certified DPO |
| Owner | DPO / COO |
| Target residual | 6, Medium |
| Review | 60 days |

### RISK-007 — UK remittance partner breach

| Field | Detail |
|---|---|
| Category | Third-Party Risk / Regulatory Compliance |
| Description | NovaPay shares customer data with its UK remittance partner under an arrangement that may lack adequate data processing agreements. A partner breach could expose shared customer data and create cross-border liability. |
| Threat source | Third-party breach / supply chain |
| Inherent score (full register) | 20, Critical |
| Weakness | W-07 |
| Treatment | Mitigate + Transfer |
| Action | Execute data processing agreements with breach notification clauses aligned to NDPA and UK GDPR; quarterly or annual third-party security assessment of the UK partner; confirm cyber insurance covers cross-border breach liability |
| Owner | CRO / DPO |
| Target residual | 6, Medium |
| Review | 90 days |

### RISK-008 — Business Email Compromise against untrained staff

| Field | Detail |
|---|---|
| Category | Cybersecurity |
| Description | Staff with no formal security awareness training fall victim to BEC attempts. |
| Threat source | External attacker impersonating executives |
| Inherent score (full register) | 16, High (Critical in Task 1) |
| Weakness | W-08 |
| Treatment | Mitigate |
| Action | Mandatory security awareness training; BEC-specific email authentication controls; dual authorisation for all transfers above N1M |
| Owner | CISO |
| Target residual | 5, Low |
| Review | 30 days |

### RISK-009 — Contractor unmanaged endpoint access

| Field | Detail |
|---|---|
| Category | Access Control / Endpoint Security |
| Description | Remote contractors access production systems from unmanaged devices with no endpoint protection or compliance verification. |
| Threat source | External attacker leveraging a compromised endpoint |
| Inherent score (full register) | 16, High (Critical in Task 1) |
| Weakness | W-09 |
| Treatment | Mitigate |
| Action | Prohibit direct production access from unmanaged devices; implement endpoint detection and response (EDR) |
| Owner | Head of IT / CISO |
| Target residual | 6, Medium |
| Review | 60 days |

### RISK-010 — Customer service agents access full BVN details

| Field | Detail |
|---|---|
| Category | Data Protection |
| Description | Customer service agents have unrestricted access to full BVN details for 480,000 customers; an agent could leak or sell the data. |
| Threat source | Insider threat |
| Inherent score (full register) | 20, Critical |
| Weakness | W-10 |
| Treatment | Mitigate |
| Action | BVN data masking (display only the last 4 digits unless privilege is granted); audit logging of all BVN access events with SIEM alerting |
| Owner | DPO |
| Target residual | Not yet set |
| Review | Not yet set |

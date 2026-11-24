# 03 — Risk Treatment Plan

Treatment decisions are driven by the **zero tolerance** appetite for customer data breaches and regulatory non-compliance. Every risk is mitigated; two also transfer residual financial impact through cyber insurance.

## 1. Summary

| Risk | Treatment | Owner | Timeline | Target residual |
|---|---|---|---|---|
| RISK-001 | Mitigate | IT Manager / CISO | MFA 30 days; training 60 days | 8, Medium |
| RISK-002 | Mitigate | Compliance Team / DPO | Review 6 weeks after implementation | 5, Low |
| RISK-003 | Mitigate | Mobile App Security Engineer | Review every 6 months | 5, Low |
| RISK-004 | Mitigate | DPO / Chief Compliance Officer | Not set | 5, Low |
| RISK-005 | Mitigate + Transfer | CISO / Head of IT | Review 30 days | 6, Medium |
| RISK-006 | Mitigate | DPO / COO | Review 60 days | 6, Medium |
| RISK-007 | Mitigate + Transfer | CRO / DPO | Review 90 days | 6, Medium |
| RISK-008 | Mitigate | CISO | Review 30 days | 5, Low |
| RISK-009 | Mitigate | Head of IT / CISO | Review 60 days | 6, Medium |
| RISK-010 | Mitigate | DPO | Not set | Not set |

## 2. Why each option was chosen

| Risk | Justification from the workbook |
|---|---|
| RISK-001 | Zero tolerance for data breaches. MFA substantially reduces credential compromise. Avoid is not viable; transfer or accept would leave regulatory exposure. |
| RISK-002 | Selling 480,000 BVNs would have catastrophic regulatory and reputational consequences. The risk cannot be transferred or accepted, so likelihood must be reduced through access control. |
| RISK-003 | A three-year testing gap on a public-facing app is indefensible before regulators. |
| RISK-004 | The notification duty is mandatory law. Acceptance is prohibited by appetite; process and governance are the only valid response. |
| RISK-005 | Low tolerance for extended outages. Mitigation reduces likelihood and recovery time; insurance transfers the residual financial impact. 480,000 customers depend on availability. |
| RISK-006 | A DPIA is a legal obligation. Acceptance would be deliberate non-compliance. |
| RISK-007 | The partnership is core revenue so avoidance is not possible, and acceptance is not possible given dual regulatory exposure. Insurance is a financial backstop. |
| RISK-008 | Staff are the primary attack surface, and a formal security policy is required as an organisational measure. |
| RISK-009 | Unmanaged contractor endpoints are a primary exfiltration vector. Controls must match those applied to permanent staff. |
| RISK-010 | Unrestricted BVN access by customer-facing agents is a high insider-threat vector. |

## 3. Actions grouped by theme

| Theme | Actions | Risks addressed |
|---|---|---|
| Identity and access | MFA on Microsoft 365 via Conditional Access; RBAC and least privilege for contractors; privileged access limited to project need | 001, 002, 009 |
| Data protection | DLP to block bulk exports; BVN masking (last 4 digits); DPIAs for BVN, credit scoring and remittances | 002, 006, 010 |
| Monitoring and detection | SIEM alerting on BVN access; audit logs; threat detection capability | 004, 010 |
| Application security | Full mobile app penetration test; WAF; quarterly vulnerability assessments | 003 |
| Governance and compliance | Appoint DPO; Incident Response Plan with 72-hour NDPC procedure; quarterly tabletop exercise; formal security policy | 004, 006, 008 |
| Resilience | Tested backups and recovery; cyber insurance | 005, 007 |
| Third-party | Data processing agreements with breach clauses; periodic partner security assessment | 007 |
| People | Mandatory awareness training; quarterly phishing simulation; dual authorisation above N1M | 001, 008 |
| Endpoint | Block unmanaged devices from production; EDR; device compliance policy | 009 |

## 4. Indicative ISO/IEC 27001:2022 Annex A mapping

> Added during documentation and **not part of the source workbook**. Treat as indicative and validate against the Statement of Applicability when it is produced.

| Risk | Indicative Annex A controls |
|---|---|
| RISK-001 | A.8.5 Secure authentication; A.6.3 Awareness, education and training |
| RISK-002 | A.5.15 Access control; A.5.18 Access rights; A.8.2 Privileged access rights; A.8.12 Data leakage prevention |
| RISK-003 | A.8.8 Management of technical vulnerabilities; A.8.29 Security testing in development and acceptance |
| RISK-004 | A.5.24 to A.5.28 Information security incident management; A.5.31 Legal, statutory, regulatory and contractual requirements |
| RISK-005 | A.8.13 Information backup; A.5.29 and A.5.30 Continuity and ICT readiness |
| RISK-006 | A.5.34 Privacy and protection of PII; A.5.31 Legal requirements |
| RISK-007 | A.5.19 to A.5.22 Supplier relationships and services |
| RISK-008 | A.6.3 Awareness training; A.5.1 Policies for information security |
| RISK-009 | A.8.1 User endpoint devices; A.6.7 Remote working; A.8.7 Protection against malware |
| RISK-010 | A.8.11 Data masking; A.8.15 Logging; A.8.16 Monitoring activities |

## 5. Not yet defined

- Review dates for RISK-004 and RISK-010
- Target residual rating for RISK-010
- Budget, resourcing and dependencies between actions
- Success measures (KPIs/KRIs) per risk

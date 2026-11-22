# NovaPay Financial Services Ltd — Cyber Risk Assessment

![Status](https://img.shields.io/badge/status-in%20progress-orange)
![Version](https://img.shields.io/badge/version-1.0%20DRAFT-blue)
![Framework](https://img.shields.io/badge/framework-ISO%2FIEC%2027001%3A2022-green)

A GRC consulting project: a cyber risk assessment, risk register and treatment plan for **NovaPay Financial Services Ltd**, a Nigerian fintech with 150 staff and 480,000 customers, hosted on Microsoft Azure with a UK remittance partnership.

> **Disclaimer:** NovaPay is a simulated client created for portfolio and training purposes. All data, scenarios and scores in this repository are illustrative and do not describe a real organisation.

> **Project status: ongoing.** Version 1.0 is a draft for review. See [`docs/05-roadmap.md`](docs/05-roadmap.md) for what is done and what is next, and [`docs/04-assumptions-and-open-items.md`](docs/04-assumptions-and-open-items.md) for known inconsistencies still to be reconciled.

---

## Table of contents

- [Scenario](#scenario)
- [What this project delivers](#what-this-project-delivers)
- [Headline results](#headline-results)
- [Repository structure](#repository-structure)
- [Methodology in brief](#methodology-in-brief)
- [Frameworks and regulations](#frameworks-and-regulations)
- [How to use this repository](#how-to-use-this-repository)
- [Document control](#document-control)

## Scenario

| Item | Detail |
|---|---|
| Organisation | NovaPay Financial Services Ltd |
| Sector | Fintech, payment services |
| Size | 150 staff (full-time employees and remote contractors) |
| Customers | 480,000 registered customers |
| Hosting | Cloud-hosted on Microsoft Azure |
| Partnership | UK-based remittance partner (cross-border payments) |
| Jurisdiction | Nigeria and United Kingdom |
| Risk appetite | **Zero tolerance** for customer data breaches and regulatory non-compliance. Risks rated High or Critical require immediate treatment. |

### Known weaknesses that define the scope

| Ref | Weakness |
|---|---|
| W-01 | No MFA on Microsoft 365 |
| W-02 | A contractor with full database access exports and sells 480,000 customer BVN records |
| W-03 | Mobile app last penetration tested in 2021 |
| W-04 | Failure to notify the NDPC of a data breach within 72 hours, followed by enforcement action |
| W-05 | Ransomware encrypts the Azure cloud environment |
| W-06 | No Data Protection Impact Assessment (DPIA) conducted |
| W-07 | UK remittance partner breach exposes shared customer data |
| W-08 | Untrained staff fall victim to Business Email Compromise (BEC) |
| W-09 | Remote contractors have the same access as full-time staff |
| W-10 | Customer service agents can view full BVN details |

## What this project delivers

| Component | Deliverable | Location |
|---|---|---|
| Cover and scope | Engagement details, organisation profile, weaknesses in scope, risk appetite statement | Workbook: `CoverPage` |
| Task 1 | Risk identification and scoring (likelihood x impact, 5x5 matrix) | Workbook: `RISK SCORE REGISTER` |
| Task 2 | Treatment options with justification against risk appetite | Workbook: `TREATMENT OPTIONS` |
| Task 3 | Full risk register: inherent and residual scoring, owners, status, target residual rating, review dates | Workbook: `fULL RISK REGISTER` |
| Documentation | Method, register, treatment plan, assumptions and roadmap | [`docs/`](docs/) |

## Headline results

Ten risks were assessed. **All ten are treated with MITIGATE**, and two (RISK-005 and RISK-007) also use TRANSFER through cyber insurance.

| Risk | Scenario | Score (Task 1) | Rating |
|---|---|---|---|
| RISK-001 | Phishing with no MFA on Microsoft 365 | 20 | Critical |
| RISK-002 | Malicious contractor exports 480,000 BVN records | 20 | Critical |
| RISK-003 | Mobile app SQL injection (untested since 2021) | **25** | Critical |
| RISK-004 | Missed 72-hour NDPC breach notification | 20 | Critical |
| RISK-005 | Ransomware on the Azure environment | 15 | High |
| RISK-006 | No DPIA conducted | 12 | High |
| RISK-007 | UK remittance partner breach | 20 | Critical |
| RISK-008 | BEC against untrained staff | 16 | Critical |
| RISK-009 | Contractor access from unmanaged endpoints | 16 | Critical |
| RISK-010 | Customer service agents leak full BVN details | 20 | Critical |

Eight of ten risks rate Critical and two rate High in the Task 1 scoring. The full register re-scores each risk, which produces different numbers for some of them; see [`docs/02-risk-register.md`](docs/02-risk-register.md) and the reconciliation notes in [`docs/04-assumptions-and-open-items.md`](docs/04-assumptions-and-open-items.md).

All existing controls are assumed to be **NONE** (effectiveness "Weak") because the starting position is a very weak security environment, so residual risk currently equals inherent risk.

## Repository structure

```text
novapay-cyber-risk-assessment/
├── README.md                              <- you are here
├── data/
│   └── NOVAPAY_RISK_REGISTER.xlsx         <- source workbook (4 sheets)
└── docs/
    ├── 01-methodology.md                  <- scoring scale, rating bands, approach
    ├── 02-risk-register.md                <- all 10 risks in detail
    ├── 03-risk-treatment-plan.md          <- actions, owners, timelines, targets
    ├── 04-assumptions-and-open-items.md   <- assumptions, limitations, items to reconcile
    └── 05-roadmap.md                      <- progress and next steps
```

## Methodology in brief

- **Scale:** 5x5 matrix. Likelihood 1 (Rare) to 5 (Almost Certain); Impact 1 (Negligible) to 5 (Catastrophic).
- **Score:** Likelihood x Impact, giving 1 to 25.
- **Treatment options:** Mitigate, Transfer, Avoid, Accept, chosen against the zero-tolerance risk appetite.
- **Register fields:** category, description, threat source, existing controls, control effectiveness, inherent and residual score, treatment, owner, status, target residual rating, review date.

Full detail in [`docs/01-methodology.md`](docs/01-methodology.md).

## Frameworks and regulations

- ISO/IEC 27001:2022 (risk assessment, risk treatment, Annex A controls)
- Nigeria Data Protection Act (NDPA) 2023 and NDPR 2019, both cited in the workbook
- CBN guidelines
- UK GDPR-equivalent obligations arising from the UK remittance partnership

## How to use this repository

1. Start with this README, then read `docs/` in numerical order.
2. Open `data/NOVAPAY_RISK_REGISTER.xlsx` in Excel or LibreOffice for the working register.
3. Check `docs/04-assumptions-and-open-items.md` before reusing any score, since several items are still being reconciled.

## Document control

| Field | Value |
|---|---|
| Document reference | NOVA-CRA-2025-001 (the workbook footer also shows NOVA-ISRA-2025-001; see open items) |
| Version | 1.0 |
| Status | DRAFT, for review |
| Classification | CONFIDENTIAL (marking carried over from the workbook) |
| Date prepared | 09 August 2026 |
| Review date | 09 August 2027 |
| Prepared by | Femi Awoyomi |
| Approved by | Chief Risk Officer (simulated role) |
| Document owner | Head of Compliance & Risk (simulated role) |
| Distribution | Executive Committee (simulated) |

# 04 — Assumptions, Limitations and Open Items

This is a working document for an ongoing project. Items are listed as found in the v1.0 DRAFT workbook so they can be reconciled before the register is approved.

## 1. Assumptions

| ID | Assumption |
|---|---|
| A-01 | NovaPay is a simulated client; all facts beyond the ten known weaknesses are illustrative. |
| A-02 | Existing controls are NONE and effectiveness is Weak for all risks, so residual risk equals inherent risk. |
| A-03 | Risk appetite is zero tolerance for customer data breaches and regulatory non-compliance. |
| A-04 | Staff count is 150, a mix of full-time employees and remote contractors. |
| A-05 | The BVN dataset covers all 480,000 customers. |
| A-06 | Risk ratings are qualitative; no financial quantification (for example expected loss) is included. |

## 2. Limitations

- No asset inventory or data-flow mapping underpins the register.
- No threat modelling or technical testing was performed; scores are judgement-based.
- Likelihood and impact are not backed by incident history or industry loss data.
- Treatment actions have no cost estimates or implementation plan.

## 3. Open items to reconcile

| ID | Area | Observation | Suggested resolution |
|---|---|---|---|
| OI-01 | Rating bands | The cover page shows Critical as 20 to 25 and High as 12 to 19. The scoring sheet shows Critical as 16 to 25, overlapping High. Scores of 16 are rated Critical in Task 1. | Adopt one set of bands and update both sheets and the legend. |
| OI-02 | Scoring consistency | Likelihood and impact differ between Task 1 and the full register for RISK-001, 002, 003 and 004 (for example RISK-003 is 25 in Task 1 and 12 in the full register). | Decide which is authoritative, or document why the second pass changed the scores. |
| OI-03 | Rating labels | In the full register, inherent scores are calculated (likelihood x impact) but ratings are not shown in that column. The residual column is typed text: rows 001 to 003 show "score-RATING" (for example "25-CRITICAL") while 004 to 010 show a bare score. | Use one "score - rating" format across all rows. |
| OI-04 | Document reference | Cover page reference is NOVA-CRA-2025-001; the footer shows NOVA-ISRA-2025-001. The reference also carries 2025 while the document is dated 2026. | Align reference and year. |
| OI-05 | Regulation citations | The workbook cites NDPR 2019 on the cover and NDPA 2023 in the treatment text, including a specific section number for DPIA. | Confirm which instrument applies and verify section references against the legal text. |
| OI-06 | Acronym use | In RISK-007, "DPIA" is used where "data processing agreements" is meant. | Use DPA for data processing agreements and keep DPIA for impact assessments. |
| OI-07 | Staff numbers | RISK-001 refers to "all 200 staff and contractors"; the profile says 150 staff. | Use one headcount. |
| OI-08 | Effectiveness claims | Treatment justifications quote MFA risk reductions of 89% (Treatment sheet) and 85% (Full register) with no source. | Cite a source or remove the figures. |
| OI-09 | Typos and product names | Several spelling errors in the Treatment sheet and register text; "Microsoft Defender for 363" should read 365; sheet name `fULL RISK REGISTER` has an incorrect capital. | Proofread and rename. |
| OI-10 | Scale definitions | The likelihood and impact scales have labels (Rare to Almost Certain, Negligible to Catastrophic) but no written definitions per level (for example financial or regulatory thresholds). | Add definitions for each level. |
| OI-11 | Missing fields | Review date missing for RISK-004 and RISK-010; target residual rating missing for RISK-010. | Complete. |
| OI-12 | Calculations | Scores are calculated by formula (likelihood x impact), but rating labels and residual scores are typed text, so they will not update if inputs change. | Derive ratings and residual values by formula from the agreed bands. |
| OI-13 | Task 1 vs full risk titles | RISK-009 reads as "access without endpoint security controls" in Task 1 but "unmanaged endpoint access" in the full register, and some Task 1 scenarios differ from the cover weakness wording (W-09 describes access level, not endpoints). | Align wording across sheets. |

## 4. Change log

| Version | Date | Change |
|---|---|---|
| 1.0 DRAFT | 09 Aug 2026 | Initial register, treatment options and full register prepared |
| Docs | 22 Nov 2026 | README and documentation added; open items logged |

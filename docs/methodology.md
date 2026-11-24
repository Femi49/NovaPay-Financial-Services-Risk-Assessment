# 01 — Methodology

## 1. Purpose and scope

This assessment identifies, scores and treats cyber and data-protection risks for NovaPay Financial Services Ltd. The scope is defined by ten known weaknesses (W-01 to W-10, listed in the [README](../README.md#known-weaknesses-that-define-the-scope)). Each weakness is expressed as a risk scenario and carried through scoring, treatment and ownership.

## 2. Approach

| Step | Activity | Workbook sheet |
|---|---|---|
| 1 | Define context, scope and risk appetite | `CoverPage` |
| 2 | Identify risk scenarios from the known weaknesses | `RISK SCORE REGISTER` |
| 3 | Score each risk on likelihood and impact | `RISK SCORE REGISTER` |
| 4 | Select a treatment option and justify it against risk appetite | `TREATMENT OPTIONS` |
| 5 | Build the full register: description, threat source, controls, residual risk, owner, target, review date | `fULL RISK REGISTER` |

This follows the risk assessment and treatment structure of ISO/IEC 27001:2022 (clauses 6.1.2 and 6.1.3).

## 3. Scoring scale

**Risk score = Likelihood x Impact** (range 1 to 25).

| Score | Likelihood | Impact |
|---|---|---|
| 1 | Rare | Negligible |
| 2 | Unlikely | Minor |
| 3 | Possible | Moderate |
| 4 | Likely | Major |
| 5 | Almost Certain | Catastrophic |

## 4. Rating bands

Two sets of bands appear in the workbook. They are recorded here as found; the overlap is raised as an open item.

| Rating | Cover page legend | Scoring sheet legend |
|---|---|---|
| Low | 1 to 5 | 1 to 5 |
| Medium | 6 to 11 | 6 to 11 |
| High | 12 to 19 | 12 to 19 |
| Critical | 20 to 25 | 20 to 25 |

The Task 1 ratings in the `RISK SCORE REGISTER` sheet use the **20 to 25 Critical** band. See [open item OI-01](04-assumptions-and-open-items.md).

## 5. Risk appetite

> NovaPay operates a **zero tolerance** policy for customer data breaches and regulatory non-compliance. All risks rated High or Critical require immediate treatment.

Consequences for treatment choice:

- **Accept** is not available for any High or Critical risk.
- **Avoid** is not viable where the activity is core to the business (for example the UK remittance partnership, which is core revenue).
- **Mitigate** is the primary response, with **Transfer** (cyber insurance) used only for residual financial impact.

## 6. Treatment options

| Option | Meaning | Used for |
|---|---|---|
| Mitigate | Reduce likelihood and/or impact with controls | All 10 risks |
| Transfer | Shift financial impact, for example through cyber insurance | RISK-005, RISK-007 (combined with Mitigate) |
| Avoid | Stop the activity creating the risk | Not used |
| Accept | Tolerate the risk | Not used (prohibited by appetite) |

## 7. Control and residual risk assumptions

- Existing controls for every risk are set to **NONE**, with effectiveness **Weak**, based on the assumption that NovaPay's cyber environment is very weak.
- Residual risk therefore equals inherent risk at this stage.
- A **target residual rating** is set for each risk to show the intended outcome after treatment.

## 8. Full register fields

| Field | Description |
|---|---|
| Risk ID, Title | Unique identifier and short name |
| Risk category | For example Data Privacy & Cybersecurity, Third-Party Risk |
| Risk description | Scenario and cause |
| Threat source | Adversarial (external or insider), governance failure, supply chain |
| Likelihood, Impact | 1 to 5 each |
| Inherent risk score / rating | Likelihood x Impact |
| Existing control, effectiveness | Controls in place today and how well they work |
| Residual risk score and rating | Risk after existing controls |
| Treatment option, action | Chosen response and specific steps |
| Risk owner | Accountable role |
| Status | OPEN for all ten risks |
| Target residual risk rating | Intended rating after treatment |
| Review date | Next review trigger |

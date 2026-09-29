# AI Vendor Risk Assessment Procedure

| Field | Value |
|---|---|
| Document type | Procedure supporting the Corporate Policy for the Ethical Use of AI |
| Version | 1.0 (draft for policy version 3.0) |
| Author | Gustavo Rodrigues |
| Date | September 2026 |
| Policy mandate | Sections 3.2 (acquisition of AI solutions), 7.1 (prior approval), 8.1 (risk classification and approval) and 10.1 (AI inventory) |
| Tool | [`templates/ai-vendor-risk-assessment-matrix.xlsx`](../templates/ai-vendor-risk-assessment-matrix.xlsx) |
| License | [CC BY 4.0](../LICENSE) |

---

## 1. Purpose

Most AI used inside organizations is bought, not built: SaaS tools with AI features, model APIs, copilots and agents embedded in existing platforms. The policy requires every AI tool to be approved before use (7.1) and applies to anyone who acquires AI solutions (3.2), but it does not say **how** a vendor's AI is evaluated.

This procedure fills that gap. It defines a repeatable, vendor-agnostic method to:

1. classify the inherent risk of the intended use case;
2. assess the vendor across security, privacy, model governance and contractual domains;
3. apply knock-out criteria that no score can compensate;
4. reach a documented decision: approve, approve with conditions, or reject;
5. set reassessment triggers once the vendor is in use.

The method is **agnostic**: the same questionnaire compares commercial model providers, open-source models hosted by a third party, and SaaS products with embedded AI.

---

## 2. Scope

This procedure applies whenever the organization intends to:

- contract a new AI product, AI-enabled SaaS or model API;
- enable an AI feature in a product already in use (for example, a copilot added to an existing platform);
- use a third-party hosted open-source model;
- materially change the use of an approved AI vendor (new data category, new user group, new business process).

It does not cover AI systems developed entirely in-house without third-party models or services.

---

## 3. Roles

| Role | Responsibility |
|---|---|
| **Business owner** (requester) | Describes the use case, answers the tiering questions, owns the residual risk after approval |
| **IT / Information Security** | Assesses domains 1 (security) and 6 (resilience); validates evidence |
| **Privacy / DPO** | Assesses domain 2 (data protection); confirms LGPD requirements and international transfers |
| **Legal** | Assesses domain 7 (legal and contractual); negotiates required clauses |
| **Procurement** | Ensures the assessment is completed before contract signature |
| **AI Governance Committee** (policy Section 8) | Approves High-tier vendors and all conditional approvals; decides on exceptions |

Approval authority by tier:

| Inherent tier | Who approves |
|---|---|
| Low | IT / Information Security and Privacy |
| Medium | IT / Information Security, Privacy and Legal |
| High | AI Governance Committee |

---

## 4. Process Overview

```text
1. Intake            Business owner registers the request and describes the use case
      ↓
2. Inherent tier     Tiering questionnaire → Low / Medium / High
      ↓
3. Due diligence     Vendor questionnaire and evidence, depth set by the tier
      ↓
4. Scoring           30 questions in 8 weighted domains → overall score and residual risk
      ↓
5. Knock-outs        5 eliminatory criteria → any failure means rejection
      ↓
6. Decision          Approve / Approve with conditions / Reject
      ↓
7. Contract          Required clauses included before signature
      ↓
8. Registration      Vendor and use case added to the AI inventory (policy 10.1) + Annex I record
      ↓
9. Monitoring        Periodic reassessment and event-driven triggers
```

---

## 5. Step 1–2: Inherent Risk Tiering

The tier describes the **use case**, not the vendor. It answers: how much harm could this AI cause here if it fails? Several vendors competing for the same use case share the same tier.

| ID | Question | Points if "Yes" |
|---|---|---|
| T-1 | Will the tool process personal data? | 2 |
| T-2 | Will it process sensitive personal data (LGPD Art. 5, II) or confidential or regulated business data? | 3 |
| T-3 | Will its outputs be used in decisions that affect individuals (credit, hiring, access to services, benefits)? | 3 |
| T-4 | Will it act autonomously in other systems (agents with write access, automated actions)? | 2 |
| T-5 | Will customers, citizens or other external parties interact directly with it? | 1 |
| T-6 | Would its unavailability stop a business-critical process? | 1 |
| T-7 | Will it be used at scale (more than 1,000 users or people affected)? | 1 |

Tier rules:

| Tier | Rule |
|---|---|
| **High** | 7 points or more, **or** T-3 = Yes |
| **Medium** | 3 to 6 points |
| **Low** | 0 to 2 points |

T-3 forces High because decisions about individuals carry the highest legal and ethical exposure (LGPD Art. 20) regardless of other factors.

---

## 6. Step 3: Due Diligence Depth

| Tier | Minimum evidence |
|---|---|
| Low | Vendor questionnaire; public documentation (trust center, terms, privacy policy) |
| Medium | Low requirements, plus contractual documents for domains 1, 2 and 7 (DPA, security annex, terms) |
| High | Medium requirements, plus independent evidence for IS-01, DP-01 and DP-03 (certificate, audit report or signed contract clause), plus an AI impact assessment under policy Section 8.1 |

---

## 7. Step 4: Scoring

### 7.1 Scale

Each question is scored from 0 to 3 for each vendor:

| Score | Meaning |
|---|---|
| 0 | Not met, or no information provided |
| 1 | Claimed by the vendor, without documentation |
| 2 | Met and documented (policy, contract, technical documentation) |
| 3 | Met with independent evidence (certification, third-party audit report, signed contractual commitment) |
| N/A | Not applicable to this use case. Excluded from the calculation; the reason must be recorded |

The scale rewards **evidence**, not promises. A vendor that claims everything without documentation scores at most 33%.

### 7.2 Domains and Questions

| # | Domain | Weight | Questions |
|---|---|---|---|
| 1 | Information Security | 20% | IS-01 to IS-05 |
| 2 | Data Protection & Privacy | 20% | DP-01 to DP-05 |
| 3 | AI Model Governance | 15% | MG-01 to MG-04 |
| 4 | Responsible AI & Safety | 10% | RA-01 to RA-04 |
| 5 | Transparency & Auditability | 10% | TA-01 to TA-03 |
| 6 | Operational Resilience | 10% | OR-01 to OR-03 |
| 7 | Legal & Contractual | 10% | LC-01 to LC-04 |
| 8 | Vendor Viability | 5% | VV-01 to VV-02 |

Security and data protection carry 40% of the weight because they cover the most frequent and most regulated failure modes of AI procurement: data leakage, unauthorized training on customer data and unlawful international transfers.

The full question list, with the evidence expected for each, is in the `Assessment` sheet of the matrix and in [Annex A](#annex-a--question-list).

### 7.3 Calculation

- **Domain score** = points obtained ÷ (3 × number of applicable questions in the domain).
- **Overall score** = sum of (domain score × domain weight), with weights re-normalized if a whole domain is N/A.
- **Residual risk** from the overall score:

| Overall score | Residual risk |
|---|---|
| 75% or more | Low |
| 50% to 74% | Medium |
| Below 50% | High |

A vendor is **Incomplete** until every question is scored or marked N/A.

---

## 8. Step 5: Knock-out Criteria

A knock-out failure leads to rejection **regardless of the overall score**. These are conditions no compensating strength can offset.

| ID | Criterion | Applies to |
|---|---|---|
| KO-1 | Personal data will be processed and the vendor does not accept a data processing agreement with LGPD obligations | All tiers, when T-1 = Yes |
| KO-2 | The vendor uses customer data (prompts, files, outputs) to train or improve models with no opt-out or contractual exclusion | All tiers |
| KO-3 | The vendor does not commit to notify security incidents affecting customer data | All tiers |
| KO-4 | Personal data will be transferred outside Brazil without a mechanism recognized under LGPD Art. 33 | All tiers, when T-1 = Yes |
| KO-5 | The vendor refuses to disclose its underlying foundation model provider and subprocessors | High tier |

Each knock-out is recorded as Pass, Fail or N/A.

---

## 9. Step 6: Decision

| Condition | Decision |
|---|---|
| Any question unscored | Incomplete: no decision can be issued |
| Any knock-out = Fail | **Reject** |
| Residual risk High | **Reject** |
| Residual risk Medium | **Approve with conditions** |
| Residual risk Low, tier Low or Medium | **Approve** |
| Residual risk Low, tier High | **Approve (committee)** |

**Approve with conditions** requires: the specific gaps (questions scored 0 or 1), the compensating controls or contractual changes that address them, an owner and a deadline, AI Governance Committee sign-off, and reassessment within 6 months.

**Exceptions.** A rejected vendor may only be used through a formal risk acceptance by senior management, as required by policy Section 8 for high-risk cases. The acceptance must name the risk owner, the reason, the compensating controls and an expiry date.

---

## 10. Step 7: Required Contract Clauses

Before signature, the contract (or the vendor's standard terms, if accepted) must cover:

1. **Data processing agreement** with LGPD roles (controller and operator) and processing instructions.
2. **No training on customer data**, or an explicit opt-out applied to the organization's account.
3. **Data location** and the international transfer mechanism, when applicable.
4. **Security incident notification** with a defined timeframe.
5. **Retention and deletion** of customer data, including at contract termination.
6. **Subprocessor list** and prior notice of changes.
7. **Notice of material model changes** that may affect output quality or behavior.
8. **Ownership of inputs and outputs**, and IP indemnity where available.
9. **Audit rights** or the right to receive independent audit reports.
10. **Data export and exit assistance** in a usable format.

---

## 11. Step 8: Registration and Records

After the decision:

- the vendor, use case, tier, decision and conditions are registered in the **AI inventory** (policy 10.1);
- the **Annex I Compliance Verification Record** of the policy is completed;
- the completed matrix and evidence are stored as audit evidence (policy 12.2).

---

## 12. Step 9: Monitoring and Reassessment

| Situation | Reassessment |
|---|---|
| High tier | Every 12 months |
| Medium tier | Every 24 months |
| Low tier | Every 36 months |
| Approved with conditions | Within 6 months, and when conditions are due |

Event-driven reassessment is mandatory when:

- the vendor changes the underlying model or its terms of use in a material way;
- a security or privacy incident involves the vendor;
- the use case changes tier (new data category, new user group, decisions about individuals);
- the vendor changes ownership or subprocessors in a relevant way;
- the contract is renewed.

---

## 13. Framework Alignment

| Procedure element | ISO/IEC 42001:2023 | ISO/IEC 27001:2022 | NIST AI RMF 1.0 | LGPD |
|---|---|---|---|---|
| Vendor assessment before use | A.10 Third-party and customer relationships | A.5.19 Information security in supplier relationships | GOVERN 6 (third-party risk policies) | Art. 39 (operator follows controller instructions) |
| Inherent risk tiering | 6.1.2 AI risk assessment | — | MAP | Art. 20 (automated decisions) |
| Contract clauses | A.10 | A.5.20 Addressing information security within supplier agreements | GOVERN 6 | Arts. 33 and 39 |
| Supply chain and foundation model disclosure | A.10 | A.5.21 Managing information security in the ICT supply chain | GOVERN 6, MAP | — |
| Reassessment and monitoring | 9.1 Monitoring, measurement, analysis and evaluation | A.5.22 Monitoring, review and change management of supplier services | MANAGE | — |
| Cloud-based AI services | A.10 | A.5.23 Information security for use of cloud services | GOVERN 6 | Art. 46 (security measures) |

References to ISO standards indicate conceptual alignment. They should be checked against the licensed text before formal use.

---

## Annex A – Question List

| ID | Domain | Question | Evidence expected |
|---|---|---|---|
| IS-01 | Information Security | Does the vendor hold an independent security certification or attestation (ISO/IEC 27001, SOC 2 Type II)? | Certificate or audit report and its scope |
| IS-02 | Information Security | Is customer data encrypted in transit and at rest? | Security documentation or trust center |
| IS-03 | Information Security | Does the product support SSO, MFA and role-based access control? | Product documentation |
| IS-04 | Information Security | Does the vendor run vulnerability management and regular penetration tests? | Pentest summary or attestation |
| IS-05 | Information Security | Does the vendor commit to notify security incidents within a defined timeframe? | Contract or security annex |
| DP-01 | Data Protection & Privacy | Is there a data processing agreement covering LGPD obligations? | Signed or standard DPA |
| DP-02 | Data Protection & Privacy | Are data locations disclosed, with a legal mechanism for international transfers? | DPA, data residency documentation |
| DP-03 | Data Protection & Privacy | Are prompts, files and outputs excluded from model training by default or by contract? | Contract clause or account setting documentation |
| DP-04 | Data Protection & Privacy | Can retention be configured, and is deletion verifiable? | Retention policy, deletion procedure |
| DP-05 | Data Protection & Privacy | Is a subprocessor list available, with notice of changes? | Subprocessor list |
| MG-01 | AI Model Governance | Is there model or system documentation (intended use, limitations, known risks)? | Model or system card |
| MG-02 | AI Model Governance | Does the vendor give advance notice of model changes, versioning and deprecation? | Change policy, release notes |
| MG-03 | AI Model Governance | Are evaluation results available for accuracy and performance on relevant tasks? | Evaluation reports, benchmarks |
| MG-04 | AI Model Governance | Does the vendor disclose the underlying foundation model provider? | Documentation or written confirmation |
| RA-01 | Responsible AI & Safety | Does the vendor publish a responsible AI policy or principles? | Public policy |
| RA-02 | Responsible AI & Safety | Are bias and fairness tests documented? | Test reports, model card sections |
| RA-03 | Responsible AI & Safety | Are there safeguards against harmful content and misuse? | Safety documentation, content filters |
| RA-04 | Responsible AI & Safety | Does the product support human oversight (review, override, approval steps)? | Product documentation |
| TA-01 | Transparency & Auditability | Are usage and audit logs available to the customer? | Admin console, log export or API |
| TA-02 | Transparency & Auditability | Does the product support disclosing AI-generated content to end users? | Product documentation |
| TA-03 | Transparency & Auditability | Can outputs used in decisions be explained or justified? | Explainability features, citations |
| OR-01 | Operational Resilience | Is there a contractual availability SLA? | SLA document |
| OR-02 | Operational Resilience | Are business continuity and disaster recovery plans in place and tested? | BCP/DR summary or attestation |
| OR-03 | Operational Resilience | Can data be exported in a standard format, with an exit plan? | Export features, termination clauses |
| LC-01 | Legal & Contractual | Does the contract define customer ownership of inputs and outputs? | Terms of service |
| LC-02 | Legal & Contractual | Is IP infringement indemnity offered for outputs? | Contract clause |
| LC-03 | Legal & Contractual | Does the customer have audit rights or access to audit reports? | Contract clause |
| LC-04 | Legal & Contractual | Does the vendor commit to applicable regulation (LGPD; EU AI Act where relevant)? | Contract, compliance statements |
| VV-01 | Vendor Viability | Does the vendor have a sound track record and financial stability? | Company information, references |
| VV-02 | Vendor Viability | Are concentration risk and alternatives understood? | Internal market analysis |

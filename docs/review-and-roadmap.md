# Review of Version 2.0 and Roadmap to Version 3.0

## 1. Purpose

This document records a structured review of version 2.0 of the policy. Editorial findings were resolved in version 2.1; content gaps are planned for version 3.0. It lists what the policy does well, which gaps a governance or audit reviewer would identify, and the planned changes for version 3.0.

Review date: September 2026.

---

## 2. Strengths of Version 2.0

- **Clear template status.** Section 1 states that the document is a template and only becomes binding after formal adoption. This prevents the policy from being mistaken for an active corporate rule.
- **Explicit distinction between fully automated and AI-assisted decisions** (7.3), consistent with LGPD Art. 20.
- **Shadow AI treated as a governance risk**, with inventory, monitoring and sanctions (Section 10).
- **Multidisciplinary governance body**: IT, Legal, Privacy and Information Security (Section 8).
- **Escalation of high-risk cases to senior management** (Section 8).
- **Evidence-oriented**: Annex I produces an auditable record for each AI solution.
- **Honest scope on ISO standards**: alignment is conceptual and does not imply certification (Section 4).

---

## 3. Gaps Identified

| ID | Gap | Policy section | Why it matters | Priority |
|---|---|---|---|---|
| G-01 | No risk classification criteria. The policy requires risks to be classified but does not define levels or criteria. | 8.1 | Without criteria, "high risk" is decided case by case and cannot be audited consistently. | High |
| G-02 | No method for the algorithmic impact assessment. | 8.1 | ISO/IEC 42001 6.1.4 and A.5 expect a defined impact assessment process. | High |
| G-03 | No AI incident management procedure: definition of an AI incident, severity, response time, communication. | 11.1, 13 | Users are asked to report incidents, but there is no process to receive and handle them. | High |
| G-04 | Third-party and vendor AI not covered, although acquisition is in scope. | 3.2 | Most corporate AI use comes from vendors. Due diligence is a core AI risk control. | High · **Addressed** |
| G-05 | Generative AI rules limited to data input. No rules on output verification, hallucinations, intellectual property or disclosure of AI-generated content. | 7 | These are the most frequent risks in day-to-day generative AI use. | Medium |
| G-06 | No RACI matrix. Responsibilities are listed but not assigned by role and activity. | 8, 11 | A matrix makes accountability auditable. | Medium |
| G-07 | No training and awareness requirement. | — | ISO/IEC 42001 7.2 and 7.3 require competence and awareness. | Medium |
| G-08 | Minimum content of the AI inventory not defined. | 10.1 | Without mandatory fields, inventories become inconsistent and cannot support risk decisions. | Medium |
| G-09 | Log content and retention period not defined. | 9.4 | Logs must be sufficient for audit and proportionate under LGPD. | Medium |
| G-10 | No document control: approval record, review frequency, version history. | Header, 14 | Standard requirement for any corporate policy. | Low |
| G-11 | No monitoring indicators. | 12 | Periodic audits need measurable indicators. | Low |
| G-12 | Users are responsible for logging usage and human interventions. | 11.1 | Manual logging by users is hard to enforce. Logging should be primarily a system control, with users responsible for recording human review decisions. | Low |

---

## 4. Consistency and Editorial Fixes (resolved in version 2.1)

All items below were fixed in version 2.1 (September 2026), together with the standardization of the author name to Gustavo Rodrigues and the publication under CC BY 4.0.

| ID | Version | Section | Issue | Fix |
|---|---|---|---|---|
| E-01 | EN | 4.2 | The Portuguese version requires the organization to monitor Bill 2,338/2023 and update the policy. The English version omits this sentence. | Add the sentence to the English version. |
| E-02 | PT | 5.2 | "IA Gerativa" | "IA Generativa" |
| E-03 | PT | 4.2 | "Marco Legal da IA no Brasil, a qual está em tramitação" | "o qual está em tramitação" |
| E-04 | PT | 4 | "A adoção das normas ISO [...] se referem" | "refere-se" |
| E-05 | PT | 3 | "Inclui-se ao projeto de aplicação de IA" | "Incluem-se no escopo desta política" |
| E-06 | PT | Annex I | "Esta lista [...] deverá ser preenchida [...] e validado" | "e validada" |
| E-07 | EN | Header | "Issued: january 2026" | "Issued: January 2026" |

Regulatory status check (September 2026): Bill 2,338/2023 was approved by the Federal Senate in December 2024 and is still pending in the Chamber of Deputies. It is not in force. The reference in 4.2 remains correct.

---

## 5. Version 3.0 Roadmap

| Deliverable | Addresses | Type |
|---|---|---|
| Risk classification procedure (tiers and criteria, based on ISO/IEC 23894 and the EU AI Act risk approach) | G-01 | Procedure |
| AI impact assessment template | G-02 | Template |
| AI incident response procedure | G-03 | Procedure |
| AI vendor due diligence: [procedure](../procedures/ai-vendor-risk-assessment.md) and [assessment matrix](../templates/ai-vendor-risk-assessment-matrix.xlsx) | G-04 | **Done (September 2026)**. Policy text reference to be added in 3.0 |
| Generative AI usage rules: output review, IP, disclosure | G-05 | New policy section |
| RACI matrix | G-06 | Annex |
| Training and awareness requirement | G-07 | New policy section |
| AI inventory template with mandatory fields | G-08 | Template |
| Logging and retention requirements | G-09, G-12 | Policy section update |
| Document control table and version history | G-10 | Header |
| Monitoring indicators (for example: percentage of AI tools inventoried, Shadow AI cases detected, high-risk systems with a completed impact assessment) | G-11 | Annex |
| NIST AI RMF and EU AI Act added as references | Framework mapping, Section 3 | Section 4 update |

Target structure for version 3.0:

```text
ethical-ai-policy/
├── README.md
├── policy/
│   ├── en/corporate-ai-policy-v3.0.md
│   └── pt-br/politica-corporativa-ia-v3.0.md
├── procedures/
│   ├── ai-risk-classification.md
│   ├── ai-incident-response.md
│   └── ai-vendor-risk-assessment.md               done
├── templates/
│   ├── ai-impact-assessment.md
│   ├── ai-inventory.md
│   └── ai-vendor-risk-assessment-matrix.xlsx      done
└── docs/
    ├── framework-mapping.md
    └── review-and-roadmap.md
```

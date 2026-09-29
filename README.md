# Corporate Policy for the Ethical Use of Artificial Intelligence

An original, adoptable policy template that organizations can use to govern the ethical, secure and compliant use of Artificial Intelligence. Available in English and Brazilian Portuguese.

| | |
|---|---|
| **Version** | 2.1 (September 2026) |
| **Type** | Policy template, not an active policy of any organization |
| **Languages** | English, Brazilian Portuguese |
| **Aligned with** | LGPD, ISO/IEC 42001:2023, ISO/IEC 27001, OECD AI Principles, Brazil's Bill 2,338/2023 |
| **License** | [CC BY 4.0](LICENSE): free to use and adapt, with credit to the author |
| **Next version** | 3.0, see [review and roadmap](docs/review-and-roadmap.md) |

---

## Read the Policy

| Language | Read on GitHub | Official PDF |
|---|---|---|
| English | [corporate-ai-policy-v2.1.md](policy/en/corporate-ai-policy-v2.1.md) | [PDF](./Corporate%20Policy%20for%20the%20Ethical%20Use%20of%20Artificial%20Intelligence%202.1.pdf) |
| Português (Brasil) | [politica-corporativa-ia-v2.1.md](policy/pt-br/politica-corporativa-ia-v2.1.md) | [PDF](./Pol%C3%ADtica%20Corporativa%20para%20Uso%20%C3%89tico%20de%20Intelig%C3%AAncia%20Artificial%202.1.pdf) |

The Markdown versions reproduce the PDF text so the policy can be searched and version-controlled. If they differ, the PDF prevails. Previous versions are kept in [`archive/`](archive/).

---

## The Problem It Addresses

Employees adopt AI tools faster than organizations can approve them. The result is **Shadow AI**: personal or confidential data entered into unapproved tools, automated decisions without human review, and no record of which AI systems are in use.

This template gives an organization a starting point to set the rules: which AI can be used, with which data, under whose approval, with what human oversight, and with what evidence for audit.

---

## Policy Structure

| # | Section | What it establishes |
|---|---|---|
| 1 | Nature and conditions of use | Template status and what an organization must do to adopt it |
| 2 | Purpose | Five objectives, from ethical adoption to human oversight |
| 3 | Scope | Who it applies to and which AI systems are covered |
| 4 | Legal and normative references | LGPD, Bill 2,338/2023, ISO/IEC 42001, ISO/IEC 27001, OECD |
| 5 | Definitions | AI system, generative AI, Shadow AI, algorithmic bias, explainability |
| 6 | Principles | Transparency, fairness, security, privacy, human responsibility and oversight |
| 7 | Acceptable use | Prior approval, data restrictions, automated decisions, prohibited uses |
| 8 | Governance structure | Multidisciplinary AI committee, risk classification, impact assessment, escalation |
| 9 | Security and privacy | Legal basis, data subject rights, international transfers, audit logs |
| 10 | Shadow AI | Mandatory inventory, monitoring, sanctions |
| 11 | Responsibilities | Users, IT and governance |
| 12 | Monitoring and audit | Periodic audits, evidence, corrective action |
| 13 | Sanctions | Indicative disciplinary measures and ANPD notification |
| 14 | Final provisions | Adoption conditions and review cycle |
| Annex I | Compliance verification record | Auditable checklist signed by the solution owner and the governance body |

---

## Key Controls

- **Prior approval** of every AI tool by a designated governance body.
- **Prohibition of unregistered AI** and a mandatory AI inventory.
- **No personal, sensitive or confidential data** in unauthorized systems.
- **Human review** of decisions with significant impact, and notice to affected parties.
- **Algorithmic impact assessment** for high-risk AI systems.
- **Audit logs** and periodic audits of risk, bias and security.
- **Escalation** of high-risk cases to senior management.

---

## Supporting Procedures and Tools

| Document | What it does | Status |
|---|---|---|
| [AI Vendor Risk Assessment Procedure](procedures/ai-vendor-risk-assessment.md) | Vendor-agnostic method to assess AI vendors before purchase: inherent risk tiering, 30 questions in 8 weighted domains, 5 knock-out criteria, decision rules, required contract clauses and reassessment triggers | v1.0, part of policy 3.0 |
| [AI Vendor Risk Assessment Matrix](templates/ai-vendor-risk-assessment-matrix.xlsx) | Excel tool that applies the procedure to up to 3 vendors side by side and calculates score, residual risk and decision. Pre-filled with a fictional example | v1.0 |

The procedure operationalizes policy sections 3.2 (acquisition of AI), 7.1 (prior approval), 8.1 (risk classification) and 10.1 (AI inventory). It maps to ISO/IEC 42001 A.10, ISO/IEC 27001:2022 A.5.19–A.5.23, NIST AI RMF GOVERN 6 and LGPD Arts. 33 and 39.

---

## Framework Alignment

A section-by-section mapping to ISO/IEC 42001 (clauses and Annex A), NIST AI RMF and LGPD articles is in **[docs/framework-mapping.md](docs/framework-mapping.md)**.

Summary: of 23 mapped requirements, 13 are covered explicitly, 7 partially and 3 are delegated to the adopting organization. The gaps are documented, prioritized and addressed in the [version 3.0 roadmap](docs/review-and-roadmap.md).

---

## How to Adopt This Template

1. **Assign an owner** for the policy inside the organization.
2. **Set up the governance body**, with IT, Legal, Privacy and Information Security at a minimum.
3. **Adapt** the sections to the organization's structure, code of conduct and disciplinary rules.
4. **Build the AI inventory** and run Annex I for each AI solution already in use.
5. **Approve** the policy formally and publish it in the organization's policy repository.
6. **Define the review cycle** to follow regulatory changes, including Bill 2,338/2023.

Adopting organizations remain responsible for their own legal and regulatory compliance.

---

## Repository Structure

```text
ethical-ai-policy/
├── README.md
├── LICENSE                     CC BY 4.0
├── Corporate Policy for the Ethical Use of Artificial Intelligence 2.1.pdf
├── Política Corporativa para Uso Ético de Inteligência Artificial 2.1.pdf
├── policy/
│   ├── en/corporate-ai-policy-v2.1.md
│   └── pt-br/politica-corporativa-ia-v2.1.md
├── procedures/
│   └── ai-vendor-risk-assessment.md
├── templates/
│   └── ai-vendor-risk-assessment-matrix.xlsx
├── docs/
│   ├── framework-mapping.md
│   └── review-and-roadmap.md
└── archive/
    └── v2.0/                   original v2.0 PDFs
```

---

## Version History

| Version | Date | Changes |
|---|---|---|
| 2.0 | January 2026 | Initial public template. Template status, governance structure, Shadow AI controls, Annex I compliance record. |
| 2.1 | September 2026 | Current version. Editorial revision: legislative status of Bill 2,338/2023 updated, EN and PT versions aligned, wording fixes, document control table, author name standardized, published under CC BY 4.0. No change to requirements or controls. |
| 3.0 | In progress | Risk classification, impact assessment template, AI incident response, vendor due diligence, generative AI rules. See [roadmap](docs/review-and-roadmap.md). |

---

## Related Project

**[AI Autonomous Support Agent](https://github.com/gustavogg99-ctrl/ai-autonomous-support-agent)**: a Python prototype that applies the principles of this policy in practice. It shows human-in-the-loop escalation, automation boundaries, sensitive data detection and redacted audit logs.

---

## Author

**Gustavo Rodrigues**, AI Governance Specialist
[LinkedIn](https://www.linkedin.com/in/gustavo99rodrigues) · [GitHub](https://github.com/gustavogg99-ctrl)

---

## License

© 2026 Gustavo Rodrigues. Licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](LICENSE).

You may copy, adapt and use this template, including for commercial purposes, as long as you give appropriate credit: *"Based on the Corporate Policy for the Ethical Use of Artificial Intelligence by Gustavo Rodrigues, licensed under CC BY 4.0."*

---

> ⚠️ This is a template. It does not constitute legal advice and has no effect until it is adapted, validated and formally approved by an adopting organization.

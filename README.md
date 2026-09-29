# Corporate Policy for the Ethical Use of Artificial Intelligence

An original, adoptable policy template that organizations can use to govern the ethical, secure and compliant use of Artificial Intelligence. Available in English and Brazilian Portuguese.

| | |
|---|---|
| **Version** | 2.0 (January 2026) |
| **Type** | Policy template, not an active policy of any organization |
| **Languages** | English, Brazilian Portuguese |
| **Aligned with** | LGPD, ISO/IEC 42001:2023, ISO/IEC 27001, OECD AI Principles, Brazil's Bill 2,338/2023 |
| **Next version** | 3.0, see [review and roadmap](docs/review-and-roadmap.md) |

---

## Read the Policy

| Language | Read on GitHub | Official PDF |
|---|---|---|
| English | [corporate-ai-policy-v2.0.md](policy/en/corporate-ai-policy-v2.0.md) | [PDF](./Corporate%20Policy%20for%20the%20Ethical%20Use%20of%20Artificial%20Intelligence%202.0.pdf) |
| Português (Brasil) | [politica-corporativa-ia-v2.0.md](policy/pt-br/politica-corporativa-ia-v2.0.md) | [PDF](./Pol%C3%ADtica%20Corporativa%20para%20Uso%20%C3%89tico%20de%20Intelig%C3%AAncia%20Artificial%202.0.pdf) |

The Markdown versions reproduce the PDF text so the policy can be searched and version-controlled. If they differ, the PDF prevails.

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
├── Corporate Policy for the Ethical Use of Artificial Intelligence 2.0.pdf
├── Política Corporativa para Uso Ético de Inteligência Artificial 2.0.pdf
├── policy/
│   ├── en/corporate-ai-policy-v2.0.md
│   └── pt-br/politica-corporativa-ia-v2.0.md
└── docs/
    ├── framework-mapping.md
    └── review-and-roadmap.md
```

---

## Version History

| Version | Date | Changes |
|---|---|---|
| 2.0 | January 2026 | Current version. Template status, governance structure, Shadow AI controls, Annex I compliance record. |
| 3.0 | Planned | Risk classification, impact assessment template, AI incident response, vendor due diligence, generative AI rules. See [roadmap](docs/review-and-roadmap.md). |

---

## Related Project

**[AI Autonomous Support Agent](https://github.com/gustavogg99-ctrl/ai-autonomous-support-agent)**: a Python prototype that applies the principles of this policy in practice. It shows human-in-the-loop escalation, automation boundaries, sensitive data detection and redacted audit logs.

---

## Author

**Gustavo Henrique**, AI Governance Specialist
[LinkedIn](https://www.linkedin.com/in/gustavo99rodrigues) · [GitHub](https://github.com/gustavogg99-ctrl)

---

> ⚠️ This is a template. It does not constitute legal advice and has no effect until it is adapted, validated and formally approved by an adopting organization.

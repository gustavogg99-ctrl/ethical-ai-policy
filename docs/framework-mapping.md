# Framework Mapping

## Purpose

This document maps each section of the policy (version 2.1; requirements unchanged from 2.0) to the frameworks it references. It shows which requirements the policy already addresses and which ones it leaves to the adopting organization.

The mapping is a **conceptual alignment** exercise. It is not a certification assessment. ISO/IEC 42001 references are at clause and Annex A control-group level and should be checked against the licensed text of the standard before formal use.

Coverage legend:

| Level | Meaning |
|---|---|
| **Covered** | The policy states the requirement explicitly |
| **Partial** | The policy states the requirement but without the procedure, criteria or artifact needed to operate it |
| **Delegated** | The policy explicitly assigns the definition to the adopting organization |

---

## 1. Policy Sections vs Frameworks

| Policy section | ISO/IEC 42001:2023 | NIST AI RMF 1.0 | LGPD (Law 13.709/2018) | Coverage |
|---|---|---|---|---|
| 1. Nature and conditions of use | 4.3 Scope of the AIMS; 5.2 AI policy | GOVERN | Art. 50 (governance and good practices) | Delegated |
| 2. Purpose | 5.2 AI policy; A.2 Policies related to AI | GOVERN | Art. 6 (principles) | Covered |
| 3. Scope of application | 4.3 Scope; A.10 Third-party and customer relationships | GOVERN, MAP | — | Covered |
| 4. Legal and normative references | 4.1 / 4.2 Context and interested parties | GOVERN | — | Covered |
| 5. Definitions | — | MAP | Art. 5 (definitions, including sensitive data and anonymization) | Covered |
| 6. AI usage principles | 5.2 AI policy; A.2 | GOVERN (trustworthiness characteristics) | Art. 6 (transparency, non-discrimination, security, accountability) | Covered |
| 7.1 Authorization and control | 8 Operation; A.6 AI system life cycle; A.9 Use of AI systems | GOVERN, MANAGE | — | Partial |
| 7.2 Data use | A.7 Data for AI systems | MAP, MANAGE | Arts. 6, 7 and 11 (principles and legal bases) | Covered |
| 7.3 Automated decisions | A.8 Information for interested parties; A.9 | GOVERN, MANAGE | Art. 20 (review of automated decisions) | Covered |
| 7.4 Improper use | A.9 Use of AI systems | GOVERN | — | Covered |
| 8. AI governance structure | 5.1 Leadership; 5.3 Roles and responsibilities; A.3 Internal organization | GOVERN | Art. 50 | Partial |
| 8.1 Risk classification | 6.1.2 AI risk assessment; 6.1.3 AI risk treatment | MAP, MEASURE, MANAGE | — | Partial |
| 8.1 Algorithmic impact assessment | 6.1.4 AI system impact assessment; A.5 Assessing impacts of AI systems | MAP | Art. 38 (data protection impact report) | Partial |
| 9.1 Anonymization / legal basis | A.7 | MANAGE | Arts. 7, 11 and 12 | Covered |
| 9.2 Deletion and correction | A.7 | MANAGE | Art. 18 (data subject rights) | Covered |
| 9.3 International transfers | A.7 | MANAGE | Art. 33 | Covered |
| 9.4 Usage logs | 7.5 Documented information; A.6 | MEASURE | Art. 37 (records of processing) | Partial |
| 10. Shadow AI prevention | A.4 Resources for AI systems (inventory); A.9 | GOVERN, MAP | — | Covered |
| 11. Responsibilities | 5.3 Roles; 7.3 Awareness; A.3 | GOVERN | — | Partial |
| 12. Monitoring, audit and control | 9.1 Monitoring; 9.2 Internal audit; 10.2 Nonconformity and corrective action | MEASURE, MANAGE | — | Partial |
| 13. Sanctions | 7.3 Awareness | GOVERN | Art. 48 (incident communication to ANPD) | Delegated |
| 14. Final provisions (review cycle) | 9.3 Management review; 10.1 Continual improvement | GOVERN | — | Delegated |
| Annex I. Compliance record | 7.5 Documented information | GOVERN, MANAGE | Art. 37 | Covered |

---

## 2. Summary

| Coverage | Sections |
|---|---|
| Covered | 13 |
| Partial | 7 |
| Delegated | 3 |

The policy is strong on **principles, data protection and acceptable use**. It is less complete where it depends on operational artifacts: risk classification criteria, the impact assessment method, roles in matrix form, AI incident handling and third-party AI.

This is expected for a policy. In an ISO/IEC 42001 management system, the policy is supported by procedures and records. The gaps and the planned supporting documents are listed in [`review-and-roadmap.md`](review-and-roadmap.md).

---

## 3. Frameworks Not Yet Referenced

| Framework | Relevance | Planned action |
|---|---|---|
| NIST AI Risk Management Framework 1.0 | Widely used AI risk vocabulary (Govern, Map, Measure, Manage) | Add as a normative reference in version 3.0 |
| EU AI Act (Regulation (EU) 2024/1689) | Risk-based obligations for organizations operating in or selling to the EU | Add as a reference for multinational adopters |
| ISO/IEC 23894:2023 | Guidance on AI risk management | Use as the basis for the risk classification procedure |

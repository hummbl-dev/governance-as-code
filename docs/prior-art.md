# Prior Art and Adjacent Ecosystem References

This document collects public prior art and adjacent ecosystem references relevant to `governance-as-code`.

> **Important:** These are **references**, not adopted canon. Listing a tool or framework here does not mean it is endorsed, integrated, or normatively adopted by this repository. This repo remains `seed`/`v0.1-draft` until explicitly adopted by HUMMBL authority. See [`docs/v0.1-boundary.md`](v0.1-boundary.md) and [`docs/definition.md`](definition.md) for the current non-canon posture.

## Public Prior Art

### Open Policy Agent (OPA)

- **What it does:** A general-purpose policy engine that lets teams write policy as code (in the Rego language) and evaluate it against structured data. Commonly used for admission control, authorization, and policy enforcement across cloud-native systems.
- **Relevance to this repo:** OPA demonstrates how decision logic can be expressed as version-controlled, testable, machine-evaluable source. The pattern of separating policy from application code and evaluating it against input data maps closely onto governance gates expressed as reviewable source.
- **Public docs:** https://www.openpolicyagent.org/

### AWS Config

- **What it does:** A service that records configuration state of AWS resources and evaluates that state against configurable rules, enabling continuous compliance assessment and configuration change tracking.
- **Relevance to this repo:** AWS Config illustrates continuous, evidence-oriented evaluation of operational state against declared rules — a useful analog for how governance-as-code might express "desired governance state" and detect drift.
- **Public docs:** https://docs.aws.amazon.com/config/

### Azure Policy

- **What it does:** A policy-as-code service in Azure that enforces compliance rules over resources using declarative policy definitions and initiatives, with built-in compliance evaluation and remediation.
- **Relevance to this repo:** Azure Policy shows how declarative, auditable policy definitions can be assigned, evaluated, and reported against at scale — relevant to expressing review gates and institutional constraints as inspectable source.
- **Public docs:** https://learn.microsoft.com/azure/governance/policy/

### GCP Organization Policy

- **What it does:** Google Cloud's organization policy service that lets administrators define constraints on resource usage across the organization hierarchy, enforced centrally and inherited by projects and folders.
- **Relevance to this repo:** Demonstrates hierarchical, inherited governance constraints applied as declarative configuration — relevant to how governance-as-code might represent decision authority and constraints that cascade across teams or repos.
- **Public docs:** https://cloud.google.com/resource-manager/docs/organization-policy/

### Chef InSpec

- **What it does:** An open-source framework for writing compliance, security, and policy controls as code, runnable against infrastructure to produce pass/fail evidence and audit reports.
- **Relevance to this repo:** InSpec is a strong example of controls-as-code with explicit evidence output, directly relevant to how governance-as-code might produce auditable, reviewable evidence for decision gates.
- **Public docs:** https://docs.chef.io/inspec/

## Adjacent Ecosystem

### SOC 2 automation tools

- **What they do:** Tools that automate evidence collection, control mapping, and continuous monitoring required for SOC 2 Type I/II audits, reducing manual audit preparation.
- **Relevance to this repo:** SOC 2 automation demonstrates the pattern of turning control frameworks into continuously-collected, reviewable evidence — adjacent to governance-as-code's goal of producing auditable decision records.
- **Public reference:** https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome.html (SOC 2 framework)

### NIST CSF tools

- **What they do:** Tooling aligned to the NIST Cybersecurity Framework (CSF) that helps organizations assess, manage, and document cybersecurity posture across the framework's core functions (Identify, Protect, Detect, Respond, Recover).
- **Relevance to this repo:** NIST CSF tooling shows how a control framework can be operationalized into measurable, documented state — relevant to governance-as-code's interest in control frameworks and evidence.
- **Public reference:** https://www.nist.gov/cyberframework

### ISO 27001 tooling

- **What they do:** Tools supporting ISO/IEC 27001 information security management systems (ISMS), including risk assessment, control implementation tracking, and audit-readiness evidence management.
- **Relevance to this repo:** ISO 27001 tooling illustrates structured management of controls, risks, and evidence over time — adjacent to governance-as-code's concerns with review gates, provenance, and auditability.
- **Public reference:** https://www.iso.org/standard/27001

### Vanta

- **What it does:** A compliance automation platform that connects to cloud and SaaS tools to continuously monitor security controls, collect audit evidence, and streamline SOC 2, ISO 27001, HIPAA, and similar audits.
- **Relevance to this repo:** Vanta exemplifies continuous, automated evidence collection against control frameworks — a concrete instance of the compliance-automation pattern governance-as-code may reference.
- **Public docs:** https://docs.vanta.com/

### Drata

- **What it does:** A compliance automation platform that automates evidence collection, control monitoring, and audit readiness for frameworks such as SOC 2, ISO 27001, HIPAA, and GDPR.
- **Relevance to this repo:** Drata represents the same continuous-compliance-evidence pattern as other automation tools, relevant as an adjacent ecosystem reference.
- **Public docs:** https://docs.drata.com/

### Secureframe

- **What it does:** A compliance automation platform that helps organizations achieve and maintain compliance across frameworks (SOC 2, ISO 27001, HIPAA, etc.) through automated control monitoring and evidence collection.
- **Relevance to this repo:** Secureframe is another adjacent reference for automated control monitoring and audit evidence, useful as context for the compliance-automation landscape.
- **Public docs:** https://secureframe.com/

## Vocabulary References

These terms are collected as shared vocabulary for the domain. They are descriptive references, not normative definitions adopted by this repo.

| Term | Working sense | Public reference |
| --- | --- | --- |
| governance-as-code | Representing decision rights, review gates, escalation paths, and institutional constraints as version-controlled, reviewable, testable source. | This repo — [`docs/definition.md`](definition.md) |
| compliance automation | Automating evidence collection, control monitoring, and audit readiness against recognized frameworks. | https://www.nist.gov/cyberframework , https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome.html |
| control mapping | Relating implemented controls to framework requirements to demonstrate coverage. | https://www.nist.gov/cyberframework |
| audit evidence | Artifacts collected to demonstrate that a control is operating effectively. | https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/sorhome.html |

## Key Concepts

These concepts recur across the prior art and adjacent ecosystem above. They are collected here as orientation, not as adopted doctrine.

- **Policy engines** — Systems that evaluate declarative policy/rules against input data and return decisions (e.g., OPA, Azure Policy). Relevant to how governance-as-code might express and evaluate gates.
- **Control frameworks** — Structured sets of controls (SOC 2, NIST CSF, ISO 27001) that define what "good" looks like for a domain. Relevant as a reference model for governance controls.
- **Evidence collection** — The practice of continuously gathering artifacts that demonstrate control operation. Central to compliance automation tools and relevant to governance-as-code's auditability goal.
- **Audit trails** — Immutable, reviewable records of what was decided, when, by whom, and against what state. Relevant to governance-as-code's provenance and review-history principles.
- **Attestation** — A formal assertion (by a human or system) that a condition holds. Relevant to how governance-as-code might represent approval, review, and sign-off as reviewable source.

## Non-canon reminder

This document is a reference collection. Nothing here is adopted operating canon for `governance-as-code` or HUMMBL. Tools and frameworks are listed to orient contributors and readers, not to prescribe integration or endorsement. Per [`docs/principles.md`](principles.md): separate examples from adopted operating canon.

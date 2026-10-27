# Using Open Source

<!--
########################################################################################
For OSPO Staff: How to Use This Template

1. Replace placeholders in the body text like [Company Name] with your company information.
2. Verify completeness using the customization checklist.
3. Refer to the customization guide at the end to expand content based on your company's context.

Simply replacing placeholders allows immediate use as internal documentation.
Expanding text according to the guide yields an even more practical document.
########################################################################################
-->

In modern software engineering, leveraging open source software (OSS) is indispensable.
Proper adoption significantly accelerates development velocity and boosts product quality.
However, teams must navigate critical considerations around license compliance and security.

This section provides a practical guide for effective open source adoption—systematically organizing information engineers need daily across discovery, evaluation, integration, and continuous management.

## Baseline Open Source Adoption Lifecycle

Adopting open source effectively requires a structured, phased approach:

1. Discovery and Selection

    When planning new open source adoption, check the [Approved Internal OSS Inventory](../using/oss-inventory.md) first.
    This catalog lists software pre-assessed for license compatibility, security posture, technical quality, community health, and long-term viability.
    Selecting pre-approved components significantly reduces lead time and operational risk. Note that if your proposed usage differs from previous approvals, re-verifying license compatibility is required.

    If suitable software is not listed, follow [Finding Open Source Software](../using/finding-oss.md) to discover candidates matching project requirements, leveraging GitHub search techniques, trusted indexes, and screening protocols.

2. Evaluation and Verification

    Upon identifying candidates, evaluate them holistically following [Evaluating Open Source Software](../using/evaluation.md)—assessing technical fit, license compatibility, security posture, community vitality, and maintainability.

    Conduct evaluations in phases to maintain efficiency without overlooking critical risks across three stages: Initial Screening, Technical Evaluation, and Security & Risk Assessment.

3. License Verification

    License evaluation is critical yet frequently overlooked.
    Build foundational understanding via [What Is a License?](../compliance/what-is-a-license.md), paying special attention to [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md) and [OSS with Commercial License Options](../compliance/oss-with-commercial-license-options.md).

    Because license impact varies dramatically by deployment model, evaluate compatibility against clear project requirements.

    Primary deployment models include:
    - **Internal Operations Only**: Usage restricted strictly to internal development and runtime systems.
    - **External Distribution**: Commercial software products, embedded hardware devices, or deliverables for client projects.
    - **SaaS Delivery**: Offering capabilities as cloud services over network APIs.

    Because distribution models trigger distinct compliance obligations, evaluate licenses against specific delivery channels.

4. Integration and Management

    Following license clearance, proceed with technical integration using security best practices—downloading from official registries, verifying hashes, and scanning for vulnerabilities.

    Register adopted open source components in the internal component catalog ([Approved Internal OSS Inventory](../using/oss-inventory.md)) to streamline license tracking, security monitoring, and dependency management.

## Importance of License Compliance

Open source licenses represent legal copyright permissions granting software usage under specific terms. "Open source" does not mean unrestricted usage; every license carries distinct conditions and obligations.

Licensing non-compliance creates legal risks while threatening project schedules through mandatory refactoring, re-architecting, or emergency component replacement. Proactive evaluation and management mitigate these risks.

## Primary License Categories

Open source licenses fall into tiers based on obligation scopes:

**Permissive Licenses (MIT, BSD, Apache-2.0)**
Impose minimal obligations, primarily retaining copyright notices and license text without requiring source code disclosure.

**Licenses with Source Code Disclosure Obligations (GPL, AGPL)**
Enforce copyleft reciprocity on derivative works, directly shaping architecture. Certain licenses (AGPL) trigger source disclosure obligations upon network service delivery, demanding vigilance in SaaS environments.

**Component-Level Source Disclosure Licenses (LGPL, MPL)**
Occupy a middle ground, relaxing copyleft disclosure obligations across dynamic linking or module boundaries.

For details, refer to [What Is a License?](../compliance/what-is-a-license.md) and [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md).

## Security Considerations

Managing open source security represents a critical modern engineering requirement, demanding continuous vulnerability monitoring, dependency management, and supply chain security.

### Pre-Integration Security Screening

When adopting new open source, perform the following security checks:

- **Source Trust**: Download exclusively from official registries or verified package managers.
- **Checksum Verification**: Confirm file integrity against published hashes.
- **Vulnerability Scanning**: Screen dependencies against CVE databases.
- **Dependency Analysis**: Evaluate transitive dependency trees for security risks.

For details, see the security evaluation section in [Evaluating Open Source Software](../using/evaluation.md).

## When to Consult the OSPO

Consult the OSPO prior to integration when encountering the following scenarios:

- **Licenses with complex compliance terms** (source code disclosure obligations, copyleft terms, mandatory attribution propagation).
- **Components potentially requiring commercial licensing**.
- **Security vulnerabilities requiring specialized risk review** (consult Security).
- **Adopting software not listed on the Approved Internal OSS Inventory**.

If your project team possesses strong open source expertise, you may execute evaluations autonomously. (*The OSPO exists to empower project decision-making, not to act as a bottleneck proxy.*)

### Consultation Checklist

When consulting the OSPO, provide the following details:

- Component name, repository URL, and version.
- Intended deployment model (Internal tool, distributed binary, embedded device, SaaS offering).
- Details of any source code modifications.
- Project timelines and background constraints.
- Technical alternatives evaluated.
- Relevant customer contracts or EULA drafts (even early drafts are helpful).

---
<!--
########################################################################################
About the Customization Checklist

This checklist comprehensively organizes items to consider when designing or refining OSS operations.
Implementation items and priorities vary depending on organizational scale, business model, OSS usage, and maturity.
You do not need to check every item.
Adopt and implement items incrementally based on organizational goals and priorities.
########################################################################################
-->

## Customization Checklist

- [ ] Specified location and governance policy for the Approved Internal OSS Inventory.
- [ ] Documented integration procedures with existing approval workflows and CI/CD chains.
- [ ] Created and linked OSPO consultation intake templates/forms.
- [ ] Clarified emergency escalation pathways and security contacts.
- [ ] Published target SLA turnaround times for OSPO consultations.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Managing Approved Internal Inventories

Maintaining an approved internal OSS list requires continuous OSPO commitment to update records, handle developer inquiries, and maintain catalog criteria transparently.
Balance catalog governance against the risk of creating a misconception that "unlisted OSS cannot be used." Most enterprises encourage autonomous team selection while reserving OSPO consultations for high-risk licenses.

■ Aligning with Existing Engineering Workflows

Integrate open source governance into established toolchains, CI/CD pipelines, and escalation paths.

■ Streamlining Consultations

Foster a culture where early consultation is seen as a risk mitigation enabler rather than a development blocker. Provide clear consultation forms, robust FAQs, and SLA targets to empower autonomous developer decision-making over time.

########################################################################################
########################################################################################
-->

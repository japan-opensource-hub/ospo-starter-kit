# Licenses with Source Code Disclosure Obligations

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

Among open source licenses, those imposing source code disclosure obligations require heightened vigilance.
While general concepts are covered in **[What Is a License?](../compliance/what-is-a-license.md)**, this document details the specific characteristics of source disclosure licenses and their business impacts.

## Why These Licenses Require Heightened Vigilance

Licenses with source code disclosure obligations (copyleft licenses) are designed to preserve software freedom permanently.

Unlike permissive licenses (MIT, BSD), copyleft licenses may mandate that modifications or closely combined works be distributed under identical licensing terms, including source code availability. What constitutes "close combination" varies by license and technical mechanism (static linking, dynamic linking, IPC).

Because copyleft scope boundaries can be complex, proprietary software combined with copyleft components risks triggering unintended source disclosure obligations.
This presents potential impacts on corporate intellectual property strategies and competitive differentiators, demanding careful management.

However, using copyleft software does not inherently represent unacceptable risk.
Under proper understanding and compliance, organizations leverage copyleft software safely.
The key lies in evaluating license terms against business deployment models to make informed architectural choices.

## Understanding the Business Impacts

### Triggering Source Code Disclosure

The defining feature of copyleft licenses is mandatory source code disclosure for derivative works.
Modifying or bundling copyleft software into distributed products requires providing corresponding source code under identical license terms.

### Operational Impacts by Deployment Model

- **Internal Operations Only**
    Using copyleft software strictly within internal operations does not constitute external distribution under most copyleft licenses, avoiding source disclosure obligations.

- **Binary Distribution**
    Distributing binaries or embedded software externally triggers requirements to provide corresponding source code.

- **SaaS Delivery**
    Network service delivery impacts vary by license. The Affero GPL (AGPL) explicitly defines network access as triggering source code disclosure obligations to service users.

### Copyleft Scope and Architectural Coupling

Copyleft reciprocity varies by license family and technical coupling:

**Strong Copyleft (GPL v2/v3)**
Static or dynamic linking combines application components into a single derivative work, extending GPL terms across the combined work.

**Weak / Component Copyleft (LGPL)**
Requires disclosing source code for the LGPL library itself, alongside providing object code or build scripts allowing users to relink modified libraries. Proprietary application source code linking to unmodified LGPL libraries remains private, though LGPL compliance obligations still apply.

For detailed license descriptions, see **[Types of Licenses](../compliance/license-types.md)**.

## Usage Guidelines

### Pre-Adoption Checklist

Evaluate new open source software against this checklist prior to adoption:

1. **Identify the License**: Verify terms in README, LICENSE files, or package metadata.
2. **Evaluate Deployment Models**: Determine whether usage is internal-only, distributed, or delivered via SaaS.
3. **Assess Technical Coupling**: Analyze architectural integration methods (linking, IPC, network APIs).
4. **Evaluate Permissive Alternatives**: Determine if permissively licensed alternatives satisfy technical requirements.

### Scenarios Requiring Care

- **Development Environments**
  Ensure tools or libraries used in build pipelines do not inadvertently bundle into final production deliverables.

- **Releasing Proprietary Software as Open Source**
  Scan proprietary codebases prior to public release to ensure copyleft components are accounted for.

- **M&A and Tech Transfers**
  Auditing copyleft compliance is critical during corporate acquisitions or technology transfers, as inherited copyleft obligations pass to acquiring entities.

## Consult the OSPO When Uncertain

Copyleft licenses offer immense value when managed correctly.
When licensing interpretations are unclear, consult the OSPO.
Refer to "[What Is an OSPO?](../about/ospo.md)" for contact details.

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

- [ ] Established Legal-approved criteria defining "derivative works" and "combination."
- [ ] Defined exact scope boundaries for source code disclosure.
- [ ] Formulated classification standards for shareable vs. non-shareable code.
- [ ] Defined internal criteria for "distribution" (including transfers to subsidiaries or partners).
- [ ] Established corporate policy regarding AGPL usage in SaaS products.
- [ ] Created mapping tables linking architectural coupling methods to copyleft scope.
- [ ] Curated external reference links explaining complex copyleft interpretations.
- [ ] Published developer guidelines for copyleft software integration.
- [ ] Defined policies for Software Composition Analysis (SCA) tool usage.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Formulating Corporate Stances

Avoid blanket bans on copyleft software; instead, establish clear corporate interpretations.
Work with Legal to define internal boundaries for derivative works, distribution, and AGPL usage in SaaS.

■ Coupling Methods and Copyleft Scope

Provide clear architectural mapping tables illustrating how dynamic linking, static linking, microservices, and IPC interact with copyleft licenses.

■ Process Integration

Empower development teams to evaluate copyleft software autonomously through clear decision trees, reserving OSPO consultations for complex edge cases.

########################################################################################
########################################################################################
-->

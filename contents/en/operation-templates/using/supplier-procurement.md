# Procuring OSS from Suppliers

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

Procuring software containing open source software (OSS) from third-party suppliers requires structured management workflows.
Unmanaged supplier OSS usage risks introducing severe post-delivery compliance violations and security vulnerabilities, jeopardizing project success.

This guide provides practical procedures for procuring software containing OSS from suppliers—covering contract terms through post-delivery verification to minimize operational risk.

## Supplier Procurement Workflow

Procuring software containing OSS requires a phased approach:

**Pre-Procurement Contracting and Alignment**

Establishing clear OSS policies and review workflows during contract negotiations prevents post-delivery licensing surprises and costly rework.

**Post-Delivery Verification and Remediation**

Conducting thorough verification upon delivery in accordance with contract terms ensures rapid remediation of identified issues.

## Pre-Procurement Alignment Requirements

Establish and record mutual agreement with suppliers on the following items prior to contract execution or development kickoff:

**Scope of Permitted Usage**

We recommend permitting suppliers to use OSS while making prior verification of the OSS they use the baseline expectation.
On that basis, it is easier to operate if you set review criteria by license type: OSS under licenses with few obligations (MIT, BSD, etc.) has relatively limited verification requirements, whereas OSS under licenses with source code disclosure obligations (GPL, AGPL, etc.) calls for careful evaluation of the impact on your own products.

For license details, see [What Is a License?](../compliance/what-is-a-license.md) and [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md).

**Pre-Consultation and Approval Processes**

Define approval workflows for suppliers adopting new OSS components:

- **Early Consultation**: Set up a mechanism for suppliers to consult with you about OSS they are considering, before development begins.
- **Stated Criteria**: Clarify, as far as practical, which conditions require attention and what perspectives inform the decision.
- **Sharing the Internal OSS Inventory for Reference**: If you maintain an inventory of OSS already evaluated and adopted internally, you can share it as reference information. Note that usage conditions change with the business use case and with combinations of other software, so suppliers still need to perform their own case-by-case verification.

### OSS Inventory Submission Requirements

**Submission Milestones**

Define explicit milestones for suppliers to submit OSS inventories:

- **Architecture Review Phase**: Submit proposed OSS inventories upon finalizing architecture designs.
- **Development Phase**: Report newly added OSS components as development progresses.
- **Pre-Delivery Phase**: Submit complete, finalized OSS inventories for all release deliverables.

Setting milestones too late hampers remediation, while requiring reporting too early creates administrative churn; establish milestone cadences appropriate for project scale.

**Inventory Data Fields**

Require suppliers to provide the following data fields in OSS disclosures:

- OSS component name and exact version.
- License type and SPDX identifier.
- Source repository URL.
- Usage scope and technical coupling mechanism.
- Details of modifications made to the OSS component.
- Dependency tree details (transitive dependencies).

### Executing License Clearance

**Defining Clearance Responsibilities**

Clarify boundaries and expectations for license clearance workflows:

- **Responsible Entity**: Specify whether clearance is executed by supplier, buyer, or jointly.
- **Milestones**: Specify development phases where clearance must occur.
- **Acceptance Criteria**: Define explicit clearance criteria for delivery approval.
- **Tooling Mandates**: Specify required Software Composition Analysis (SCA) tooling if applicable.

**Submitting Clearance Deliverables**

Define required formats for clearance deliverables—such as automated SCA scan reports or audited compliance checklists.

### Security Requirements

**Vulnerability Scanning Requirements**

Define security scanning requirements for supplier deliverables:

- **Scanning Cadence**: Require scans during development and prior to final delivery.
- **Acceptable Severity Levels**: For example, Critical/High vulnerabilities are not acceptable; Medium and below require consultation.
- **Remediation Policy**: Define how discovered vulnerabilities are to be handled (patching, workarounds, switching to alternative OSS).

For details, see the security evaluation section in [Evaluating Open Source Software](../using/evaluation.md).

**Post-Delivery Vulnerability Response**

It is important to agree in advance on how vulnerabilities discovered after delivery will be handled:

- The obligation to provide security updates during the maintenance period.
- The communication channels to use when a serious vulnerability is found.
- The standard timeframe within which updates will be provided.

### Contractual Provisions

**Legal Terms**

Legal arrangements concerning OSS usage require careful consideration in coordination with Legal.
The following are examples of items commonly considered; always obtain Legal's confirmation on what is actually written into the contract:

- Responsibility and response if non-compliance with license conditions comes to light.
- Handling of intellectual property issues arising from OSS included in deliverables.
- The scope of warranties and disclaimers concerning OSS usage.
- Handling of cases where a source code provision obligation arises.

## Post-Delivery Verification Workflows

Upon receiving supplier deliverables, execute verification checks against contractual agreements:

### OSS Inventory Verification

**Auditing Submitted Disclosures**

Audit supplier OSS disclosures against the following criteria:

- **Completeness**: Confirm all required fields (names, versions, licenses) are provided.
- **Consistency**: Verify recorded license terms match official records (e.g., [SPDX License List](https://spdx.org/licenses/)).
- **Timeliness**: Confirm inventories reflect final release builds rather than outdated drafts.

These checks verify list completeness and accuracy rather than placing full audit burdens on the buyer. Automated tools enhance verification precision.

**Automated Tool Verification**

When feasible, use SCA or SBOM tools to audit supplier deliverables against submitted inventories, uncovering omitted components or misidentified licenses. Alternatively, require suppliers to submit automated SCA scan results alongside deliverables.

### License Clearance Verification

**Reviewing Clearance Rigor**

Review supplier license clearance results for operational rigor:

- Confirm all embedded OSS components were audited.
- Verify component licenses, technical coupling, and modifications were reviewed.
- Confirm deliverables satisfy pre-agreed acceptance criteria.

**Verifying License Compatibility**

Verify individual OSS component licenses against intended deployment models (internal use, binary distribution, SaaS delivery), paying close attention to:

- Scope impacts from copyleft licenses (GPL, AGPL).
- Dependencies requiring commercial licenses.
- Incompatible license combinations within deliverables.

For details, see [What Is a License?](../compliance/what-is-a-license.md) and [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md).

### Issue Remediation Protocols

**Classifying Issues by Severity**

Categorize identified non-compliance issues by severity to drive appropriate response workflows:

**Critical Issues (Immediate Response Required)**

- OSS under a license with source code disclosure obligations is used improperly, without those obligations being met.
- Critical/High severity vulnerabilities are present.
- The deliverable is not in compliance with license conditions.
- A large volume of undeclared OSS is included.

**Minor Issues (Resolvable Through Discussion and Adjustment)**

- Omissions or errors in the OSS inventory.
- Vulnerabilities at Medium severity or below.
- Insufficient documentation of modifications.

**Executing Remediation**

Execute remediation based on issue severity:

- **Notifying the Supplier and Requesting an Explanation**: Communicate the issue clearly and ask the supplier to explain the situation.
- **Requesting Corrective Action**: Present the specific corrections required (replacing the OSS, fixing vulnerabilities, completing license information, etc.) along with a deadline.
- **Considering Alternatives**: Where correction is difficult, discuss switching to alternative OSS or changing how it is used.
- **Acceptance Decision**: Confirm that corrective actions have been carried out, then decide whether to accept the deliverable.

Critical issues require escalation to Legal and, in some cases, executive management.

## When to Consult the OSPO

Consult the OSPO during supplier procurement in the following scenarios:

- **Drafting Procurement Contracts**: Incorporating open source clauses into supplier master agreements.
- **Reviewing Complex Clearance Findings**: Evaluating ambiguous licensing terms or vulnerability risks.
- **Critical Non-Compliance Findings**: Handling unapproved copyleft components or severe vulnerabilities.
- **Disagreements with Suppliers**: Resolving technical or legal licensing disputes with suppliers.

Early consultation prevents risk expansion and ensures appropriate remediation.

Establishing clear supplier expectations during contracting coupled with diligent delivery verification minimizes compliance risks.

Contact the OSPO with questions. Refer to "[What Is an OSPO?](../about/ospo.md)" for staff contacts.

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

- [ ] Decided the scope of the internal OSS inventory to be shared with suppliers.
- [ ] Standardized OSS inventory submission formats (Excel, CSV, SPDX, CycloneDX).
- [ ] Established Legal-approved contract clause guidelines for OSS procurement.
- [ ] Defined severity tiers and decision-making authority for procurement non-compliance.
- [ ] Established escalation pathways and contacts.
- [ ] Established periodic communication cadence with key suppliers.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Providing an OSS Inventory to Suppliers

Consider the following when sharing an inventory of already-adopted OSS with suppliers:
 * Set the scope of the inventory appropriately (all OSS, or only certain categories).
 * Establish the update frequency and the maintenance structure.
 * Clarify the procedure for when a supplier wants to use OSS that is not on the inventory.

In the early stages, a realistic approach is to list only major OSS and expand in stages.

■ Standardizing the Inventory Submission Format

Standardizing the submission format makes post-delivery analysis more efficient:
 * Consider adopting standard Software Bill of Materials (SBOM) formats (SPDX, CycloneDX, etc.).
 * If you are not yet ready to manage standard SBOM formats, consider collecting the information in Excel/CSV form.

Also consider adjusting the level of detail you request based on the supplier's technical maturity and size.

■ Contract Clause Guidelines

Because these involve company-specific legal risk, we recommend keeping this to general guidance:
 * Establish a contract review process in coordination with Legal.
 * Maintain internal guidelines on OSS-related contract clauses.
 * Document cautionary points based on past issues.

If you provide template contract language, state clearly that it is illustrative and requires Legal's confirmation.
For legally binding documents, avoid decisions by the OSPO alone and always involve Legal.

■ Establishing the Issue Response Process

Aligning with internal decision-making processes is essential:
 * Define severity levels for issues and who has decision authority at each level.
 * Prepare communication templates for suppliers.
 * Set standard correction periods according to the type of issue.
 * Establish escalation paths and contacts.

Accumulating past issues and how they were handled, and using them as a knowledge base, makes future responses more efficient.

■ Maturing the Process in Stages

Throughout this guide, we recommend continuously improving the following:
 * Start with basic requirements and add detail gradually through actual operation.
 * Collect feedback from suppliers to improve feasibility.
 * Document both successes and failures to promote organizational learning.
 * Set realistic requirements that account for the supplier's situation, rather than making one-sided demands.

########################################################################################
########################################################################################
-->

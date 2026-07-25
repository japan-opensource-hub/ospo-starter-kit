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

While permitting supplier OSS usage, establish pre-use notification requirements as a baseline.
Tier review requirements by license risk—permissive licenses (MIT, BSD) require streamlined checks, whereas copyleft licenses (GPL, AGPL) demand rigorous evaluation regarding architectural impacts on proprietary codebases.

For license details, see [What Is a License?](../compliance/what-is-a-license.md) and [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md).

**Pre-Consultation and Approval Processes**

Define approval workflows for suppliers adopting new OSS components:

- **Early Notification**: Mandate that suppliers disclose proposed OSS components prior to development.
- **Clear Criteria**: Provide explicit guidelines detailing restricted license terms and security standards.
- **Reference Catalog Sharing**: Share approved internal OSS inventories as reference guidelines. Note that because license implications depend on specific deployment contexts, suppliers remain responsible for conducting independent compliance reviews.

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
- **Severity Thresholds**: Prohibit unmitigated Critical/High vulnerabilities; require formal risk reviews for Medium issues.
- **Remediation SLA**: Define remediation expectations (patching, workarounds, component replacement).

For details, see the security evaluation section in [Evaluating Open Source Software](../using/evaluation.md).

**Post-Delivery Vulnerability Response**

Establish post-delivery vulnerability protocols in supplier contracts:

- Mandatory security update provisions during maintenance windows.
- Emergency notification SLA for newly disclosed Critical vulnerabilities.
- Standard response SLAs for patch delivery.

### Contractual Provisions

**Legal Terms**

Collaborate with Legal to incorporate open source terms into procurement contracts:

- Liability and indemnification for licensing non-compliance.
- Intellectual property warranty coverage for embedded open source components.
- Warranty scopes and disclaimers for open source software.
- Remedies and source code delivery obligations triggered by copyleft terms.

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

**Critical Issues (Immediate Escalation & Blockers)**

- Copyleft software deployed in non-compliant architectures without fulfilling source disclosure terms.
- Unmitigated Critical/High security vulnerabilities.
- Material licensing non-compliance.
- Massive unapproved OSS additions.

**Minor Issues (Remediated via Technical Alignment)**

- Minor inventory typos or omitted metadata.
- Low/Medium vulnerability findings.
- Incomplete modification documentation.

**Executing Remediation**

Execute remediation based on issue severity:

- **Issue Notification**: Issue formal remediation requests detailing non-compliance findings.
- **Mandatory Remediation**: Require suppliers to replace components, patch vulnerabilities, or supply missing notices within set SLAs.
- **Alternative Evaluation**: Discuss architectural refactoring if component replacement is infeasible.
- **Final Acceptance**: Re-audit deliverables post-remediation prior to formal acceptance.

Escalate critical non-compliance issues to Legal and executive leadership immediately.

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

- [ ] Defined sharing scope for supplier-facing approved OSS catalogs.
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

■ Standardizing Inventory Submission Formats

Adopting standard Software Bill of Materials (SBOM) formats (SPDX, CycloneDX) streamlines post-delivery analysis. Use spreadsheet formats (Excel/CSV) if automated SBOM pipelines are not yet established.

■ Contract Clause Guidelines

Work with Legal to establish contract review workflows and boilerplate open source clauses for supplier contracts. Include explicit disclaimers that template clauses require Legal review before execution.

■ Procurement Incident Response

Define decision-making authority for procurement non-compliance, prepare communication templates, and establish standard SLAs for supplier remediation.

########################################################################################
########################################################################################
-->

# How to Use This Guide (For End Users)

## Start Here

- Gateway to internal open source adoption:
  - -> [[Company Name] Open Source Guide](./about/opensource-guide.md)

## Understanding Open Source

- What open source is and why we use it:
  - -> [About Open Source](./about/about-opensource.md)
- Advantages of leveraging open source:
  - -> [Benefits of Open Source](./about/benefits.md)
- The internal team driving open source strategy (OSPO):
  - -> [What Is an OSPO?](./about/ospo.md)
- Applying open source methodologies internally (InnerSource):
  - -> [What Is InnerSource?](./about/innersource.md)

## Practical OSS Adoption Guide

- Practical workflow covering discovery, evaluation, license verification, and deployment:
  - -> [Using Open Source](./using/using-oss.md)

## Finding Open Source Software

- Can existing OSS solve your problem?
- Where to search?
- [Approved Internal OSS Inventory](./using/oss-inventory.md) / Recommended OSS:
  - -> [Finding Open Source Software](./using/finding-oss.md)

## Evaluating Open Source Software

- Technical suitability
- High-level license compatibility
- Security vulnerabilities and maintenance health (commit frequency, responsiveness)
- Dependency trees (transitive dependencies)
  - -> [Evaluating Open Source Software](./using/evaluation.md)

## Understanding Licensing Fundamentals

- Open source comes with terms and conditions
- Differences between distribution, SaaS, and internal use
- Deployment models (Internal / Distribution / SaaS)
- Overview of open source license compliance:
  - -> [Open Source License Compliance](./compliance/license-compliance.md)
- What a license is:
  - -> [What Is a License?](./compliance/what-is-a-license.md)
- License categories and classifications:
  - -> [Types of Licenses](./compliance/license-types.md)

## Cases Requiring Care

- Scenarios triggering source disclosure obligations
- Scenarios requiring commercial licensing
- "Looks like OSS, but isn't OSS"
  - -> [Licenses with Source Code Disclosure Obligations](./compliance/source-disclosure-licenses.md) / [OSS with Commercial License Options](./compliance/oss-with-commercial-license-options.md)

## Using Open Source in Engineering & Procurement

- In-house development
- Vendor deliverables
- Contracting requirements for outsourced or joint development (OSS disclosure lists, SBOMs, remediation SLAs)
- Logging utilized OSS metadata (inventories, evaluation logs, approval decisions)
- Purchasing commercial products, SDKs, or middleware containing embedded OSS for product integration:
  - Confirm whether procured deliverables contain OSS (subject to OSS disclosure requests)
  - -> [Procuring OSS from Suppliers](./using/supplier-procurement.md)

## Pre-Release Verification

- License compliance checks
- Notice artifact inclusion (LICENSE / NOTICE files)
- Finalizing release deliverables
- Logging OSS inventories, evaluation logs, and approval records for release builds
- Source code disclosure and modification notices where required
- Incident protocols for suspected license violations, data leaks, or security bugs
- Ensuring deliverable authenticity and provenance (code signing, SBOMs, provenance attestations)
- Contractual term verification
  - (e.g., verifying consistency between EULA/contract terms and OSS license terms; ensuring user rights under LGPL are preserved; confirming OSS license terms override conflicting proprietary restrictions)

## Post-Release Operations (Maintenance & Support)

- Fulfilling source code requests (intake channels, fulfillment procedures, source bundle packaging)
- Vulnerability and bug management (impact analysis -> mitigation/patching -> customer notifications -> post-mortems)
- Remediating post-release OSS discoveries or license issues (over-the-air updates, advisories)
- Continuous dependency and SBOM maintenance

## Troubleshooting & Consultations

- [OSS Usage FAQ](./using/usage-faq.md)
- [License FAQ](./compliance/license-faq.md)
- [Glossary](./about/glossary.md)
- [What Is an OSPO?](./about/ospo.md)
- Consulting on upstream contributions or CLA executions

## Releasing Open Source Software

- Release applications / verification checklists / official repositories / change management:
  - -> Releasing Open Source Software *(Work in Progress as of April 2026)*

## Contributing to External Open Source Projects

- Pre-approvals / review criteria / CLA & DCO handling / blanket approvals:
  - -> Contributing to Open Source *(Work in Progress as of April 2026)*

## Personal Open Source Activity Guidelines

- Confidentiality / corporate resources / employer disclaimers and affiliation templates

## Incident & Vulnerability Reporting

- Protocols for suspected license non-compliance, data leaks, or security vulnerabilities

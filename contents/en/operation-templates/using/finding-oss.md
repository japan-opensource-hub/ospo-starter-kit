# Finding Open Source Software

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

When implementing new features, asking "Can existing open source software solve this problem?" represents standard practice in modern software engineering.
However, adopting unsuitable software risks introducing post-integration licensing violations or security vulnerabilities, derailing project timelines.

With millions of GitHub repositories available, multiple options exist for almost any engineering requirement.
Rather than relying blindly on star counts or superficial popularity, teams must evaluate license compatibility, security health, community vitality, and long-term project viability holistically.

This practical guide outlines structured discovery methodologies for identifying and selecting suitable open source software.

## Step 1: Search the Approved Internal OSS Inventory

Begin open source discovery by searching the internal approved inventory.
Listed components have passed technical screening and security evaluations, accelerating integration approval. Note that because licensing conditions depend on deployment models (internal tool, distributed product, SaaS delivery), verify that your proposed usage aligns with previous approval scopes.
Existing components often satisfy new feature requirements directly or through combination.

If exact matches are unavailable, search for components in similar domains.
Even partial overlaps provide starting points for discovering related libraries or suitable alternatives.

## Effective Discovery Techniques

### Multi-Faceted Information Gathering

Begin GitHub searches using targeted keywords (`language` + `capability`), exploring curated Awesome lists (e.g., `awesome-nodejs`) and GitHub Topics.
Cross-reference candidates against package registry download trends (npm, PyPI, Maven Central), Stack Overflow community recommendations, and technical engineering blogs.

Community discussions on Stack Overflow or Reddit reveal practical operational realities absent from official documentation.
Real-world troubleshooting experiences and performance benchmarks provide vital evaluation context.

## Critical Evaluation Criteria

### License Compatibility Verification

License verification represents a critical evaluation step.
Inspect `LICENSE` files and `README` documentation to confirm license types, evaluating compatibility against your deployment model (internal use, binary distribution, SaaS delivery).

Pay close attention to copyleft terms requiring source disclosure upon modification or distribution, network copyleft terms (AGPL), or enterprise commercial licensing thresholds.
Review criteria in [What Is a License?](../compliance/what-is-a-license.md) and [Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md), consulting the OSPO when terms are ambiguous.

### Project Activity and Sustainability

Healthy open source projects demonstrate regular commits, active discussion, and multi-developer contributions.
Projects with commits within the past six months and issue responses within days indicate active maintainer stewardship.

Projects backed by multiple organizations or neutral foundations offer higher long-term viability than projects dependent on single individuals or vendors.
Corporate sponsorship, clear governance models, and commercial support options indicate enterprise maturity.

### Security and Trustworthiness

Security screening evaluates maintainer responsiveness and disclosure transparency alongside historical bug records.
Screen candidate projects against CVE database records to evaluate patch velocity for reported vulnerabilities.

Mature projects implement automated testing, continuous integration, static code analysis, dependency scanning, and published vulnerability disclosure policies (`SECURITY.md`).
These practices signal production-grade engineering quality.

## Common Evaluation Pitfalls

Relying solely on popularity indicators represents a frequent mistake.
High repository star counts do not guarantee architectural fit, code quality, or maintainability.
Furthermore, latest releases are not automatically stable releases; evaluate Long-Term Support (LTS) releases for production workloads.

Overlooking transitive dependency trees represents another common oversight.
A top-level library may appear clean while pulling in deeply nested dependencies carrying copyleft licenses, security vulnerabilities, or abandoned code.
Evaluate entire dependency trees thoroughly.

Consider long-term operational impacts during selection—evaluating upgrade compatibility, deprecation risks, and migration costs.

## When to Consult the OSPO

Consult the OSPO prior to adoption in the following scenarios:
Uncertainty regarding commercial licensing requirements; security concerns (consult Security); or uncertainty regarding unlisted open source components.

Provide the following details to accelerate OSPO review:

- **Target Problem**: Specific technical capability required.
- **Deployment Model**: Internal tool / binary distribution / SaaS service.
- **Technical Integration**: Linking mechanism, dependency coupling.
- **Alternatives Evaluated**: Other libraries considered.

Selecting suitable open source software requires multi-dimensional evaluation across technical fit, licensing, security, and sustainability.
Following this guide minimizes risk while maximizing open source value.

Consult the OSPO with questions. Refer to "[What Is an OSPO?](../about/ospo.md)" for staff contacts.

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

- [ ] Documented location, format, and governance for the Approved Internal Inventory.
- [ ] Stated clear approval workflows and delegation policies.
- [ ] Created mapping tables linking security criteria to internal standards.
- [ ] Incorporated internal case studies detailing past selection mistakes.
- [ ] Published standard SLA turnaround times for OSPO reviews.
- [ ] Compiled curated discovery indexes for key internal languages and frameworks.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Maintaining Approved Catalogs

Define approval governance clearly—encouraging autonomous team evaluation while reserving consultations for complex copyleft licenses.
Keep catalogs updated through regular reviews and explicitly note that catalogs serve as reference guides rather than exclusive lists.

■ Documenting Internal Lessons Learned

Incorporate internal case studies detailing past component selection errors (e.g., refactoring due to unaddressed copyleft terms) to build practical engineering awareness.

■ Consultation SLAs

Establish target turnaround SLAs for OSPO inquiries, keeping decision-making authority centered on engineering leads while providing expert OSPO guidance.

########################################################################################
########################################################################################
-->

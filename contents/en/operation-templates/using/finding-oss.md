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

## Step 1: Search the Internal OSS Inventory

Begin open source discovery by searching the internal OSS inventory.
Listed components have already passed technical screening and security evaluations, accelerating adoption. Note that because licensing conditions depend on deployment models (internal tool, distributed product, SaaS delivery), verify that your proposed usage aligns with previous approval scopes.
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

Pay close attention to terms requiring source code provision upon modification or redistribution, terms triggered by delivery over a network, and terms requiring a commercial license beyond a certain usage scale or purpose.
These are not the only cases: obligations vary widely depending on how you use the software, so always check the specific conditions of each license.
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
High repository star counts do not guarantee architectural fit, and the software may be too complex to maintain for your purposes.
Furthermore, the latest release is not necessarily the stable release, so choose versions carefully.

Overlooking dependencies represents another common oversight.
Even when the chosen software itself is sound, the libraries it depends on may carry license issues, vulnerabilities, or the risk of abandoned maintenance.
Failing to evaluate the dependency tree as a whole can lead to serious problems later.

Consider long-term operational impacts during selection—evaluating upgrade compatibility, deprecation risks, and migration costs.

## When to Consult the OSPO

Consult the responsible staff or the OSPO prior to adoption in the following scenarios:
when it is unclear whether a commercial license is required; when there are security concerns (consult Security); or when you are unsure about software that is not on the Internal OSS Inventory.

Providing the following details helps the OSPO review proceed smoothly:

- **Purpose of Use**: What you want to solve. Please be as specific as possible, since the points to check vary with the purpose.
- **How It Will Be Used**: Internal use only / distribution / SaaS delivery, etc.
- **Technical Details**: Coupling method, dependencies, etc.
- **Alternatives Considered**: If any, as applicable.

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

- [ ] Documented location, format, and governance for the Internal OSS Inventory.
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

■ Building the Internal OSS Inventory

The internal OSS inventory is the cornerstone of this guide. Put the following elements in place:
 * Decide whether to create an approval process or leave selection to individual discretion (many companies make autonomous developer judgment the default and recommend consultation only for licenses with extensive verification requirements).
 * State the location and format of the inventory (internal wiki, portal, management system, etc.).
 * Establish a periodic review process so the inventory does not go stale.

If the inventory is thin at first, a realistic approach is to start from a survey of current usage and build it up in stages.
State explicitly that the inventory is reference information, so it does not create the misconception that "OSS not on the list cannot be used."

■ Turning Common Mistakes into Internal Case Studies

Grounding this section in actual internal cases makes it far more persuasive:
 * Share internal failure cases (e.g., "Team A chose X, then had to switch to Y later because of a license issue").
 * Make evaluation criteria concrete (e.g., weighting last-updated date and issue response speed).
 * Clarify internal criteria for when to adopt OSS at all (for projects with a small amount of code, OSS is not always the right choice).

■ Establishing the Consultation Process

The OSPO's role is to provide support and guidance that optimizes the company's use of OSS.
Set up the process so that support work does not become excessive:
 * Set a standard lead time from consultation to response.
 * Establish an expedited process for urgent cases.
 * Standardize how decisions are documented and shared internally.
 * Turn frequently asked topics into FAQs and build a knowledge base.
 * Make communication more efficient by turning it into a defined process.

It is important to communicate clearly that final responsibility for technology selection rests with the development team.

########################################################################################
########################################################################################
-->

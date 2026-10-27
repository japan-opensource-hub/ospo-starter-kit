# Types of Licenses

<!--
########################################################################################
For OSPO Staff: How to Use This Template

1. Add marks or notes to licenses frequently used in your company.
2. Verify completeness using the customization checklist.
3. Refer to the customization guide at the end to expand content based on your company's context.

This page provides an inventory of licenses and official text links.
Specific interpretations and condition evaluations should be determined in consultation with Legal.
########################################################################################
-->

This document is a reference guide classifying open source software licenses into five categories based on compliance obligation tiers.
Higher category numbers indicate increased obligations during distribution or service delivery:
1. **Category 1 (Attribution & License Text Inclusion)**
2. **Category 2 (Inclusion of Designated Information)**
3. **Category 3 (Source Code Disclosure for OSS Component)**
4. **Category 4 (Source Code Disclosure for Linked/Combined Software)**
5. **Category 5 (Source Code Disclosure for Network Service Users)**

Each category provides summaries, details for key licenses, and links to official license texts.

## License Category Mapping Table

Maps representative licenses to categories. Category 1 (Attribution) applies universally to all OSS licenses; higher numbers denote cumulative obligations.

| License | Category 1 | Category 2 | Category 3 | Category 4 | Category 5 |
|---|:---:|:---:|:---:|:---:|:---:|
| MIT License | ● | | | | |
| BSD 2-Clause License | ● | | | | |
| BSD 3-Clause License | ● | | | | |
| ISC License | ● | | | | |
| Apache License 2.0 | ● | ● | | | |
| GNU Lesser General Public License v2.1 | ● | | ● | | |
| GNU Lesser General Public License v3.0 | ● | | ● | | |
| Mozilla Public License 2.0 | ● | | ● | | |
| GNU General Public License v2.0 | ● | | ● | ● | |
| GNU General Public License v3.0 | ● | | ● | ● | |
| GNU Affero General Public License v3.0 | ● | | ● | ● | ● |
| Open Software License 3.0 | ● | | ● | ● | ● |

## Category 1. Retain Copyright Notices and License Text Upon Distribution

The most permissive category. Imposes minimal obligations on usage, modification, and redistribution—primarily retaining copyright notices and license text. Allows redistributing modified works under proprietary licenses, making it widely adopted in enterprise software.

**Key Characteristics:**

- Unrestricted use and embedding in commercial products
- No source code disclosure obligations for modified works
- Simple compliance requirements and low operational overhead
- High compatibility with other licenses
- Widespread enterprise adoption

### Representative Licenses

| License Name | SPDX Identifier | Official Text |
|---|---|---|
| MIT License | MIT | [opensource.org/licenses/MIT](https://opensource.org/licenses/MIT) |
| BSD 2-Clause License | BSD-2-Clause | [opensource.org/licenses/BSD-2-Clause](https://opensource.org/licenses/BSD-2-Clause) |
| BSD 3-Clause License | BSD-3-Clause | [opensource.org/licenses/BSD-3-Clause](https://opensource.org/licenses/BSD-3-Clause) |
| ISC License | ISC | [opensource.org/licenses/ISC](https://opensource.org/licenses/ISC) |

## Category 2. Include Designated Information (NOTICE Files, Acknowledgments) Upon Distribution

Requires retaining copyright notices and license texts, plus including designated supplementary notices (such as NOTICE files or acknowledgments) in distributions. Notably, Apache License 2.0 requires propagating NOTICE file contents, explicitly granting patent licenses and requiring notices of modifications.

**Key Characteristics:**

- Requires conveying additional designated information alongside copyright/license texts
- Mandates propagating NOTICE file contents
- Often includes explicit patent grants
- No source code disclosure obligations for modified works

### Representative Licenses

| License Name | SPDX Identifier | Official Text |
|---|---|---|
| Apache License 2.0 | Apache-2.0 | [apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0) |

## Category 3. Disclose Source Code for the OSS Component Upon Distribution

Primarily applies to software libraries. Requires disclosing source code for the OSS component itself upon distribution, but does not mandate disclosing source code for proprietary application code linking to the library. Modifies Category 4 copyleft obligations to allow proprietary software linking.

**Key Characteristics:**

- Source disclosure applies strictly to the OSS component itself (not linking application code)
- File-level or library-level copyleft scope

### Representative Licenses

| License Name | SPDX Identifier | Official Text |
|---|---|---|
| GNU Lesser General Public License v2.1 | LGPL-2.1-only | [gnu.org/licenses/old-licenses/lgpl-2.1.html](https://www.gnu.org/licenses/old-licenses/lgpl-2.1.html) |
| GNU Lesser General Public License v3.0 | LGPL-3.0-only | [gnu.org/licenses/lgpl-3.0.html](https://www.gnu.org/licenses/lgpl-3.0.html) |
| Mozilla Public License 2.0 | MPL-2.0 | [mozilla.org/MPL/2.0/](https://www.mozilla.org/en-US/MPL/2.0/) |

## Category 4. Disclose Source Code for Software Linked/Combined with the OSS Upon Distribution

Requires disclosing source code for both the OSS component and any software combined or linked with it upon distribution. Mandates that all derivative and combined works be licensed under identical or compatible license terms. This strong copyleft reciprocity dictates that embedding, linking, or deriving from covered OSS triggers copyleft terms across the combined work.

**Key Characteristics:**

- Broad copyleft scope covering combined works
- Mandates licensing derivative works under identical license terms
- Requires providing corresponding source code upon distribution
- Broadly enforces software openness

### Representative Licenses

| License Name | SPDX Identifier | Official Text |
|---|---|---|
| GNU General Public License v2.0 | GPL-2.0-only | [gnu.org/licenses/old-licenses/gpl-2.0.html](https://www.gnu.org/licenses/old-licenses/gpl-2.0-standalone.html) |
| GNU General Public License v3.0 | GPL-3.0-only | [gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0-standalone.html) |

## Category 5. Disclose Source Code to Users Accessing Services Over a Network

Extends Category 4 obligations to software delivered as network services. Even without physical distribution, making software accessible over a network as a service triggers source code disclosure obligations. Demands careful evaluation when operating cloud or SaaS offerings.

**Key Characteristics:**

- Obligations triggered by both distribution and network interaction
- Mandates offering source code to network service users
- Addresses modern cloud and SaaS deployment models
- Applies compliance terms without physical binary distribution

### Representative Licenses

| License Name | SPDX Identifier | Official Text |
|---|---|---|
| GNU Affero General Public License v3.0 | AGPL-3.0-only | [gnu.org/licenses/agpl-3.0.html](https://www.gnu.org/licenses/agpl-3.0.en.html) |
| Open Software License 3.0 | OSL-3.0 | [opensource.org/license/osl-3-0](https://opensource.org/license/osl-3-0) |

## Key Takeaways

Understanding these license categories underpins both consuming and contributing to open source:

1. **Category 1 (Attribution)** offers maximum flexibility, ideal for libraries seeking universal adoption.
2. **Category 2 (Designated Information)** requires conveying NOTICE files, without source disclosure obligations.
3. **Category 3 (OSS Source Disclosure)** balances library openness with commercial usability.
4. **Category 4 (Combined Work Source Disclosure)** enforces strong copyleft openness, requiring detailed compliance reviews.
5. **Category 5 (Network Service Source Disclosure)** extends copyleft obligations to modern cloud/SaaS deployments.

Each category satisfies distinct community governance goals.

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

- [ ] Added notes or callouts to licenses frequently used internally.
- [ ] Annotated restricted or prohibited licenses based on company policy.
- [ ] Highlighted categories particularly relevant to company business models (e.g., Category 5 for SaaS).

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Customizing for Your Organization

Document internal track records and considerations for frequently used licenses in supplementary guides.
Formulate license interpretations based on Legal advice.
Highlight categories requiring heightened vigilance based on deployment models (SaaS vs. distribution).

■ Expanding the Inventory

Add non-OSD-compliant licenses (BSL, Elastic License, etc.) encountered in your ecosystem under a clear "Non-OSI Approved" label.

########################################################################################
########################################################################################
-->

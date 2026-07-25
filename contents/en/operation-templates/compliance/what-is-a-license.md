# What Is a License?

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

When hearing "open source software" (OSS), people often assume it can be used without restrictions. In reality, all OSS components carry licenses, and usage must strictly comply with their terms. This represents a critical aspect requiring careful management in enterprise environments.

This guide explains foundational open source licensing concepts, classifications, risk factors, and practical compliance workflows to empower actionable decision-making on engineering teams.

## Why Licensing Matters

"Open source" and "public domain" are fundamentally distinct. Public domain software lacks copyright or has had copyright explicitly waived, making licensing concepts inapplicable.
Conversely, open source software remains copyrighted by its authors, who grant specific freedoms (use, copy, modify, distribute) conditioned upon license terms.
Licenses enable developers to specify "how my code may be used" and consumers to understand "what activities are permitted," fostering safe software exchange.

Ignoring this legal framework converts compliance risk into tangible enterprise costs: copyright infringement litigation, distribution injunctions, forced source code disclosure, back-license fees, and brand damage.
In enterprise environments, defining the boundaries of "distribution"—such as SaaS delivery, product embedding, and internal sharing across subsidiaries or partners—represents a key practical requirement.
Misunderstandings lead to pre-shipment architectural rewrites and delayed product launches.

## The Role of Open Source Licenses

An open source license is a legal document specifying terms under which software creators grant usage rights to third parties.
Under copyright law, original software receives copyright protection automatically upon creation.
Licenses grant permission to exercise specific exclusive rights under defined conditions.

Licenses balance permitted grants against mandatory obligations.
Permitted grants include usage, copying, distribution, modification, and commercial exploitation. Mandatory obligations include retaining copyright notices, accompanying license texts, documenting modifications, and disclosing source code. Diverse combinations of these terms produce numerous open source licenses balancing distinct rights and responsibilities.

The Open Source Initiative (OSI) is the international body certifying open source licenses. OSI-approved licenses guarantee adherence to all 10 criteria of the Open Source Definition (OSD)—including source code access, free redistribution, derivative works permission, non-discrimination against persons/groups or fields of endeavor, and technology neutrality. Many widely used licenses exist outside OSI approval; when adopting software, evaluate both OSI approval status and specific license conditions.

## Understanding and Achieving Compliance

The first step in license compliance is explicitly defining your project's technical deployment model:
Will software run strictly internally, undergo modification, link with other software, be distributed to customers in binary forms, or be offered as a cloud service over network APIs?
Ambiguity on deployment models yields opposite legal conclusions for the identical license.

In enterprise contexts, "distribution" boundaries are frequently nuanced.
Deploying software to separate legal entities—such as subsidiaries, international branches, or partner organizations—may legally constitute external distribution despite appearing to be internal usage.
While traditional SaaS delivery does not constitute distribution under most licenses, network-copyleft licenses like AGPL trigger compliance obligations upon network interaction.
For example, bundling open source JavaScript libraries into web application frontends constitutes static file redistribution, triggering requirements to retain copyright notices, accompany full license texts, and include NOTICE files where applicable.

In practice, locate official license texts prior to integration (`LICENSE`, `COPYING`, repository root, file headers, `NOTICE`). Evaluate permitted rights and obligations against your specific deployment model.
Analyze long license texts by identifying key functional clauses: Rights Grant, Conditions/Obligations, Limitations/Restrictions, Disclaimers/Warranties, Patent Grants, and Trademark Rules.
For example, when redistributing code under Apache-2.0, ensure operational pipelines propagate existing NOTICE file contents.

License compliance is a continuous lifecycle process rather than a one-time gateway check. It requires pre-adoption screening, automated CI/CD dependency detection, release artifact audits, and continuous tracking for upstream license changes (e.g., BSD to GPL transitions).
Automating detection via Software Composition Analysis (SCA), SBOM generation, dependency lockfiles, and signature verification enables engineering teams to focus manual reviews on architectural boundary assessments and complex policy exceptions.

### Primary License Categories

Open source licenses are categorized into five obligation tiers:

| Obligation Tier | Summary | Representative License Examples |
|---|---|---|
| **Category 1: Attribution & License Text Inclusion** | Retaining copyright notices and accompanying license texts represents the primary obligation. | MIT, BSD |
| **Category 2: Inclusion of Designated Information** | Include NOTICE files, acknowledgments, and modification notices in distributions. | Apache-2.0 |
| **Category 3: Source Code Disclosure for OSS Component** | Requires disclosing source code for the OSS component itself (proprietary application code remains private). | LGPL, MPL |
| **Category 4: Source Code Disclosure for Combined Software** | Requires disclosing source code for software combined or linked with the copyleft OSS component. | GPL |
| **Category 5: Source Code Disclosure for Network Service Users** | Triggers source code disclosure obligations upon delivering software as a network service (SaaS). | AGPL |

**Note 1**: Category 4 requires source code disclosure only for parts reached by copyleft reciprocity.
**Note 2**: Under Category 3 LGPL, proprietary application code does not require source disclosure, but developers must provide object code or build mechanisms enabling users to relink modified library binaries.

Category 4 copyleft licenses (GPL) mandate disclosing source code for derivative and combined works, covering static linking and same-process dynamic linking.
Category 5 licenses (AGPL) extend copyleft obligations to SaaS delivery, requiring heightened vigilance from cloud service providers.
Category 1 and 2 permissive licenses impose low compliance overhead and minimal review friction.

When projects combine components under multiple licenses, verify license compatibility to ensure terms do not conflict.

For detailed summaries, see **[Types of Licenses](../compliance/license-types.md)**; for high-impact copyleft licenses, see **[Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md)**.
Aligning architectural assumptions (static vs. dynamic linking, plugin boundaries, SaaS vs. binary distribution) during early design prevents costly rework.

### Locating and Reading License Terms

When evaluating software, locate official license texts in repository roots (`LICENSE`, `COPYING`), file headers, and `NOTICE` files.
When creating release artifacts, **always retain original copyright notices and license texts**, and **propagate NOTICE file contents** under Apache-2.0.

Read structured license documents by jumping directly to relevant sections: Grants, Conditions, Restrictions, Disclaimers, Warranties, Patents, and Trademarks. Focus on sections impacting your specific deployment model, relying on original legal text over unofficial translations.

### Common Misconceptions

Common enterprise misconceptions include: "Internal tools are exempt from compliance," "SaaS delivery never triggers GPL obligations," "Hosted on GitHub means freely usable," and "Distributing binary builds avoids license obligations."

In reality, sharing software with separate legal entities (subsidiaries or contractors) constitutes distribution under most licenses. Under AGPL, delivering SaaS services triggers source code disclosure obligations equivalent to physical distribution. Public code on GitHub remains bound by its license terms. Furthermore, distributing binary builds still requires accompanying copyright notices and full license texts.

Addressing these factors during early architectural design represents the most cost-effective compliance approach.

### Dual-Licensing and Commercial Options

Certain open source projects offer commercial licenses alongside open source terms (dual-licensing) or enforce commercial licenses above specific usage thresholds.
For details, see **[OSS with Commercial License Options](../compliance/oss-with-commercial-license-options.md)**.

### Continuous License Governance

License governance requires continuous oversight across software lifecycles.
As dependency trees update, new capabilities merge, and deployment models evolve, compliance baselines shift.
Conduct periodic audits to verify continuous alignment with licensing requirements.

Large projects incorporating hundreds of dependencies require automated SCA tooling and standardized governance processes rather than manual tracking.

## Consult the OSPO When Uncertain

Open source licenses sustain the long-term health of the open source ecosystem.
Proper understanding and adherence enable organizations to leverage open source with confidence.
Contact the OSPO when encountering licensing ambiguities. Refer to "[What Is an OSPO?](../about/ospo.md)" for staff contact information.

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

- [ ] Integrated internal IP review contacts and precedent review processes into body text.
- [ ] Compiled past license inquiries and incident reports into the FAQ.
- [ ] Documented corporate positions on license interpretations alongside concrete examples.
- [ ] Identified high-priority licenses for detailed internal guidance.
- [ ] Specified Software Composition Analysis (SCA) tooling used for license management.
- [ ] Defined compliance workflows and cross-departmental responsibilities.
- [ ] Documented audit cadences and escalation pathways.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Content Strategy

Focus body text on core principles and migrate edge cases to the FAQ to keep documentation scannable and practical.
Frame compliance as an enabler for confident open source adoption rather than a restrictive barrier.

■ Integration with Internal Workflows

Integrate existing Legal and IP consultation channels into compliance workflows.

■ Documenting Corporate Stances

Publish clear corporate positions on ambiguous licensing terms alongside concrete examples to guide developer decision-making.

■ Defining Tooling and Audits

Specify official SCA tools, audit cadences, and escalation protocols to build an operational compliance framework.

########################################################################################
########################################################################################
-->

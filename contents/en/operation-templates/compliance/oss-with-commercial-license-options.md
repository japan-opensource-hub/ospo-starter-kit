# OSS with Commercial License Options

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

Open source software (OSS) by definition permits commercial use.
However, specific open source licenses establish conditions on redistribution or modification, and vendors may offer commercial licenses for usage scenarios that do not comply with those open source conditions.

## Why Commercial Licenses Are Offered

Offering commercial licenses represents a strategic choice by creators and companies to build sustainable business models.
By releasing core functionality as open source while charging licensing fees for enterprise features, support, or proprietary commercial rights, vendors fund ongoing development and maintenance.

Using dual-licensed software without adhering to open source license conditions results in non-compliant usage, exposing organizations to legal liabilities, unexpected injunctions, and back-license claims.
Preventing these risks requires thorough pre-use verification and structured license management.

## Scenarios Requiring Commercial Licensing

This section outlines primary scenarios where commercial licensing becomes necessary:

- **Dual-Licensing Models**

  Certain open source software employs dual-licensing models—offering the identical codebase under both an open source license (GPL, AGPL, etc.) and a commercial license.

  Selecting the open source option requires strict compliance with its terms (such as source disclosure obligations).
  If business requirements prevent meeting these open source conditions, purchasing a commercial license becomes mandatory.

- **Non-OSS Licensing Terms Triggered by Usage Scale or Operational Metrics**

  Some source-available software includes conditions tied to organizational revenue, user counts, or usage scale.
  For example, vendors may require separate commercial contracts for companies exceeding revenue thresholds or organizational scale limits.
  These licenses do not meet the Open Source Definition (OSD); however, because their source code is publicly accessible, they are easily mistaken for OSS, necessitating careful review of licensing terms prior to adoption.

- **Commercial Support and Enterprise Add-On Features**

  Some OSS vendors provide core functionality under open source licenses while selling add-on services or enterprise capabilities separately.
  Enterprise security features, management consoles, and formal SLAs are typically delivered under commercial contracts.
  When enterprise operational requirements demand these capabilities, organizations purchase commercial agreements alongside open source usage.

## Covered Software [TO BE EDITED]

## OSS Requiring Heightened Vigilance [TO BE EDITED]

### Evaluation Guidelines

Verify the following points when evaluating new OSS:

1. **Review Licensing Terms**: Confirm whether dual-licensing or non-OSS commercial terms apply.
2. **Evaluate Deployment Models**: Categorize intended use (embedded binary distribution, SaaS delivery, internal tooling).
3. **Check Organizational Scale Criteria**: Verify whether revenue or employee thresholds trigger non-OSS commercial licensing.
4. **Assess Feature Requirements**: Determine whether open source features satisfy project requirements or if enterprise commercial add-ons are necessary.

## Consult the OSPO When Uncertain

When licensing terms are ambiguous, consult the OSPO.
Refer to "[What Is an OSPO?](../about/ospo.md)" for contact details.
Proper license management ensures seamless, efficient open source adoption.

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

- [ ] Listed representative commercial licenses already purchased internally.
- [ ] Listed prohibited source-available or dual-licensed software.
- [ ] Documented licenses requiring special review procedures.
- [ ] Created dedicated usage guides for frequently used dual-licensed software.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Listing Covered Software ("Covered Software" Section)

Provide representative examples of commercially licensed software already procured internally to guide developers.

■ Identifying High-Risk Software ("OSS Requiring Heightened Vigilance" Section)

Clearly document software requiring heightened vigilance:
 * Detail open source licenses requiring special review.
 * List software banned from internal use if commercial licenses are not procured.
 * Remind employees that publicly downloadable software may still carry restricted commercial terms.
 * Provide dedicated guides for heavily used, complex dual-licensed software.

########################################################################################
########################################################################################
-->

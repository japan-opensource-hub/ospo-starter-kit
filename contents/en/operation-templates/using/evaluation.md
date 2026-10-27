# Evaluating Open Source Software

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

Selecting open source software is a critical technical decision with long-term architectural impacts.
Superficial feature comparisons often obscure hidden risks that surface later as security vulnerabilities, license non-compliance, or abandoned maintainer support.

This guide outlines practical evaluation methodologies for software engineers, organizing reviews into distinct phases to ensure thoroughness without creating unnecessary friction.
For high-level discovery guidelines, refer to **[Finding Open Source Software](../using/finding-oss.md)**.

## Phased Evaluation Workflow

Execute candidate evaluations across three sequential phases, establishing clear criteria at each stage to determine whether to proceed.
Because expecting perfect software that satisfies every requirement is unrealistic, set practical, realistic pass criteria at each stage.

### Phase 1: Initial Screening

Filter candidates rapidly to eliminate clearly unsuitable options early.
The same applies to commercial software, but for open source, account for the fact that licenses differ substantially from commercial licenses and that projects are often run by communities.
Screen candidates against these baseline checks:

**License Verification**
Inspect `LICENSE` files and `README` documentation to confirm license types and verify compatibility with your deployment model (internal tool, binary distribution, SaaS service).
For licenses with source disclosure obligations (GPL, AGPL) or software that may require a commercial license, consult the OSPO during initial screening, as verification requirements vary by usage model.

**Activity Baseline**
Verify whether repositories have commits, issue activity, or merged pull requests within the past six months.
Avoid unmaintained projects to minimize security and sustainability risks.

**Core Functional Match**
Review `README` documentation to verify that candidate libraries satisfy baseline technical requirements. Detailed testing is unnecessary at this stage.

### Phase 2: Technical Evaluation

Conduct deep technical evaluation on candidates passing initial screening, following methodologies similar to commercial software reviews.

**Hands-On Verification**
Deploy candidate libraries in sandbox environments to test installation effort, configuration complexity, functional behavior, and documentation accuracy.
Libraries that appear clean in theory often reveal integration friction during hands-on testing.

**Performance and Stability**
Measure response latency, memory footprint, and CPU utilization under expected operational workloads. Verify error handling and stability under stress conditions.

**Architectural Compatibility**
Verify integration compatibility with existing systems, APIs, authentication protocols, and build pipelines.

**Dependency Tree Analysis**
Inspect transitive dependency trees to evaluate security posture, maintainability, and licensing across nested libraries.
Risky dependencies compromise top-level candidates.

### Phase 3: Security and Risk Assessment

Assess candidates across security posture and project governance.

**Vulnerability History**
Search CVE databases for historical vulnerability records, evaluating maintainer patch velocity and disclosure transparency. Response speed matters more than historical vulnerability counts.

**Security Practices**
Assess maintainer security practices—such as published security policies (`SECURITY.md`), automated testing, static analysis, and dependency scanning pipelines.

**Project Sustainability**
Evaluate developer diversity, corporate sponsorship, and foundation backing. Projects dependent on single individuals or single vendors carry higher abandonment risks.

**Community Vitality**
Inspect GitHub Insights and contributor trends. Active, welcoming communities indicate long-term viability.

## Key Evaluation Factors

### License Compliance and Architectural Scope

License evaluation must analyze technical integration mechanisms alongside license categories.
For copyleft licenses (GPL, AGPL), evaluate copyleft scope boundaries against architectural coupling—static linking, dynamic linking, IPC, or network APIs.
For details, see **[Licenses with Source Code Disclosure Obligations](../compliance/source-disclosure-licenses.md)**.

Carefully evaluate legal risks when combining libraries carrying conflicting license terms.

### Documentation and Support Ecosystem

**Documentation Quality**
Assess API references, setup guides, and code samples. Quality documentation significantly reduces integration and onboarding costs.

**Community Support**
Review responsiveness on GitHub Issues and discussion forums. Active community support accelerates troubleshooting.

**Commercial Support**
For mission-critical production workloads, verify whether commercial SLAs, enterprise add-ons, or professional support contracts are available.

## Evaluation Pitfalls to Avoid

1. **Over-Relying on Popularity Metrics**

    Repository stars and download counts provide useful indicators but do not guarantee security, code quality, or architectural fit.
    It also helps to understand why a project attracts attention. The fact that many people use it is reassuring, and many issues (including bugs) may already have been discovered.
    Still, treat popularity metrics as one reference point among many, and give more weight to technical fit and risk evaluation.

2. **Blindly Adopting "Latest" Releases**

    Latest releases may introduce unvetted bugs or breaking API changes. Prefer Long-Term Support (LTS) or stable releases for production environments.

3. **Feature Bloat**

    Feature-rich software looks attractive, but excessive unneeded capabilities increase learning and operational overhead. Prefer simple, understandable software with a scope appropriate to your requirements.

4. **Neglecting Continuous Re-Evaluation**

    Software evaluation is an ongoing process rather than a one-time gateway. Establish continuous dependency monitoring to re-assess security health and maintainer status over time.

## Documenting and Sharing Evaluations

Insights gained through evaluation should serve not only individual learning but the whole team and organization.
Document evaluation results properly, share them with colleagues, reuse them in similar future projects, and use them to raise the organization's overall evaluation capability.

Recording specific problems and strengths discovered during evaluation provides valuable reference for later decisions.
Also record improvement points for the evaluation process itself to help the organization evaluate better over time.

When evaluating multiple candidates, create comparison tables or evaluation matrices to make decision rationales explicit.
This supports accountability for selection decisions and serves as reference material for future reviews.

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

- [ ] Tailored license review criteria to align with corporate risk policies.
- [ ] Defined activity thresholds (e.g., "commits within past 6 months").
- [ ] Created tech-stack-specific evaluation guidelines.
- [ ] Standardized dependency analysis tools and scanning workflows.
- [ ] Clarified criteria for whether commercial support is required, by business criticality.
- [ ] Established periodic re-evaluation schedules for core dependencies.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Customizing Screening Criteria

Adjust initial screening criteria to match your company's risk tolerance:
 * Make license compatibility criteria concrete in line with internal policy.
 * Define minimum activity thresholds (e.g., "commits within the past 6 months required").

In early stages, prioritize practical criteria that exclude clearly problematic software over perfect criteria.

■ Addressing Common Pitfalls

Creating concrete guidelines based on actual internal experience is most effective:
 * Document lessons learned from past failures.
 * Clarify version-selection criteria by use case.
 * Establish periodic re-evaluation schedules and processes.

Also prepare preventive guidance for judgment errors common among new or less experienced developers.
Combine with "Finding Open Source Software" to provide realistic evaluation criteria.

■ Security Alignment

Customize security evaluation to align with internal security policies and development processes:
 * Create mapping tables to internal security standards.
 * Document how to use vulnerability monitoring tools.
 * Provide checklists for assessing project health.

Use this document as a baseline and make it concrete for your company's circumstances.

########################################################################################
########################################################################################
-->

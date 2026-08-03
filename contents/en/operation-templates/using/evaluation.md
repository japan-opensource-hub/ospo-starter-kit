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
Set realistic, practical pass criteria rather than seeking mythical "zero-risk" software.

### Phase 1: Initial Screening

Filter candidates rapidly to eliminate clearly unsuitable options early.
Unlike commercial software evaluation, open source screening accounts for copyleft licensing mechanics and community project governance.
Screen candidates against these baseline checks:

**License Verification**
Inspect `LICENSE` files and `README` documentation to confirm license types and verify compatibility with your deployment model (internal tool, binary distribution, SaaS service).
For licenses with source disclosure obligations (GPL, AGPL) or dual-licensing terms, consult the OSPO during initial screening.

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

    Repository stars and download counts provide useful indicators but do not guarantee security, code quality, or architectural fit. Treat popularity metrics as secondary data points behind technical evaluation.

2. **Blindly Adopting "Latest" Releases**

    Latest releases may introduce unvetted bugs or breaking API changes. Prefer Long-Term Support (LTS) or stable releases for production environments.

3. **Feature Bloat**

    Excessive unneeded capabilities increase attack surfaces and learning overhead. Prefer focused, modular libraries.

4. **Neglecting Continuous Re-Evaluation**

    Software evaluation is an ongoing process rather than a one-time gateway. Establish continuous dependency monitoring to re-assess security health and maintainer status over time.

## Documenting and Sharing Evaluations

Document evaluation findings in comparison matrices to capture decision rationales, build institutional knowledge, and streamline future architectural reviews.

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
- [ ] Defined criteria requiring commercial support SLAs based on service criticality.
- [ ] Established periodic re-evaluation schedules for core dependencies.

<!--
########################################################################################
Customization Guide

Guidance for expanding and refining content to match your company context following placeholder replacement.
########################################################################################

■ Customizing Screening Criteria

Set practical initial screening rules that filter out high-risk components without stifling development momentum.

■ Addressing Common Pitfalls

Incorporate internal case studies detailing past evaluation errors (such as adopting unstable releases) to build practical team awareness.

■ Security Alignment

Align evaluation guidelines with internal security baseline standards, detailing automated SCA tool usage and vulnerability triage protocols.

########################################################################################
########################################################################################
-->

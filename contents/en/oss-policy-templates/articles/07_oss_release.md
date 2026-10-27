# Article 7. Releasing Company Works as OSS

## Sample Article

[Article 7. Releasing Company Works as OSS

1. When an Employee intends to release software developed in connection with Company duties as new OSS, in addition to complying with Article 5, the Employee must complete application procedures specified separately in advance.
2. During the application process under the preceding paragraph, the project lead (or responsible Employee) shall comply with the preceding article and verify the following matters, with OSPO providing support as necessary:
  a. Presence of third-party works, and compatibility between third-party license terms and the proposed license terms for the new OSS
  b. Absence of confidential information, personal data, or other restricted data within the software to be released
  c. Intellectual property relationships regarding patents, trademarks, etc. (risk of third-party infringement, necessity of patent filings, potential restrictions on enforcing Company rights)
  d. Structuring license terms in light of the intended usage model of the OSS
  e. Support policy, development structure, and maintenance plan
3. As a rule, new OSS shall be published on official repositories managed by the Company (or designated by OSPO). Upon release, copyright notices and licensing terms (including usage conditions and disclaimers) must be properly embedded in the new OSS.
4. When changing licenses, modifying visibility, transferring repositories, or archiving/deprecating Company-released OSS, the project lead must obtain prior approval from the OSPO.
5. When incorporating third-party works or accepting source code, documentation, or other works from third parties into Company-released and maintained OSS, prescribed standards and procedures shall be followed, and the project lead (or responsible Employee) shall verify:
  a. Rights ownership and licensing terms of the contributed work
  b. Compatibility with the overall license of the OSS
  c. Security risks (malware, vulnerabilities), third-party rights infringement, and potential legal violations
6. When accepting contributions under the preceding paragraph, the OSPO may (in consultation with Legal) advise on the necessity of executing a CLA or other contracts with contributors and propose necessary actions to relevant departments.]

## Commentary

Once software is released as OSS, retracting information is virtually impossible; leaking proprietary code risks losing competitive edge. Public repositories have high visibility, making accidental inclusion of customer assets, third-party code, or patented technology a major legal liability with high remediation costs. Establishing pre-release reviews standardizes quality independent of individual expertise. Pre-defining emergency protocols (reporting/takedown) mitigates leak damage while empowering strategic releases (standardization, ecosystem building) without sacrificing momentum.

## Customization Perspectives and Operational Notes

Calibrate application friction based on the nature of the released OSS. Excessive friction stifles open source initiatives.

- Explicitly define release objectives (ecosystem growth, industry standards) and distinguish between releasable areas (utilities, frameworks) and non-releasable areas (core differentiators).
- Standardize verification items (license compatibility, secrets scanning, IP, export controls) into checklists. Combine with automated SCA tools to prevent human oversight.
- Select 1–2 default corporate open source licenses to accelerate evaluation.
- Align post-release maintenance responsibilities (vulnerability handling) with Article 11, and emergency takedowns (accidental leaks) with Article 10 incident protocols.

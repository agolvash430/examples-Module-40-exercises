# Lab 40 — Outline Security Assessment

## Step 1 — Sections

1. Scope
2. Tools
3. Findings Summary
4. Remediations Planned
5. Residual Risks
6. Evidence Index

### Scope

- Spring CRM application assessment.
- Review of API, dependency, and configuration risks.
- Review of Dependency-Check findings and triage process.
- Validation of documented security controls and evidence.
- Pre-lab planning only; no remediation or re-scan performed.

### Tools

- OWASP Dependency-Check
- Maven Wrapper (mvnw)
- JDK 21
- Findings Triage CSV
- Source Code Review (SAST activities)
- Regression Test Suite

### Findings Summary

- Total Findings: _____
- True Positives: _____
- False Positives: _____
- Accepted Risks: _____
- Fixed Findings: _____

### Remediations Planned

- Upgrade vulnerable dependencies identified as true positives.
- Review authorization controls on customer-facing API endpoints.
- Remove or rotate exposed secrets if discovered.
- Validate logging and monitoring coverage.
- Execute regression testing after approved fixes.

### Residual Risks

| Risk | Severity | Owner | Due Date | Mitigating Control |
| --- | --- | --- | --- | --- |
| _____ | _____ | _____ | _____ | _____ |
| _____ | _____ | _____ | _____ | _____ |
| _____ | _____ | _____ | _____ | _____ |

## Step 2 — Check the reference

Residual risk entries must contain:

- Risk
- Severity
- Owner
- Due Date
- Mitigating Control

No residual risk record should be considered complete if any of these fields are missing.

## Step 3 — Evidence index draft

| Claim | Artifact Path |
| --- | --- |
| Dependency scan completed | notes/lab-40/dependency-check-report.html |
| Dependency scan machine-readable evidence available | notes/lab-40/dependency-check-report.json |
| Findings triaged and classified | notes/lab-40/findings-triage.csv |
| Vulnerability review documented | notes/lab-40/security-assessment.md |
| Regression verification executed | _____RegressionTestName_____ |
| Authorized fix validation completed | _____ArtifactPath_____ |

## Step 4 — Scope honesty

Note: This is a pre-lab outline only; full remediation, validation, and re-scan activities occur during the Lab 40 timed/full path exercise.

## Scope

Pre-lab only — do not finish the full lab in this exercise.

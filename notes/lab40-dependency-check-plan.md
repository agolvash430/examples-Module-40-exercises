# Lab 40 — Plan Dependency-Check Gate

## Step 1 — Profile sketch

- Create a Maven profile named `security-scan`.
- Configure the OWASP Dependency-Check Maven plugin.
- Run the `dependency-check:check` goal during the security review process.
- Generate HTML reports for human review.
- Generate JSON reports for automation and evidence collection.
- Store reports in a dedicated output directory.
- Define a placeholder CVSS fail threshold (for example: `CVSS >= X.X`) to block builds when high-risk vulnerabilities are detected.
- Document the threshold so it can be adjusted by project policy later.

## Step 2 — Check the reference

JDK 21 and Maven Wrapper habits:

```bash
./mvnw -B -Psecurity-scan dependency-check:check

# Lab 40 — Sketch Findings Triage CSV

## Reference

| Classification | Meaning |
| --- | --- |
| true_positive | Confirm and fix or accept with owner |
| false_positive | Document CPE/path mismatch |
| accepted_risk | Time-bounded, owned |
| fixed | Re-scan evidence required |

## Step 1 — Columns

CSV Headers:

finding_id,cve,cvss,dependency,path,classification,owner,due_date,notes

## Step 2 — Check the reference

Classification Rules:

- true_positive = Finding confirmed and requires remediation or formal risk acceptance.
- false_positive = Finding determined to be incorrect due to dependency,

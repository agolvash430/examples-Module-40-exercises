# Lab 40 — Draft AppSec Go/No-Go Questions

## Step 1 — Questions

### 1. Are all High/Critical CVEs assigned an owner and documented remediation or risk disposition?

Go/No-Go:
- GO if every High/Critical finding has ownership and a documented action.
- NO-GO if any High/Critical finding is unowned or unexplained.

### 2. Has the repository been verified to contain no secrets, passwords, tokens, keys, or credentials?

Go/No-Go:
- GO if secret scanning and review show no exposed secrets.
- NO-GO if any secret exists in source control.


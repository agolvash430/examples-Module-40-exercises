# Lab 40 — Map CRM Attack Surfaces

## Reference

| Surface | OWASP theme | Example |
| --- | --- | --- |
| Customer GET/PUT API | Broken access control | Agent reads CUS-1001 |
| Search query params | Injection | Name/email filters |
| pom.xml deps | Vulnerable components | Transitive CVE |
| application.yml secrets | Security misconfiguration | DB password in Git |
| Actuator endpoints | Security misconfiguration | Unprotected /env |

## Step 1 — Inventory touchpoints

| Surface | Purpose | Data Type |
| --- | --- | --- |
| Customer HTTP APIs (GET /customers/{id}, PUT /customers/{id}) | Agents retrieve and update customer records for CUS-1001 (Amina Khan) and CUS-1002 (Ravi Singh) | PII + IDs |
| JWT Authentication & RBAC | Verifies agent identity and permissions before allowing access | IDs |
| SQL Database / JPA Repositories | Stores customer records and account data | PII + IDs |
| Application Logs / Audit Logs | Records customer lookups, updates, and security events | PII + IDs (if logged improperly) |
| Search Query Parameters | Allows filtering customers by name, email, or customer ID | PII + IDs |
| Configuration Files (application.yml) | Stores application settings, database connections, and secrets | IDs + Secrets |
| Kafka Event Topics (future integration) | Publishes customer update events across services | PII + IDs |

PII Examples: customer name, email, phone number, address.

ID Examples: customer ID (CUS-1001, CUS-1002), agent ID, JWT subject identifier.

## Step 2 — Check the reference

| Surface | OWASP Theme |
| --- | --- |
| Search query parameters | Injection |
| Customer APIs | Broken Access Control |
| JWT/RBAC authorization | Broken Access Control |
| application.yml secrets | Security Misconfiguration |
| Actuator endpoints | Security Misconfiguration |
| pom.xml dependencies | Vulnerable Components |
| Application logging | Logging and Monitoring Failures |
| Kafka events | Logging/Monitoring Failures and Misconfiguration (if not monitored or secured) |

## Step 3 — Rank top three

### 1. Customer HTTP APIs

Business Impact: Broken access controls could allow an agent or attacker to view or modify customer records such as CUS-1001 or CUS-1002, resulting in a privacy breach and loss of customer trust.

### 2. application.yml Secrets

Business Impact: Exposure of database credentials or API keys could provide attackers direct access to backend systems and sensitive customer data.

### 3. Search Query Parameters

Business Impact: Injection vulnerabilities could enable unauthorized database access, data disclosure, or manipulation of CRM records.

## Scope

Pre-lab only. This exercise inventories CRM attack surfaces, maps them to OWASP themes, and identifies the highest-risk areas that should be reviewed before release. It does not perform detailed threat modeling, testing, or remediation activities.

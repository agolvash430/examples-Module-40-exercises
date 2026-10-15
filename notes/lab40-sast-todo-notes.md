# Lab 40 — Fill SAST Path TODOs

## Step 1 — Copy template

Create: `sast-path-todo.md`

Template:

Endpoint: _____
Authz check: _____
Sink (SQL/file/log): _____
Customer fixture used: _____
Risk if missing check: _____

## Step 2 — Fill for customer read

Endpoint: GET /api/customers/{id}
Authz check: Verify authenticated user has required role (AGENT) and perform object-level access check TODO _____
Sink (SQL/file/log): SQL (customer lookup) and application log
Customer fixture used: CUS-1001
Risk if missing check: Unauthorized users may view customer records and sensitive CRM data for customers they should not access

## Step 3 — Second path

Endpoint: PUT /api/customers/{id}/status
Authz check: Verify authenticated user has required role (AGENT or SUPERVISOR) and perform object-level update authorization check TODO _____
Sink (SQL/file/log): SQL (status update) and application log
Customer fixture used: CUS-1002
Risk if missing check: Unauthorized users may modify customer status, leading to data integrity issues and incorrect business decisions

## Step 4 — Self-check

- No passwords included.
- No API tokens included.
- No database secrets included.
- No real customer PII included.
- Customer fixtures use IDs only (CUS-1001 and CUS-1002).
- Object-level authorization verification remains marked as `_____` and will be proven during Lab 40 code review.
- Specific authorization implementation remains marked as `_____` and will be validated against application code.
- Any repository, service, or controller enforcement details remain marked as `_____` pending code analysis.

## Scope

Pre-lab only — do not finish the full lab in this exercise.

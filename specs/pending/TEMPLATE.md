---
title:
description:
date: YYYY-MM-DD
---

## Context / Problem

<!-- To fill by the Product Manager -->

## Requirements

<!-- To fill by the Product Manager -->


## Acceptance criteria
- [ ] Criterion 1
- [ ] Criterion 2

## Out of Scope

<!-- N/A if not applicable -->

## Technical Specifications

### Section 1
- [ ] Task 1
- [ ] Task 2

### Section 2
- [ ] Task 1
- [ ] Task 2

## Security Review

<!-- To fill by the Security Architect -->

### Authentication & Authorisation
- [ ] Are all new endpoints/actions protected by appropriate auth checks?
- [ ] Are permissions and ownership properly defined and authorisation checks in place?
- [ ] Are there privilege escalation paths the spec doesn't address?

### Input & Data
- [ ] Is all user input validated and sanitized before use?
- [ ] Are there injection risks (SQL, command, template, path traversal)?
- [ ] Does the spec handle untrusted data flowing into sensitive sinks (eval, innerHTML, exec, file paths)?

### Secrets & Credentials
- [ ] Are any secrets, tokens, or credentials involved? Are they handled via env vars / secret stores — never hardcoded?
- [ ] Are API keys or tokens scoped to minimum required permissions?

### Data Exposure
- [ ] Does the spec avoid leaking sensitive data in logs, error messages, or API responses?
- [ ] Are there PII or sensitive fields that need masking or encryption?

### Dependencies & Supply Chain
- [ ] Does the spec introduce new third-party dependencies? If so, are they well-maintained and audited?

## Code Review

<!-- N/A if not applicable -->

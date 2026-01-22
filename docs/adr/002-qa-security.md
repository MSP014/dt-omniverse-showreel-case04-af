# ADR 002: QA & Security Guardrails

## Status

Accepted

## Context

"Case 04" involves Python logic automating complex logistics. Typos or untested code could break the showreel pipeline. We also need to prevent secret leakage (API Keys) and vulnerable dependencies.

## Decision

We enforce the **"Measure Twice, Cut Once"** philosophy through automated guardrails.

### 1. Pre-commit Hooks

Must run before every commit:

* **Formatting**: `black`, `isort` (Consistency)
* **Linting**: `flake8` (Syntax/Logic errors)
* **Security**: `bandit` (Static code analysis), `pip-audit` (Dependency vulnerabilities)
* **Hygiene**: `trailing-whitespace`, `check-yaml`

### 2. Security

* **Secrets**: strictly `.env`. Never commit secrets.
* **Network**: No external calls (curl/requests) without user permit.

## Consequences

* **Positive**: Code is always clean and formatted. Vulnerabilities are caught early.
* **Negative**: Committing takes longer (~10s). Requires rigorous discipline to fix errors instead of bypassing hooks.

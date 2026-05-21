# Case 04 Technical Debt

## Unresolved Technical Debts

_No open technical debts at the moment._

## Resolved Technical Debts

### [SECURITY] Pip Security Lock & Dependencies Conflict

- **Status:** Resolved (2026-05-21)
- **Severity:** High
- **Description:** Environment previously used `pip 25.3` due to historic compatibility issues between `pip 26.0+` and older `pip-tools`.
- **Resolution:** Upgraded tooling in `case04-env` and validated lock generation workflow.
  - `pip` -> `26.1.1`
  - `pip-tools` -> `7.5.3`
  - Lock refresh command: `conda run -n case04-env pip-compile --upgrade requirements.in`
  - Result: `requirements.txt` pins `pip-tools==7.5.3`.
- **Verification Date:** 2026-05-21

# ADR 001: Naming Conventions & Language Standards

## Status

Accepted

## Context

In a hybrid pipeline (Houdini/Omniverse/Python), conflicting naming standards (Houdini's `snake_case` vs USD's `CamelCase`) cause friction. We need a unified standard to ensure "Case 04" integration logic remains clean and predictable.

## Decision

### 1. Language

* **Documentation**: British English (en-GB). Use `s` (optimise), not `z`.
* **Commit Messages**: British English. Imperative mood ("Add", not "Added").
* **User Communication**: Russian (as per Persona).

### 2. Python

* **Files/Modules**: `snake_case.py`
* **Functions/Variables**: `snake_case`
* **Classes**: `PascalCase`
* **Constants**: `SCREAMING_SNAKE_CASE`

### 3. USD / Omniverse / Houdini

* **Asset Names**: `PascalCase` (e.g., `FuelTanker`, `GroundCrew`)
* **USD Stages**: `snake_case` (e.g., `main_stage.usd`)
* **Attributes**: `camelCase` (e.g., `fuelLevel`, `routeId`) to align with USD schema standards.

### 4. Git

* **Branches**: `feature/description-of-change`
* **Tags**: `vX.Y.Z`

## Consequences

* **Positive**: Predictable auto-complete in Python and USD. Clear distinction between Logic (Python) and Data/Scene (USD).
* **Negative**: Requires mental switching between `snake_case` (Python) and `camelCase` (USD attributes).

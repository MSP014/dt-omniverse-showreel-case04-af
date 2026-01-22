# ADR 003: Dependency Locking Strategy

## Status

Accepted

## Context

Python environments are prone to "drift" if dependencies are not strictly locked. Standard `requirements.txt` often misses transitive dependency versions, leading to "it works on my machine" issues.

## Decision

We adopt **explicit dependency compilation**.

### 1. Mechanism

* **Source**: `requirements.in` (Top-level direct dependencies).
* **Lockfile**: `requirements.txt` (Generated via `pip-compile`). Includes ALL dependencies with strict hashes.

### 2. Workflow

* Add package to `requirements.in`.
* Run `pip-compile requirements.in`.
* Commit both files.
* Install via `pip install -r requirements.txt`.

## Consequences

* **Positive**: 100% reproducible builds. Pip-audit can scan exact versions used.
* **Negative**: Extra step to update packages (cannot just `pip install X`).

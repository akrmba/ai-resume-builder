# Architecture Decision Records (ADRs)

This directory contains **Architecture Decision Records** (ADRs) that document significant architectural decisions for the AI Resume Builder project.

## What is an ADR?
An ADR is a short document that captures:
- **Decision**: What we decided.
- **Context**: Why we needed to make this decision.
- **Consequences**: What the decision means for the project (good and bad).
- **Status**: Proposed, accepted, superseded, or deprecated.

## Purpose
- Provide a historical record of why certain choices were made.
- Help new team members understand the architectural landscape.
- Reduce repeated debates by documenting the rationale.
- Ensure decisions align with the constitution and golden rules.

## Template
Each ADR should follow this template:

```
# [ADR‑###] Short descriptive title

## Status
[Proposed | Accepted | Superseded | Deprecated]

## Context
Describe the problem, constraints, and forces that led to this decision.

## Decision
State the decision clearly and concisely.

## Consequences
### Positive
- What benefits does this decision bring?

### Negative
- What trade‑offs or drawbacks does it introduce?

### Neutral
- What other impacts (maintenance, learning curve, etc.) should be noted?

## References
- Links to related documents, issues, or pull requests.
- Citation of constitution sections or golden rules that influenced the decision.
```

## Naming Convention
- `ADR‑001‑short‑title.md`
- Use sequential numbers (001, 002, …).
- Keep the filename descriptive but concise.

## Process
1. **Propose**: Create a new ADR file in this directory with status “Proposed”.
2. **Discuss**: Share with the team and gather feedback.
3. **Accept**: Update status to “Accepted” once consensus is reached.
4. **Implement**: Follow the decision in code and documentation.
5. **Supersede/Deprecate**: If a later decision changes or replaces an ADR, update its status accordingly.

---

**Version**: [ADRS_001] | **Last Reviewed**: [DATE]
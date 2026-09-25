# AI Resume Builder – Spec Kit + Golden Gates Repository

This repository follows the **Spec Kit workflow** and is governed by **golden gates** to ensure consistency, quality, and adherence to architectural principles.

## Quick Start

### 1. Run the Constitution
Before any feature work, execute the constitution once to establish the foundational rules:
```
/speckit.constitution
```

### 2. Feature Development Flow
For each new feature, follow this order:

1. **Specify** – `/speckit.specify`  
   Create a feature specification in `.specify/specs/`.

2. **Clarify** – `/speckit.clarify`  
   Refine requirements and resolve ambiguities.

3. **Plan** – `/speckit.plan`  
   Produce an implementation plan.

4. **Tasks** – `/speckit.tasks`  
   Break down the plan into actionable tasks.

5. **Analyze** – `/speckit.analyze`  
   Review risks, dependencies, and compliance.

6. **Implement** – `/speckit.implement`  
   Write code, adhering to the golden gates.

### 3. Golden Gates
- **Golden rules** are in `golden/RULES.md` – they are law.
- **Definition of Done** is in `golden/CHECKLIST.md` – all items must pass before merging.
- **Contracts** live in `golden/contracts/` – external shapes are defined here.
- **Operator tasks** are in `golden/OPERATOR_TASKS.md` – manual setup and deployment steps.

## Repository Structure

```
.specify/          # Spec Kit workflow artifacts
├── memory/constitution.md
└── specs/         # Feature specifications

golden/            # Golden gates
├── RULES.md
├── CHECKLIST.md
├── OPERATOR_TASKS.md
├── contracts/     # API/data contracts
├── examples/      # Example implementations
└── prompts/       # LLM prompt templates

docs/ADRs/         # Architecture Decision Records

tests/             # Test suites
├── unit/
└── integration/

src/               # Source code
```

## Development Commands

The `Makefile` provides placeholder targets for common tasks:

```bash
make check   # Run formatting, linting, and type checking (placeholder)
make fmt     # Format code (placeholder)
make test    # Run unit and integration tests (placeholder)
```

## Key Principles

- **No merge unless gates pass** – Every change must satisfy `golden/CHECKLIST.md`.
- **Contracts are law** – External integrations must conform to `golden/contracts/*`.
- **Adapter pattern** – No direct vendor SDKs in core logic.
- **Stop and ask** – When in doubt, escalate; do not guess.

## Contributing

1. Read the constitution (`.specify/memory/constitution.md`).
2. Follow the Spec Kit workflow for feature work.
3. Ensure your changes pass all golden gates before opening a pull request.
4. Document architectural decisions as ADRs in `docs/ADRs/`.

---

**Version**: [README_001] | **Last Updated**: [DATE]
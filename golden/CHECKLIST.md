# Definition of Done Checklist

This checklist defines the **gates** that must pass before any change can be considered “done” and ready for merge.

## Style Lock
- [ ] **Formatting**: Run `make fmt` (or equivalent) and verify no formatting changes are needed.
- [ ] **Linting**: Run `make lint` (or equivalent) and address all warnings/errors.
- [ ] **Type checking**: Run `make typecheck` (or equivalent) and ensure no type errors.
- [ ] **Pre‑commit**: Execute `pre‑commit run --all‑files` and ensure all hooks pass.

## Behavior Lock
- [ ] **Unit tests**: Run `make test` (or equivalent) and ensure all unit tests pass.
- [ ] **Integration tests**: Run `make integration‑test` (or equivalent) and ensure all integration tests pass.
- [ ] **Contract tests**: If the change touches a contract in `golden/contracts/*`, run any contract‑validation steps.
- [ ] **Regression tests**: Verify that existing functionality is not broken.

## Documentation & Artifacts
- [ ] **README updates**: Update any relevant README sections if the change affects usage.
- [ ] **Contract updates**: If the change modifies external interfaces, update `golden/contracts/*` accordingly.
- [ ] **ADR required?**: If the change is architectural, create/update an ADR in `docs/ADRs/`.

## Security & Privacy
- [ ] **No secrets**: Confirm no secrets are committed; environment variables are used instead.
- [ ] **Privacy review**: Ensure the change does not expand data retention or logging beyond what is necessary.
- [ ] **User‑control check**: Verify that any AI‑generated changes remain editable and reversible by the user.

## Merge Gates
- [ ] **All checks pass**: All items above are satisfied.
- [ ] **Constitution compliance**: The change does not violate any principle in `.specify/memory/constitution.md`.
- [ ] **Golden rules compliance**: The change adheres to `golden/RULES.md`.
- [ ] **Operator tasks updated**: If the change affects deployment or operations, update `golden/OPERATOR_TASKS.md`.

---

**Version**: [CHECKLIST_001] | **Last Reviewed**: [DATE]
<!-- Update this checklist when new gates are added via ADR. -->
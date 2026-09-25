# Golden Rules

These rules are **law** for this repository. They define architectural constraints and development principles that must be followed.

## 1. Adapter Pattern Rule
- **No direct vendor SDKs in core logic**: All third‑party integrations (APIs, databases, external services) must be wrapped behind adapters.
- Core domain logic must depend only on stable internal interfaces, not vendor‑specific types or error models.
- Swapping vendors must be feasible by changing adapter code only, not core logic.

## 2. Contracts Are Law
- External API shapes, data schemas, and integration contracts live in `golden/contracts/*`.
- Any change to an external contract must be reflected in the corresponding contract artifact and its tests.
- Contracts are the source of truth for integration behavior; implementations must conform.

## 3. Stop and Ask
- When ambiguity or conflict arises between rules, contracts, or the constitution, **stop and ask**.
- Do not guess; escalate to the team or refer to the source‑of‑truth order defined in the constitution.
- Document the resolution as an ADR if the ambiguity reveals a missing rule.

## 4. No Merge Unless Gates Pass
- No pull request may be merged unless all gates in `golden/CHECKLIST.md` pass.
- Gates include style lock (formatting, linting, type‑checking), behavior lock (tests), and any contract‑validation steps.

## 5. Privacy‑by‑Default
- Minimize logging and retention of user‑identifiable data.
- Secrets stay in environment variables; never commit them.
- See `golden/OPERATOR_TASKS.md` for environment‑variable guidance.

---

**Version**: [RULES_001] | **Last Reviewed**: [DATE]
<!-- Keep this document concise; add new rules only after team consensus and an ADR. -->
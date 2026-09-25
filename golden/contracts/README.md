# Contracts Directory

This directory holds **external contracts** that define integration boundaries.

## Purpose
Contracts are **law** for integrations. They specify:
- API shapes (OpenAPI/Swagger, GraphQL schemas)
- Data schemas (JSON Schema, Protobuf, Avro)
- Message formats (Kafka topics, event payloads)
- Service‑level agreements (SLAs, error handling)

## Files
- `openapi.yaml` – OpenAPI 3.0 specification for REST APIs.
- (Add other contract files as needed)

## Rules
1. **Contracts are law**: Implementations must conform to the contracts defined here.
2. **Versioning**: When a contract changes, update the version and ensure backward compatibility or a migration plan.
3. **Testing**: Contract tests must validate that implementations satisfy the contract.
4. **Documentation**: Each contract file should include a clear description of its scope and any breaking‑change policy.

## Usage
- Reference these contracts in integration code.
- Use contract‑testing tools (e.g., Pact, Spring Cloud Contract) to verify conformance.
- Update contracts before implementing new integration features.

---

**Version**: [CONTRACTS_001] | **Last Reviewed**: [DATE]
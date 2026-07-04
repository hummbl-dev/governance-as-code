# Governance as Code

`governance-as-code` explores how to represent decision rights, review gates, escalation paths, and institutional operating constraints as version-controlled, reviewable, testable, auditable, and agent-operable source material.

## Working Definition

`Governance-as-Code` means treating decision rights, review gates, escalation paths, and institutional operating constraints as canonical operational state expressed through files, schemas, examples, tests, and reviewable change history.

## Goals

- Define the domain clearly.
- Collect prior art and examples.
- Provide reusable schemas and templates.
- Support human review and agent execution.
- Preserve auditability, provenance, and governance boundaries.

## Non-Goals

- This repo is not a universal standard.
- This repo is not legal, security, compliance, or operational advice.
- This repo does not canonize HUMMBL/BaseN/Ownward concepts unless explicitly marked and audited.

## Packet status

- `seed` -> `v0.1-draft`

## v0.1 packet locations

- Boundary: [`docs/v0.1-boundary.md`](docs/v0.1-boundary.md)
- Schema: [`schemas/governance-as-code-v0.1.json`](schemas/governance-as-code-v0.1.json)
- Example: [`examples/governance-gate-v0.1.example.json`](examples/governance-gate-v0.1.example.json)
- Fixtures: [`fixtures/valid/governance-gate-v0.1.valid.json`](fixtures/valid/governance-gate-v0.1.valid.json), [`fixtures/invalid/governance-gate-v0.1.invalid.json`](fixtures/invalid/governance-gate-v0.1.invalid.json)
- Receipt: [`receipts/governance-as-code-v0.1-packet-receipt.md`](receipts/governance-as-code-v0.1-packet-receipt.md)

## Status

Public seed repository. Initial executable packet in progress as `seed` -> `v0.1-draft`.

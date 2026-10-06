# SILICONA Public Evidence Claim Policy

Status: PUBLIC RELEASE STANDARD
Effective: 2026-10-06

## Rule

The public evidence room exists to establish technical credibility through reproducible evidence, not presentation language.

Every material claim must have an evidence anchor.

## Allowed claim classes

MEASURED

A deterministic engineering tool or benchmark run produced the value.

ANALYTICAL ESTIMATE

The value is calculated from stated assumptions and is not presented as a measured tool result.

UNCLAIMED

The capability exists as a direction, implementation boundary, or research objective, but the public evidence package does not establish the claim.

CONFLICTING

Evidence disagrees. The claim is release-blocked until resolved.

## Release rules

Do not transform an implementation description into a production claim.
Do not transform a model response into an engineering result.
Do not transform provider registry membership into provider benchmark evidence.
Do not transform a commercial adapter into a customer-qualified commercial execution.
Do not transform a manufacturing profile into foundry acceptance.
Do not transform a historical benchmark into a current production metric.
Do not delete a negative result because a later experiment performed better.

## Evidence chain

Preferred chain:

Specification
→ deterministic execution
→ stage result
→ artifact digest
→ certification state
→ release record

For higher-value records:

Specification
→ deterministic execution
→ artifact manifest
→ signed provenance
→ independent verification
→ external witness
→ release capsule

## Update discipline

A public package is versioned.
A new package must carry a new release identifier and snapshot date.
The previous package remains a historical record.
# Post-Snapshot Software Readiness Addendum

Effective date: 2026-10-06

Public release status: NOT A NEW EVIDENCE RELEASE

Historical baseline: ER-2026-09-30-01

This addendum records software and qualification progress after the frozen 30 September 2026 public evidence snapshot. The historical evidence release remains immutable and authoritative for the measured figures in the four baseline PDFs.

## Measured engineering readiness

The current private SILICONA main revision is:

`3a612d255e61b56b0a7a0f2b422304b0d4eae047`

Fresh local qualification on the DreamStation engineering host produced:

| Gate | Result |
| :--- | :--- |
| TypeScript | PASS, zero compiler errors |
| ESLint | PASS |
| Production Next.js build | PASS |
| Standalone packaging | PASS |
| Production server startup | PASS |
| Commercial EDA adapter parser qualification | PASS |
| Evidence Passport signing and verification | PASS |
| Provider registry and honest fallback | PASS |
| Artifact storage qualification | PASS |
| Payment signature and checkout idempotency qualification | PASS |
| CSRF qualification | PASS |
| API rate-limit contention qualification | PASS |
| Durable security rate-limit qualification | PASS |
| Execution control-plane qualification | PASS |
| SDK smoke | PASS, 25/25 |

The SDK smoke was executed against a standalone production build through HTTP using a disposable database copy upgraded to the current schema. Real authentication, project operations, reference FIFO artifact reads, experiment reads, error handling, retry behavior, quota behavior, and cleanup all passed.

## Defects discovered during qualification

The hardening run found concrete implementation defects and repaired them before merge.

Most significant:

- The API rate limiter referenced the wrong identifier in its atomic update predicate. The production implementation now uses the correct API-key identifier.
- The qualification harness previously asserted provider fallbacks without explicitly enrolling the fallback providers. The test is now self-contained.
- Qualification code contained missing required fields and nullable-result assumptions. The cases are now type-correct and runtime-qualified.
- The production build used Unix-only asset-copy syntax. Standalone asset packaging is now cross-platform.
- The production start command used Unix-only environment assignment syntax. Production startup is now cross-platform.
- Graph UI and graph-engine contracts were reconciled.
- REST error-code and artifact-body type contracts were tightened.

## What this does not prove

This addendum does not establish:

- production PostgreSQL qualification
- external object-storage qualification
- live cloud execution
- fresh multi-provider model performance
- independent evidence witnessing
- licensed commercial EDA customer execution
- independent design-partner qualification
- sustained production observability
- manufacturing handoff
- measured silicon feedback

These remain explicit external gates.

## Evidence-room policy

The September 30 release remains frozen.

This document is contextual engineering progress, not a replacement benchmark release. A new public evidence release requires the evidence gate to close with a machine-readable run manifest, reproducibility information, updated integrity metadata, and explicit measured-versus-planned boundaries.

The public room therefore gets a stronger current engineering picture without rewriting the historical measurement record.

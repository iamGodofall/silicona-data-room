# SILICONA Public Evidence Room — Release Status

Release identifier: ER-2026-09-30-01
Public repository branch: main
Public evidence snapshot: 2026-09-30
Control review date: 2026-10-06

## Authority

This repository is the public evidence surface for SILICONA.

The private SILICONA repository remains the controlled engineering and product source. This public room never represents the private implementation as open source.

The public package is a dated evidence release. A later private engineering change does not silently rewrite this snapshot.

## Evidence state

The current public package contains four controlled documents:

| File | Purpose |
|---|---|
| `docs/01_Technical_Evidence_Dossier.pdf` | Technical system and measured engineering evidence |
| `docs/02_Investor_Brief.pdf` | Financing and business context |
| `docs/03_Benchmark_Protocol_v1.pdf` | Measurement rules and benchmark methodology |
| `docs/04_Competitor_Intelligence_v1.pdf` | Source-based competitive analysis |

The package also includes a supporting raw demonstration link.

## Claim hierarchy

A public claim must be traceable to one of:

1. A named measurement in the evidence package
2. A documented benchmark rule
3. A stated analytical estimate with its assumptions
4. A documented limitation or unclaimed result

The following are not inferred from the existence of source code, product screens, model output, or architecture diagrams:

- production availability
- customer qualification
- foundry acceptance
- independent laboratory reproduction
- multi-provider benchmark performance
- commercial EDA qualification
- signoff-grade post-route power or IR-drop
- sustained production-scale throughput

## Public snapshot versus live product

The public evidence documents are intentionally dated.

The controlled engineering record was reviewed again on 2026-10-06. New implementation work, production controls, provenance systems, commercial EDA adapters and internal qualification work are not promoted into this public package until a new evidence release is approved.

This prevents a stale PDF from being mistaken for a live product status page.

## Release integrity

Every public release must:

- identify the snapshot date
- identify every included document
- verify all expected files exist
- verify PDF file signatures
- scan tracked text for credential-like material
- verify README links to tracked evidence
- record the release commit
- preserve the previous release rather than silently replacing historical claims

## Golden-standard rule

A stronger engineering claim replaces a weaker claim only when its own evidence exists.

Historical evidence is retained.
Negative results are retained.
Retractions are explicit.
Unsupported claims are excluded.
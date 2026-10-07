# SILICONA Evidence Room

AI proposes. EDA calculates. Verification decides. Engineer approves.

Public technical evidence and diligence material for SILICONA, an evidence-gated engineering control plane for AI-assisted semiconductor design.

The repository is designed for engineers, EDA practitioners, cloud and compute partners, researchers, technical investors, and other reviewers who want to inspect the evidence rather than rely on presentation claims.

## Start Here

This repository is a versioned public evidence snapshot. The current package is ER-2026-09-30-01, based on measurements dated 30 September 2026. See [Release Status](./docs/00_RELEASE_STATUS.md) before relying on any figure.

For post-snapshot software qualification and launch-hardening progress, see [07 Post-Snapshot Software Readiness](./docs/07_Post_Snapshot_Software_Readiness_2026-10-06.md). This is contextual engineering progress, not a replacement public evidence release.

For worker execution isolation and resource-enforcement qualification, see [08 Worker Resource Isolation](./docs/08_Worker_Resource_Isolation_2026-10-07.md). This is also contextual software progress, not a replacement benchmark release.

For the external infrastructure, startup-program, partner and validation roadmap, see [09 External Validation Roadmap](./docs/09_External_Validation_Roadmap_2026-10-07.md). This is an execution roadmap, not evidence of program acceptance, production operation or customer validation.

1. Watch the raw terminal demonstration
2. Read the Technical Evidence Dossier
3. Read the Benchmark Protocol
4. Review the dated measured state below
5. Review the infrastructure requirements
6. Contact SILICONA for partner or compute discussions

[Below 90-Second Raw Terminal Demo](https://www.youtube.com/watch?v=1SfKJ0iRbfQ)

[01 Technical Evidence Dossier](./docs/01_Technical_Evidence_Dossier.pdf)

[03 Benchmark Protocol v1](./docs/03_Benchmark_Protocol_v1.pdf)

[02 Investor Brief](./docs/02_Investor_Brief.pdf)

[04 Competitor Intelligence v1](./docs/04_Competitor_Intelligence_v1.pdf)

## What This Repository Is

This is a public evidence room and technical data room.

The repository records:

- measured engineering results
- benchmark methodology
- toolchain and verification methodology
- provenance and artifact accounting
- infrastructure requirements
- competitive source material
- documented limitations and unclaimed results

The repository does not contain the proprietary SILICONA orchestration engine or agentic routing logic.

Engineering claims are intended to trace back to deterministic EDA execution and hash-bound artifacts. AI-generated output is not treated as an engineering verdict.

## Core Doctrine

AI Proposes

Architecture, RTL, testbenches, bounded repair candidates, and search candidates.

EDA Calculates

Yosys, SymbiYosys + Z3, Icarus Verilog, OpenSTA, OpenROAD, and KLayout perform the measurable engineering work.

Verification Decides

Certification states transition from deterministic tool verdicts rather than model assertions.

Engineer Approves

Policy-controlled gates define where automation is permitted and where engineering approval is required.

## Public Snapshot: 30 September 2026

The table below is a dated evidence snapshot, not a live production dashboard.

The figures below describe the current evidence corpus and the demonstrated SKY130 open-PDK reference flow. The evidence snapshot referenced by the current dossiers is dated 30 September 2026.

| Area | Recorded result |
| :--- | :--- |
| Physical closure | 14/14 pipeline stages passed |
| DRC | 0 violations |
| LVS | Dual LVS MATCH |
| Reference design | FIFO 16 × 32 |
| Devices | 20,962 |
| Nets | 11,544 |
| Post-route timing slack | +3.48 ns |
| Architecture search | matrix-mac +98.21% ADP improvement over human baseline, n=5 |
| stream-fifo RL | 0.00% improvement |
| Model evaluations | 177 |
| Model evaluation outcomes | 131 success, 1 partial, 51 HTTP-429 failures |
| Provider coverage in current model corpus | GLM |
| Hash-bound artifacts | 1,138 |
| Recorded stage runs | 563 |
| Recorded PASS rate | 81.0% |
| Classified flow failures | 104 |

The 0.00% stream-fifo RL result is retained as a negative result.

The 51 HTTP-429 failures are retained as measured evidence of the current single-provider dependency.

Post-route SPEF extraction and signoff-grade IR-drop are not claimed by this evidence room.

## Evidence Documents

| Document | Purpose | Primary readers |
| :--- | :--- | :--- |
| [01 Technical Evidence Dossier](./docs/01_Technical_Evidence_Dossier.pdf) | 14-stage pipeline, evidence hierarchy, certification ladder, infrastructure controls | Cloud architects, DevRel, EDA engineers |
| [02 Investor Brief](./docs/02_Investor_Brief.pdf) | Financing scenarios, business model progression, risks, and evidence-linked milestones | Deep-tech investors, strategic partners |
| [03 Benchmark Protocol v1](./docs/03_Benchmark_Protocol_v1.pdf) | Measurement rules, pinned toolchains, seeds, negative-result handling, and benchmark distributions | AI researchers, benchmark reviewers |
| [04 Competitor Intelligence v1](./docs/04_Competitor_Intelligence_v1.pdf) | Source-based review of the agentic EDA market | Market analysts, strategic partners |
| [10 External Infrastructure Program Matrix](./docs/10_External_Infrastructure_Program_Matrix_2026-10-07.md) | Current cloud/startup infrastructure routes, eligibility notes and execution order | Cloud partners, accelerators, infrastructure reviewers |
| [11 Commercial Pricing Standard](./docs/11_Commercial_Pricing_Standard_2026-10-07.md) | Current platform subscriptions, execution-credit model and certification offer | Customers, partners, diligence reviewers |

## Raw Demonstration

[Watch the below-90-second raw terminal demonstration](https://www.youtube.com/watch?v=1SfKJ0iRbfQ)

The demonstration is presented without voiceover or marketing narration. It shows the SILICONA dashboard, model evaluation records, terminal execution through the EDA flow, and the resulting verification output.

The video is supporting evidence, not a replacement for the benchmark protocol or artifact records.

## Infrastructure Requirement

The current evidence corpus was produced inside a constrained development environment with approximately 4 GB RAM and 10 GB disk capacity.

Phase B requires a properly provisioned environment for cross-provider measurement and larger Evidence Graph workloads.

| Workload | Required profile | Primary reason |
| :--- | :--- | :--- |
| Control plane | 8 vCPU / 32 GB RAM / 1 TB NVMe | Orchestration, policy engine, ledger |
| Solver fleet | 32+ cores / 256 GB RAM | Z3 workloads are compute and memory intensive |
| Physical design | 64 cores / 512 GB RAM / 8 TB NVMe | OpenROAD and KLayout workloads require substantial memory and local scratch |
| AI / GPU | 1 H200 for dense inference through 8 H200 for larger MoE workloads | Model inference and architecture-search workloads |

Phase 0 software prerequisites include concurrency limiting, queueing, disk protection, blob-store offloading, timeout tuning, and a production database decision. The Technical Evidence Dossier contains the detailed requirements.

## What Is Demonstrated vs Unclaimed

Demonstrated results are tied to the evidence corpus described above.

The following are deliberately not presented as completed claims:

- signoff-grade IR-drop analysis
- post-route SPEF extraction as a completed signoff claim
- independent reproduction by an external laboratory
- broad cross-provider model conclusions from the current single-provider model corpus
- production-scale compute performance outside the constrained development environment

These boundaries are part of the evidence standard.

## Reproduction and Audit Path

A technical reviewer should be able to move through the evidence in this order:

README → Technical Evidence Dossier → Benchmark Protocol → Raw Terminal Demo → artifact and run records → reproduction environment

The current public room provides the first four layers. Release integrity controls are now automated through GitHub Actions. Expanding the public machine-readable artifact manifest and reproducible environment remains part of the next evidence-room development phase.

## Partner and Compute Program

SILICONA is entering Phase B of its Cross-Provider Measurement Campaign.

The immediate technical requirement is compute capacity for controlled comparison of:

- model providers
- inference hardware
- solver throughput
- physical-design throughput
- benchmark repeatability
- failure modes
- cost per verified engineering result

Partner discussions are focused on measurable workloads and reproducible evidence rather than generic sponsorship.

## IP Boundary

This repository contains evaluation data, methodology, benchmark material, infrastructure planning, and diligence documents.

The core SILICONA orchestration engine, agentic routing logic, and proprietary implementation remain private.

## Release controls

See [Claim Policy](./docs/05_CLAIM_POLICY.md). Public changes are expected to preserve dated evidence, explicit limitations, reproducibility information, and negative results.

## Contact

Themba Enock Mpehle  
Founder, Enock Labs  
founder@silicona.dev  
South Africa, operating globally

# SILICONA Evidence Room

**AI proposes. EDA calculates. Verification decides. Engineer approves.**

This repository serves as the public evidence room and technical data room for **SILICONA**, an evidence-gated engineering control plane for AI-assisted semiconductor design. 

It contains the clinical technical dossiers, benchmark protocols, competitive landscape analysis, and infrastructure requirements used for technical partnerships, compute federation provisioning, and institutional diligence.

> **Note on IP:** This repository contains evaluation data, methodology, and infrastructure planning. The core SILICONA orchestration engine and agentic routing logic remain proprietary. 

---

## 1. The Core Doctrine
SILICONA is not an AI chat wrapper for hardware. It is an execution system where AI output is never recorded as fact. Only deterministic, open-source EDA tool runs produce measured results, and every engineering claim traces to a hash-bound artifact in a queryable ledger.

*   **AI Proposes:** Architecture, RTL, testbenches, and bounded repair candidates.
*   **EDA Calculates:** Yosys, SymbiYosys+Z3, Icarus Verilog, OpenSTA, OpenROAD, KLayout.
*   **Verification Decides:** Certification states transition only on deterministic tool verdicts.
*   **Engineer Approves:** Policy-controlled gates govern bounded automation.

---

## 2. The Data Room (Documents)

All documents below are clinical records of what is implemented, tool-verified, artifact-bound, and not yet independently reproduced. Superlatives and inferred competitor capabilities are excluded.

| Document | Purpose | Target Audience |
| :--- | :--- | :--- |
| **[01_Technical_Evidence_Dossier.pdf](./docs/01_Technical_Evidence_Dossier.pdf)** | Clinical record of the 14-stage pipeline, E0-E4 evidence hierarchy, L1-L10 certification ladder, and Phase 0 infrastructure controls. | Cloud Architects, DevRel, EDA Engineers |
| **[02_Investor_Brief.pdf](./docs/02_Investor_Brief.pdf)** | Financing scenarios, business model progression, risk register, and evidence-based milestones. | Deep-Tech VCs, Strategic Partners |
| **[03_Benchmark_Protocol_v1.pdf](./docs/03_Benchmark_Protocol_v1.pdf)** | Formal measurement standard: pinned toolchains, recorded seeds, mandatory negative results, and distributions over headlines. | AI Researchers, Benchmark Auditors |
| **[04_Competitor_Intelligence_v1.pdf](./docs/04_Competitor_Intelligence_v1.pdf)** | Evidence-scored landscape of the agentic-EDA market (14 primary sources, tiered E1-E4). | Market Analysts, Strategic Partners |

---

## 3. Current Measured State (Live DB Extract)
*The following figures are extracted directly from the SILICONA engineering-memory database. They represent the current demonstrated capability ceiling on the SKY130 open-PDK.*

*   **Physical Closure [E3]:** 14/14 pipeline stages passed. Reference FIFO achieved **DRC 0 violations** and **Dual LVS MATCH** (foundry deck + deterministic structural compare). 20,962 devices / 11,544 nets. Post-route timing slack: +3.48 ns. *(Note: Post-route SPEF extraction and signoff-grade IR-drop are explicitly unclaimed).*
*   **Architecture Search [E3]:** matrix-mac family achieved **+98.21% area/delay product (ADP)** improvement over human baseline (n=5, variance ±0.00). stream-fifo RL mode achieved 0.00% (honest negative published as data).
*   **Model Evaluation [E3]:** 177 AI model evaluations recorded. 131 success, 1 partial, **51 HTTP-429 rate-limit failures**. All 177 rows are currently measured against a single provider (GLM). The 51 failures are published as evidence of single-provider dependency.
*   **Provenance [E3]:** 1,138 hash-bound artifacts. 563 recorded stage runs (81.0% PASS rate). 104 flow failures classified with root causes.

---

## 4. The Infrastructure Ask (Production BOM)
The platform achieved its current evidence corpus inside a constrained development sandbox (4GB RAM / 10GB Disk). To execute Phase B (Cross-Provider Measurement) and scale the Evidence Graph, the following Production BOM is required:

| Workload Pool | Hardware Profile Required | Justification (Tool Architecture) |
| :--- | :--- | :--- |
| **A. Control Plane** | 8 vCPU / 32GB RAM / 1TB NVMe | Orchestrator, Policy Engine, Postgres-class Ledger |
| **B. Solver Fleet** | 32+ Cores (≥3.5 GHz) / 256GB RAM | Z3 SMT solving is single-threaded per property and RAM-bound |
| **C. Physical Design** | 64 Cores / 512GB RAM / 8TB NVMe | OpenROAD P&R and KLayout DRC/LVS require high-IOPS local scratch |
| **D. AI / GPU** | 1x H200 (Dense) to 8x H200 (MoE) | Sovereign inference for GLM-4.5; L10 RL architecture search |

*For full Phase 0 code-level prerequisites (concurrency limiters, blob store offloads), see Section 13 of the Technical Evidence Dossier.*

---

## 5. Video Demonstration
**[Link to 90-Second Raw Terminal Demo]**
*No voiceover. No marketing. Just the dashboard, the 177 evaluations (including the 51 HTTP-429 failures), the terminal executing OpenROAD, and the final DRC 0 / LVS MATCH output.*

---

## Contact & Partnerships
We are executing **Phase B** of our Cross-Provider Measurement Campaign. We are looking for technical partners to sponsor the compute tiers outlined in our BOM to benchmark hardware/models against our deterministic EDA gates.

**Themba Enock Mpehle** | Founder, Enock Labs  
📧 founder@silicona.dev  
🌍 South Africa (Operating globally)

# SILICONA External Validation and Infrastructure Roadmap

Status: PUBLIC CONTEXTUAL ROADMAP
Effective: 2026-10-07

This document explains the next externalization phase after the dated SILICONA evidence snapshot.

It does not replace the dated evidence release, and it does not convert implementation into a production claim.

## The transition

SILICONA has a demonstrated open-PDK physical-signoff boundary.

The next step is external proof:

**built product → external infrastructure → independent qualification → customer workload → manufacturing feedback**

The remaining work is primarily external execution and validation rather than another reinvention of the core product.

## External gates

The roadmap targets:

- production PostgreSQL
- external object storage
- live Linux cloud workers
- Linux resource enforcement
- hosted CI
- multi-provider AI measurement
- external evidence witnessing
- commercial EDA execution
- independent technical review
- customer design-partner execution
- production observability
- manufacturing handoff
- silicon feedback

## Infrastructure model

SILICONA is designed as a distributed control plane with disposable execution workers.

The target production topology is:

`Edge → API/Web → Queue/Scheduler → Isolated Worker Fleet → Artifact Store`

Production state belongs in PostgreSQL.

Oversized evidence belongs in object storage.

Workers are replaceable execution units with:

- exact toolchain identity
- project/revision binding
- CPU/memory/disk ceilings
- process isolation
- network policy
- credential expiry and revocation
- measured telemetry
- evidence-bound artifacts

## External program strategy

SILICONA is pursuing multiple infrastructure and ecosystem routes rather than a single vendor.

Priority categories:

1. Cloud credits and compute sponsorship
2. Semiconductor startup programs
3. Commercial EDA startup programs
4. Foundry and shuttle relationships
5. Independent technical review
6. Customer design partners
7. Startup funding and accelerators

## Program targets

### Cloud

AWS Activate

Google for Startups

Microsoft for Startups

Cloudflare for Startups

NVIDIA Inception

Huawei Cloud Startup Program

Oracle for Startups

DigitalOcean Startups

Alibaba Cloud Startup Catalyst / AI Catalyst

### Semiconductor ecosystem

Arm Flexible Access for Startups

Synopsys Startup Program

Siemens for Startups

Silicon Catalyst

ChipFoundry

Tiny Tapeout

Technology Innovation Agency

## Validation model

External validation is structured as measured workloads.

A partner does not need to accept a slide deck as proof.

The preferred exchange is:

1. Partner provides infrastructure, software, IP or execution access.
2. SILICONA runs a fixed workload.
3. The environment, inputs and toolchain are recorded.
4. Outputs and hashes are captured.
5. Resource and cost telemetry are recorded.
6. The result becomes an externally reviewable evidence package.

## Customer validation

The first customer validation targets are:

- fabless semiconductor startups
- AI accelerator teams
- ASIC/design houses
- research and advanced engineering groups
- EDA partners
- cloud/compute partners
- foundry/shuttle partners

A first pilot should use one bounded real workload with an agreed baseline and a measurable outcome.

## Evidence boundary

The public evidence room retains the distinction between:

INTERNAL

CONTROLLED

QUALIFIED

CERTIFIED

PRODUCTION

No external program award, cloud account, partner conversation or deployment manifest changes a claim state without measured evidence.

## Immediate objective

Secure enough external capacity to convert the current SILICONA control-plane implementation into measured cloud execution, fresh multi-provider benchmarks, commercial EDA qualification and a first real design-partner workload.

## Public evidence

Start with the dated evidence release and current contextual engineering updates:

- Technical Evidence Dossier
- Benchmark Protocol
- Investor Brief
- Competitor Intelligence
- Post-Snapshot Software Readiness
- Worker Resource Isolation

## Official program references

AWS:
https://aws.amazon.com/aws-startups/learn/applying-for-aws-activate-credits-a-step-by-step-guide/

Google Cloud:
https://cloud.google.com/startup

Microsoft:
https://learn.microsoft.com/en-us/azure/signups/overview

Cloudflare:
https://www.cloudflare.com/startups/

NVIDIA:
https://www.nvidia.com/en-us/startups/

Huawei Cloud:
https://startup.huaweicloud.com/intl/en-us/

Alibaba Cloud:
https://www.alibabacloud.com/en/startup/cloudcreditredemption

Arm:
https://www.arm.com/products/flexible-access/startup

Synopsys:
https://www.synopsys.com/cloud/startup-program.html

Siemens:
https://www.siemens.com/en-us/company/siemens-software-for-startups/

ChipFoundry:
https://chipfoundry.io/

Silicon Catalyst:
https://siliconcatalyst.com/application

Technology Innovation Agency:
https://www.tia.org.za/funding-instruments/

Y Combinator:
https://www.ycombinator.com/apply

Techstars:
https://www.techstars.com/accelerators

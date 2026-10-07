# Worker Resource Isolation Software Readiness Addendum

Effective date: 2026-10-07

Public evidence release status: CONTEXTUAL SOFTWARE PROGRESS

Historical evidence baseline: ER-2026-09-30-01

## New software qualification

Fresh DreamStation qualification established a per-job execution supervisor for the worker boundary.

Measured results:

- Worker resource isolation: PASS
- Worker resource recovery: PASS
- Existing execution control plane: PASS, 22/22 checks

Resource isolation passed:

- isolated handler success
- CPU reservation termination
- disk reservation termination
- external cancellation termination
- per-job workspace cleanup

Recovery passed:

- leased-job resource binding
- measured resource violation
- retry after resource violation
- second resource violation
- dead-letter after maximum attempts

## Runtime mechanism

The worker now executes handler jobs in a separate child process with a job-specific workspace.

The supervisor measures CPU, peak RSS and workspace disk use across the child process tree. Windows termination uses process-tree termination through `taskkill /T /F`. Linux deployments use process-tree termination and should add cgroup enforcement at the target production runtime.

## Claim boundary

The measured software behavior applies to the DreamStation Windows qualification host.

This addendum does not establish production worker isolation for an external cloud or customer runtime.

External PostgreSQL, object storage, cloud worker execution, fresh multi-provider benchmarks, commercial EDA customer execution, independent partner qualification, manufacturing handoff and silicon feedback remain separate external gates.

The historical ER-2026-09-30-01 release remains unchanged.

# Proposed architecture

Status: design only.

| Component | Proposed responsibility |
| --- | --- |
| User interface | Plain-language task intake, drafts, approvals and history |
| API service | Authentication, authorization, tenant scoping and workflow requests |
| Agent orchestration | Typed tasks, tool allowlists, evidence and escalation |
| Persistence | Tenant-owned records, workflow state, audit trail and credential references |
| Integration layer | Provider adapters and authorized business-system access |

Tenant identity must be established by server-side authorization and propagated to every query and tool call. Secrets should live in server-side secret storage, never in prompts, browser bundles or source control. Record model/provider versions, calculation versions and reviewed outputs for financial workflows.

Define reliable retry/idempotency behavior, failure recovery and monitoring before production use. No architecture diagram or specification in this folder proves these controls have been implemented.

# ADR-001 — Infrastructure and Environment Isolation

- Status: Accepted
- Date: 2026-11-25
- Constitutional alignment: P03, P04, P07

## Context

AI Cost Lens requires an independent development
environment that supports reproducible engineering
activities without introducing unnecessary infrastructure
costs or affecting unrelated applications.

Two existing infrastructure environments were evaluated
against resource availability, operating system
maintainability and operational constraints.

## Decision

Use an existing Linux environment for initial development.

Development activities run under a dedicated,
unprivileged operating system account with an independent
workspace and repository-scoped authentication.

Administrative privileges are reserved for explicitly
authorized infrastructure provisioning.

GitHub is the authoritative source repository.

Public deployment requires separate security assessment
and approval.

## Alternatives Considered

### Existing legacy environment

Rejected because its older operating system and runtime
baseline introduce additional maintenance concerns.

### Independent cloud infrastructure

Deferred because current development requirements can
be satisfied without additional infrastructure provisioning.

### Managed static hosting

Retained as a potential public distribution option.
It does not replace the need for a controlled
development workflow.

## Consequences

### Benefits

- Reduced initial infrastructure expenditure.
- Independent development credentials.
- Restricted development privileges.
- Reproducible repository-based workflow.

### Trade-offs

- Shared infrastructure introduces resource contention
  and operational dependencies.
- Account-level isolation does not provide the same
  security boundary as a dedicated virtual machine.
- Public hosting requires additional security controls.

## Validation

- Dedicated account and workspace provisioning.
- Restricted directory permissions.
- Repository-scoped authentication.
- Successful local and remote commit synchronization.

The decision authorizes development activities only.
It does not authorize public deployment.

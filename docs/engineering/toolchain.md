# Development Toolchain

## Verified Baseline

The following toolchain was validated on 2026-11-26.

| Component | Version | Management |
|---|---|---|
| Git | 2.34.1 | System |
| uv | 0.13.10 | User-local |
| uvx | 0.13.10 | User-local |
| Python | 3.12.16 | uv managed |
| Specify CLI | 1.4.5 | uv tool |

## Specification Framework

Repository: https://github.com/github/spec-kit

Release: v1.4.5

Resolved source commit:
`6ba8beefff8d6408cadd62038e92d459093e33a8`

Integration: Generic

Workflow scripts: Bash

Constitution: `.specify/memory/constitution.md`

## Runtime Management

Development dependencies must remain isolated from
unrelated applications and system-wide runtimes.

Project tooling must execute without administrative
privileges during normal development activities.

Application runtime and framework dependencies must
be validated for compatibility before implementation.

Application dependency manifests and lockfiles will
provide the authoritative application version baseline.

## Reproducibility

Material toolchain changes require documented rationale
and compatibility validation.

Build and test procedures must be reproducible using
the recorded runtime and dependency versions.

The project constitution establishes the applicable
engineering governance and release requirements.

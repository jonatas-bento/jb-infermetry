# ADR-002 — Independent Development Toolchain

- Status: Accepted
- Date: 2026-11-26
- Constitutional alignment: P04, P07, P09

## Context

The development environment contains system runtimes
used by unrelated applications.

Account-specific runtime discovery also identified
differences between available Node.js installations.

Replacing shared runtimes could introduce compatibility
and operational risks outside the project boundary.

## Decision

Use independently managed development runtimes and
user-local engineering tools.

Python tooling is managed through uv.

GitHub Spec Kit is installed using an explicitly
selected managed Python runtime and a pinned release.

The application runtime will also be managed independently
of system-wide Node.js installations.

Exact application dependency versions will be established
through compatibility validation and recorded in the
application dependency manifests and lockfiles.

## Alternatives Considered

### System-wide runtime upgrades

Rejected because unrelated applications may depend
on the existing runtime versions.

### Shared global development dependencies

Rejected because dependency changes could affect other
projects and weaken reproducibility.

### Containerized development

Retained as an alternative where stronger environmental
isolation or build portability becomes necessary.

## Consequences

### Benefits

- Independent dependency lifecycle.
- Reduced interference with existing applications.
- Explicit runtime selection.
- Improved build reproducibility.

### Trade-offs

- Additional user-local runtime storage.
- Independent runtime maintenance responsibilities.
- Explicit environment activation may be necessary.

## Validation

The Python toolchain and Specify CLI have been installed
under the dedicated project account.

System Node.js and Python version checks remained
unchanged following these installations.

The application-specific Node.js runtime requires its
own installation and acceptance validation.

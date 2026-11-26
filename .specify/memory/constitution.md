# JB Infermetry Constitution

## Core Principles

### P01 — Specification First (NON-NEGOTIABLE)

Every feature MUST originate from documented requirements,
user scenarios and measurable acceptance criteria.

An approved specification MUST precede feature
implementation. Implementation plans MUST explain
architectural decisions and relevant trade-offs.

Changes to approved requirements MUST be reflected
in the specification before acceptance.

Community feedback MUST be recorded and evaluated
before becoming committed implementation scope.

Rationale: implementation must solve an identified
problem rather than merely introduce functionality.

### P02 — Cost Accuracy (NON-NEGOTIABLE)

Cost calculations MUST be deterministic, reproducible
and independently testable.

Identical inputs, pricing versions and calculation
rules MUST produce identical results.

Monetary calculations MUST define precision and
rounding behavior and MUST avoid uncontrolled
floating-point rounding errors.

Token consumption MUST be represented using
explicit, non-overlapping billing categories.

Cached input MUST NOT be counted again as
uncached input.

Unsupported pricing categories MUST NOT silently
default to zero.

The product MUST distinguish estimated cost,
measured usage cost and actual billed cost.

Rationale: financial transparency depends on
correctness, reproducibility and honest reporting.

### P03 — Privacy by Design (NON-NEGOTIABLE)

The product MUST minimize data collection and
processing to what is necessary for its purpose.

The initial release MUST NOT require API keys,
conversation contents, source code uploads,
personal information or provider credentials.

Cost estimation MUST be possible without sending
user calculation inputs to external AI services.

Future data collection or integrations MUST undergo
documented privacy and security assessment.

Credentials and private engineering evidence
MUST NOT be committed to source control.

Rationale: users must be able to understand AI
economics without exposing sensitive information.

### P04 — Architectural Simplicity

The architecture MUST favor the simplest solution
that satisfies approved functional and non-functional
requirements.

Cost calculation logic MUST remain independent
of presentation frameworks and external services.

Additional infrastructure, services and dependencies
MUST have documented engineering justification.

The initial release MUST favor client-side execution
unless approved requirements justify another approach.

Development tooling MUST remain isolated from
unrelated production applications.

Rationale: unnecessary complexity increases
operational costs, risks and maintenance effort.

### P05 — Evidence-Based Delivery

Engineering claims MUST be supported by verifiable
execution evidence, tests or documented observations.

Acceptance records MUST identify the requirement,
validation procedure, observed result and status.

Evidence MUST distinguish observed results,
assumptions, simulations and future projections.

Unverified functionality MUST NOT be reported
as implemented or accepted.

Published engineering reports MUST exclude secrets,
private infrastructure details and confidential data.

Rationale: delivery confidence must originate from
evidence rather than subjective progress claims.

### P06 — Pricing Transparency (NON-NEGOTIABLE)

Pricing records MUST identify the provider, model,
currency, billing unit and source.

Records MUST include an effective date when known
and a verification date. Unknown effective dates
MUST be explicitly identified.

Pricing data MUST be versioned and reproducible.

Provider-specific pricing rules MUST NOT be
represented as universal billing behavior.

Cached input, cache creation, output and other
billable categories MUST be distinguished
where applicable and supported.

The application MUST disclose unsupported billing
dimensions, estimation assumptions and material
limitations.

Unknown prices MUST NOT be represented as free.

Rationale: an accurate calculation is insufficient
when its pricing assumptions are misleading.

### P07 — Open-Source Independence

Project source code MUST be independently authored
or incorporated under compatible licensing terms.

Third-party resources MUST retain required
attribution and licensing notices.

Dependencies MUST be reviewed for licensing,
maintenance and security implications.

Employer-owned source code, internal credentials,
confidential information and restricted datasets
MUST NOT be incorporated into the project.

Public release MUST be preceded by intellectual
property and licensing review.

Rationale: the project must maintain legal,
technical and operational independence.

### P08 — Accessible User Experience

The product MUST present costs using understandable
labels, units and calculation assumptions.

Estimated results MUST be visibly identified
as estimates.

The user interface MUST explain validation
failures without misleading the user.

Core functionality MUST support keyboard navigation
and meaningful accessible control labels.

Color MUST NOT be the sole means of conveying
important information.

The interface MUST support both technical and
non-technical audiences.

Rationale: financial transparency is valuable only
when users can understand and act on it.

### P09 — Quality Before Release (NON-NEGOTIABLE)

Every release MUST satisfy its approved acceptance
criteria and mandatory quality gates.

Cost calculation and input validation logic MUST
have automated tests covering normal, boundary
and invalid-input scenarios.

Tests for new calculation behavior MUST be defined
before its implementation.

Defects in calculation correctness, privacy or
security MUST block affected releases until resolved.

Dependency versions and build procedures MUST
be recorded sufficiently to reproduce releases.

Incomplete or failing acceptance criteria MUST NOT
be silently reclassified as successful.

Rationale: trust in the product requires measurable
quality rather than delivery speed alone.

## Product and Technical Constraints

### Cost Classification

The product MUST distinguish:

- Estimated cost: calculated from hypothetical or
  expected consumption and applicable pricing.
- Measured usage cost: calculated from actual
  reported consumption and applicable pricing rules.
- Actual billed cost: expenditure confirmed through
  authoritative provider billing records.

These classifications MUST NOT be used interchangeably.

### Initial Product Scope

The initial product MUST focus on deterministic
cost estimation for individual AI activities.

The domain model MUST accommodate cached input
where applicable pricing is available.

Full multi-turn session analysis, usage imports,
billing reconciliation and provider integrations
require separately approved specifications.

The discovery item ACL-FEATURE-001 does not itself
authorize feature implementation.

### Architecture Constraints

- The cost engine MUST be independently testable.
- Pricing data MUST be versioned.
- Presentation and calculation logic MUST be separated.
- The MVP MUST NOT depend on paid AI inference.
- Technology choices MUST be documented when material.
- Public deployment requires separate security approval.

## Development Workflow and Quality Gates

### Specification-Driven Lifecycle

Engineering work MUST follow an appropriate sequence:

1. Product discovery and problem definition.
2. Feature specification and acceptance criteria.
3. Clarification of material ambiguities.
4. Architecture and implementation planning.
5. Task decomposition and traceability.
6. Implementation and automated validation.
7. Acceptance review and release decision.

Applicable requirements MUST remain traceable
through implementation and validation.

### Version Control

GitHub is the authoritative source repository.

Changes MUST use meaningful commits and be
reviewed before integration into the main branch.

Material architecture decisions MUST be recorded
as Architecture Decision Records.

Private credentials, local secrets and unsanitized
operational evidence MUST remain outside the
version-controlled source tree.

### Mandatory Quality Gates

Before accepting a feature or release, reviewers
MUST verify applicable requirements covering:

- Specification completeness.
- Constitutional compliance.
- Cost calculation correctness.
- Input validation.
- Pricing provenance and limitations.
- Privacy and security.
- Automated test results.
- Build reproducibility.
- User experience and accessibility.
- Documentation and licensing.

Acceptance criteria that do not apply MUST have
a documented rationale.

## Governance

This constitution governs JB Infermetry engineering
practices, feature specifications, implementation
plans and release decisions.

All material changes and pull request reviews MUST
assess constitutional compliance.

When a specification conflicts with this constitution,
the conflict MUST be resolved before implementation
or release acceptance.

Amendments MUST include documented rationale,
impact assessment, explicit maintainer approval
and an updated version.

Where applicable, amendments MUST include a
migration plan for affected specifications and code.

Constitutional versions follow semantic versioning:

- MAJOR: incompatible governance changes or removal
  or redefinition of established principles.
- MINOR: new principles or materially expanded
  governance requirements.
- PATCH: clarifications, corrections and wording
  changes without semantic impact.

Non-negotiable principles MUST NOT be bypassed
through implementation-level exceptions.

Other deviations require documented justification,
risk assessment, scope, expiration and maintainer
approval.

Unresolved non-negotiable violations MUST block
the affected feature or release.

Governance changes MUST be committed to source
control after review.

**Version**: 1.0.1 | **Ratified**: 2026-11-26 | **Last Amended**: 2026-11-26

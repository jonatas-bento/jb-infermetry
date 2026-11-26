# ADR-004 — Deterministic Cost Calculation Architecture

- Status: Proposed
- Date: 2026-11-26
- Constitutional alignment: P02, P03, P04, P06, P09

## Context

AI Cost Lens aims to make everyday AI consumption
economics understandable and reproducible.

Community feedback has additionally identified
session-level cost visibility and prompt caching
as relevant product capabilities.

The initial product must provide useful cost estimates
without requiring API credentials or paid inference.

## Proposed Decision

Implement a client-side application with an independently
testable, framework-independent cost calculation engine.

Use a versioned pricing registry containing applicable
billing categories and pricing provenance.

The presentation layer consumes calculation results
without duplicating the underlying pricing logic.

The domain model distinguishes cached input, uncached
input and output consumption where applicable.

Additional billing categories require explicitly
documented pricing rules.

Unknown or unsupported prices must not be silently
interpreted as zero.

## Proposed Technology Direction

- TypeScript for application and domain implementation.
- Angular for the presentation layer.
- Versioned structured pricing data.
- Automated calculation and input validation tests.
- Static application distribution where appropriate.

Framework and dependency versions require compatibility
validation before implementation.

## Alternatives Considered

### Backend-first architecture

Deferred because the initial requirements do not
establish a need for server-side calculation or storage.

### Live provider API integration

Deferred because it introduces authentication,
network dependencies and potentially paid inference.

### Presentation-coupled calculation logic

Rejected because it reduces independent testability
and complicates future session-level analysis.

## Consequences

### Benefits

- Independently testable calculations.
- Minimal infrastructure requirements.
- Reduced exposure of user calculation inputs.
- Reusable calculation logic for future features.

### Trade-offs

- Pricing freshness depends on registry maintenance.
- Provider-specific billing dimensions require
  explicit modeling.
- Actual billed costs cannot be established through
  hypothetical token estimates alone.

## Acceptance Conditions

This proposal requires:

- An approved feature specification.
- Defined pricing and token consumption contracts.
- Explicit monetary precision and rounding rules.
- Validated application runtime compatibility.
- Documented acceptance criteria and test scenarios.
- Constitutional compliance review.

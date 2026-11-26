# ACL-FEATURE-001 — Agentic Session Cost Analyzer

## Metadata

- Created: 2026-11-26
- Status: Discovery
- Proposed priority: High
- Source: Build in Public community feedback
- Independent contributors: 2
- Implementation status: Not started
- Target release: TBD

## Problem Statement

Developers using AI coding agents may lack
visibility into the cost dynamics of multi-turn
coding sessions.

Context accumulation, repeated input tokens,
prompt caching, tool calls and provider-specific
pricing policies can influence total session cost.

A monthly aggregate alone may not explain
how these costs are generated.

## User Story

As a developer using AI coding agents,
I want to understand and compare the estimated
cost of multi-turn coding sessions,
including context accumulation and caching,
so that I can make informed decisions
about my AI consumption.

## Community Signals

Two independent community contributors
expressed interest in session-level cost
visibility and caching comparisons.

One contribution additionally identified
per-turn cost visualization and context
accumulation as relevant capabilities.

These signals support further product discovery
but do not establish broad market demand.

## Candidate Requirements

- CR-001: Estimate cost per model invocation.
- CR-002: Aggregate costs across a session.
- CR-003: Distinguish cached and uncached input.
- CR-004: Visualize context growth across turns.
- CR-005: Compare caching scenarios.
- CR-006: Explain calculation assumptions.
- CR-007: Identify applicable pricing sources.
- CR-008: Distinguish estimates from billed costs.

## Architectural Implications

The foundational cost engine should support
distinct token consumption categories,
including cached input where applicable.

Session-level calculations should reuse the
same deterministic cost calculation engine.

Provider-specific caching rules must not be
represented as universal billing behavior.

Unsupported pricing categories must not
silently default to zero.

## Scope Decision

The initial MVP remains focused on deterministic
cost estimation for individual AI activities.

Cached input should be considered when defining
the initial pricing and consumption contracts.

Full multi-turn simulation and session
visualization require a separate specification,
implementation plan and acceptance criteria.

## Privacy Considerations

Initial simulations must not require:

- API credentials
- Conversation content
- Source code uploads
- Personally identifiable information

## Open Questions

1. Which providers should be supported first?
2. How should cache creation charges be modeled?
3. How should cache expiration be represented?
4. Should context compaction be configurable?
5. How should multiple tool calls be aggregated?
6. Which usage export formats should be supported?

## Discovery Exit Criteria

- Requirements reviewed and prioritized.
- MVP boundaries explicitly established.
- Pricing categories formally defined.
- Provider-specific assumptions documented.
- Dedicated feature specification approved.

## Success Measure

Users should be able to understand the
estimated cost difference between comparable
AI session scenarios and reproduce the
calculation using documented assumptions.

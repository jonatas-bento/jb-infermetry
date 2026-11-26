# ADR-006 — Project Identity and Naming

- Status: Accepted for local adoption
- Date: 2026-11-26
- Constitutional alignment: P04, P05, P07

## Context

The project was initially established under the
name AI Cost Lens.

Preliminary naming research identified existing
software products using similar names in AI cost
analysis and financial operations.

The project requires a distinctive identity that
communicates its technical purpose while reducing
avoidable naming confusion.

## Decision

Adopt JB Infermetry as the project identity.

The name combines the maintainer's initials with
concepts associated with inference and measurement.

The canonical project identity is:

- Display name: JB Infermetry
- Repository slug: jb-infermetry
- Engineering identifier prefix: JBI
- Product category: AI Cost Intelligence
- Tagline: Make AI costs measurable.

Historical architectural decisions, evidence
identifiers and discovery records remain valid.

New engineering artifacts use the JBI prefix.

Repository history must be preserved during migration.

Operational identifiers remain independent of product
branding unless a separate operational requirement
justifies their modification.

## Alternatives Considered

### AI Cost Lens

Not retained because preliminary research identified
an existing project using the same product name.

### JB CostScope

Not selected because an existing CostScope platform
operates in a related financial operations domain.

### JB Inference Lens

Not selected because preliminary research identified
an existing InferenceLens project in a related domain.

### JB Infermetry

Selected because it combines a personal identifier
with a coined technical name representing inference
measurement and analysis.

## Consequences

### Benefits

- More distinctive project identity.
- Clear association with AI inference measurement.
- Preservation of engineering history.
- Minimal operational migration requirements.
- Compatibility with future product capabilities.

### Trade-offs

- The coined name requires explanation to new audiences.
- Existing public references may require clarification.
- Preliminary naming research cannot establish
  worldwide trademark availability.

## Migration Governance

Current product documentation uses the new identity.

Historical records retain their original context.

Constitution version 1.0.1 introduces a branding-only
amendment without changing engineering principles.

Repository renaming must preserve commit history and
maintain verified repository-scoped authentication.

The name remains subject to applicable trademark and
intellectual property obligations.

Public adoption requires a separate publication
readiness assessment.

## References

- Brazilian National Institute of Industrial Property:
  https://www.gov.br/inpi/pt-br
- WIPO Global Brand Database:
  https://branddb.wipo.int/
- Apache Software Foundation naming guidance:
  https://www.apache.org/foundation/marks/naming.html

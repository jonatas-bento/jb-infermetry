# ADR-005 — Open-Source Licensing and Intellectual Property Governance

- Status: Accepted
- Date: 2026-11-26
- Constitutional alignment: P03, P06, P07, P09

## Context

JB Infermetry is an independently maintained open-source
initiative intended to make AI consumption costs
understandable, reproducible and accessible.

The distribution model must enable broad adoption,
modification and redistribution while respecting
intellectual property and third-party obligations.

## Decision

Adopt the MIT license for original project material
that the maintainer has the rights to license.

Preserve applicable third-party copyright notices,
license terms and attribution.

Maintain the project license in the repository root
and third-party notices in THIRD_PARTY_NOTICES.md.

The project must remain independent of employer-owned
source code, confidential information and restricted
resources.

Public distribution must respect applicable intellectual
property, privacy and third-party licensing obligations.

Project licensing does not imply affiliation with or
endorsement by external organizations or AI providers.

## Alternatives Considered

### Apache License 2.0

A permissive license with explicit patent licensing
provisions.

Not selected because the maintainer prefers the
simplicity of MIT for the current project scope.

### GNU General Public License v3.0

A copyleft license that establishes corresponding
source distribution obligations for covered software.

Not selected because the project intends to permit
both open-source and proprietary downstream reuse.

### Public repository without an explicit license

Rejected because source visibility alone does not
establish general reuse and redistribution permissions.

## Consequences

### Benefits

- Broad permissions for use and modification.
- Commercial and non-commercial reuse.
- Low licensing complexity.
- Clear attribution requirements.
- Accessible community participation.

### Trade-offs

- Downstream modifications need not be published.
- Commercial reuse does not require compensation
  to the original maintainer.
- MIT does not contain an express patent grant.
- License compliance requires ongoing dependency review.

## Governance

The maintainer confirms the necessary rights to license
the original project material and accepts the permissions
granted under MIT.

Third-party material remains subject to its applicable
license and copyright conditions.

New dependencies must undergo licensing and security
review before acceptance.

License changes require explicit maintainer approval
and assessment of existing distribution rights.

No license decision substitutes for applicable legal
or contractual obligations.

## References

- MIT License: https://opensource.org/license/mit
- Open Source Definition: https://opensource.org/osd
- SPDX MIT identifier: https://spdx.org/licenses/MIT.html
- GitHub Open Source Guides: https://opensource.guide/legal/
- Brazilian Software Law: https://www.planalto.gov.br/ccivil_03/leis/l9609.htm

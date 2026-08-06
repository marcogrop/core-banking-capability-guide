# Canonical Banking Capability Model (CBCM)

The Canonical Banking Capability Model (CBCM) is a structured, implementation-independent model for defining, implementing, governing, and evaluating modern banking platforms. It is inspired by Apache Fineract and common banking architecture patterns, but it is not a vendor implementation manual.

This project originated as the Core Banking Capability Reference Guide and is evolving into the Canonical Banking Capability Model (CBCM). Historical source labels may still refer to the original guide where they describe provenance rather than the current model identity.

## What Is Included

- 27 capability chapters with purpose, business importance, conceptual domain models, lifecycles, workflows, relationships, distinctive aspects, commands, events, invariants, and boundary statements.
- A shared architecture and reading guide.
- Extracted domain-model diagrams as named image assets.
- Cross-capability, lifecycle, entity, command, and event indexes.
- A glossary, three-level capability taxonomy, and business-operation specification template.
- Draft vendor-research and CBCM gap-assessment material for evolving the model while preserving vendor neutrality.

## Start Here

1. [CBCM Charter](00-foundations/cbcm-charter.md)
2. [Architecture and Reading Guide](00-foundations/architecture-and-reading-guide.md)
3. [Capability Index](06-reference/capability-index.md)
4. [Capability Collaboration Patterns](06-reference/capability-collaboration-patterns.md)
5. [Three-Level Capability Taxonomy](06-reference/third-level-business-operations.md)
6. [Capability Feature Operation Template](06-reference/capability-feature-operation-template.md)
7. [CBCM Gap Assessment](07-research/cbcm-gap-assessment.md)

## Repository Structure

```text
canonical-banking-capability-model/
|-- README.md
|-- SUMMARY.md
|-- TODO.md
|-- 00-foundations/
|-- 01-business-capabilities/
|-- 02-policy-capabilities/
|-- 03-financial-infrastructure/
|-- 04-information-capabilities/
|-- 05-platform-capabilities/
|-- 06-reference/
|-- 07-research/
`-- assets/images/
```

Research and evolution material is kept in `07-research/`.
Roadmap is published int TODO.md

## Documentation Conventions

Each capability file contains YAML front matter with a stable identifier, capability number, category, architectural layer, primary record, criticality, and historical source where available. Commands request state changes; Business Events describe committed facts. Domain diagrams are conceptual ownership models rather than physical schemas.

## Intended Use

The collection is suitable for custom banking platform definition, capability mapping, bounded-context design, requirements discovery, specification extraction, API and event modeling, implementation planning, architecture governance, vendor evaluation, training, and AI-assisted analysis. It is not legal, regulatory, accounting, or product advice.

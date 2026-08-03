# Core Banking Capability Reference Guide

A structured, implementation-independent reference for understanding the business boundaries and interactions of a modern composable core banking platform. The model is inspired by Apache Fineract and common banking architecture patterns, but it is not a vendor implementation manual.

## What Is Included

- 27 capability chapters with purpose, business importance, conceptual domain models, lifecycles, workflows, relationships, distinctive aspects, commands, events, invariants, and boundary statements.
- A shared architecture and reading guide.
- Extracted domain-model diagrams as named image assets.
- Cross-capability, lifecycle, entity, command, and event indexes.
- A glossary and third-level business-operation specification guidance.
- Draft vendor-research and CBCM gap-assessment material for evolving the model while preserving vendor neutrality.

## Start Here

1. [Architecture and Reading Guide](00-foundations/architecture-and-reading-guide.md)
2. [Capability Index](06-reference/capability-index.md)
3. [Capability Collaboration Patterns](06-reference/capability-collaboration-patterns.md)
4. [Recommended Third-Level Business Operations](06-reference/third-level-business-operations.md)
5. [CBCM Gap Assessment](07-research/cbcm-gap-assessment.md)

## Repository Structure

```text
core-banking-capability-guide/
├── README.md
├── SUMMARY.md
├── 00-foundations/
├── 01-business-capabilities/
├── 02-policy-capabilities/
├── 03-financial-infrastructure/
├── 04-information-capabilities/
├── 05-platform-capabilities/
├── 06-reference/
└── assets/images/
```

Research and evolution material is kept in `07-research/`.

## Documentation Conventions

Each capability file contains YAML front matter with a stable identifier, capability number, category, architectural layer, primary record, and criticality where available. Commands request state changes; Business Events describe committed facts. Domain diagrams are conceptual ownership models rather than physical schemas.

## Intended Use

The collection is suitable for capability mapping, bounded-context design, requirements discovery, specification extraction, API and event modeling, implementation planning, training, and AI-assisted analysis. It is not legal, regulatory, accounting, or product advice.

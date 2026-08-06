# CBCM PoC Roadmap

## Goal

Evolve the Canonical Banking Capability Model (CBCM) from the current reference model into a first proof of concept that can guide custom banking platform definition, implementation planning, architecture governance, and vendor or solution evaluation.

The PoC should prove that CBCM can move from capability descriptions to implementable and testable design artefacts without becoming tied to a specific vendor, module structure, or deployment topology.

## PoC Definition

The first PoC is successful when CBCM can be used to:

- describe the capability shape of a target banking platform,
- decompose selected capabilities into features and business operations,
- derive implementation artefacts from those operations,
- map a retail payment account scenario to CBCM capabilities and operations,
- align RFP or vendor responses to CBCM,
- identify capability gaps and build / buy / partner / BPO decisions,
- support architecture review with clear ownership, events, invariants, and evidence.

## Recommended PoC Scope

The recommended first scenario is a basic retail payment account platform.

This scope is narrow enough to be manageable, but rich enough to exercise important CBCM concepts:

- customer onboarding and customer master,
- product setup,
- account lifecycle,
- payment initiation and execution,
- limits and holds,
- cards integration,
- reconciliation,
- accounting outputs,
- audit and reporting,
- API and event integration.

## Workstreams

### 1. Foundation

- [x] Define CBCM as a model for platform definition, implementation, governance, and evaluation.
- [x] Add CBCM charter.
- [x] Formalize the three-level taxonomy: Capability -> Feature -> Business Operation.
- [x] Add reusable capability-feature-operation template.
- [x] Decide mandatory vs optional operation-spec fields.
- [x] Decide naming conventions for features, operations, commands, and events.
- [x] Decide how to explicitly select a subset of the features and operations for subsequent refinement steps.
- [x] Decide whether read-only governed views belong in operation specs.

### 2. Method Validation

- [x] Create Customer Management operations pilot.
- [x] Review Customer Management operations pilot.
- [x] Polish Customer Management operations pilot.
- [ ] Decide whether operation documents should live beside capability chapters or under a dedicated operations folder.
- [ ] Capture lessons learned from Customer Management.
- [ ] Create a reusable review checklist for future operation documents.

### 3. Capability Decomposition PoC

- [ ] Select capabilities, features, and operations for first-pass PoC decomposition.
- [ ] Finalize Customer Management operation decomposition.
- [ ] Decompose Customer Onboarding / KYC.
- [ ] Decompose Product Catalog.
- [ ] Decompose Savings / Account Management for retail payment accounts.
- [ ] Decompose Payment Processing.
- [ ] Decompose Card Management.
- [ ] Decompose Limits and Exposure Management.
- [ ] Decompose Accounting outputs needed for the retail payment account scenario.
- [ ] Decide whether this capability set is sufficient for the first PoC after scenario mapping.

### 4. Retail Payment Account Scenario

- [ ] Define the canonical retail payment account scenario.
- [ ] Define scenario boundaries and explicit out-of-scope items.
- [ ] Apply refinement selection rules to scenario steps.
- [ ] Map scenario steps to CBCM capabilities.
- [ ] Map scenario steps to features and business operations.
- [ ] Identify required commands.
- [ ] Identify required business events.
- [ ] Identify required evidence and audit traces.
- [ ] Identify key invariants and failure cases.
- [ ] Identify implementation components needed for the scenario.

### 5. RFP and Vendor Evaluation Alignment

- [ ] Convert the current RFP Capability Matrix into a CBCM-aligned matrix.
- [ ] Add CBCM capability, feature, and operation columns.
- [ ] Define controlled values for availability.
- [ ] Define controlled values for delivery model: native, configured, custom, partner, BPO, manual, unsupported.
- [ ] Define evidence requirements by operation.
- [ ] Define sandbox test scenarios by operation.
- [ ] Decide how scoring should roll up by capability area.
- [ ] Decide whether scoring should be capability-based, scenario-based, or both.

### 6. Implementation Artefacts

- [ ] Define operation-to-API mapping format.
- [ ] Define operation-to-event mapping format.
- [ ] Define operation-to-test-case mapping format.
- [ ] Define operation-to-backlog mapping format.
- [ ] Define operation-to-data-ownership mapping format.
- [ ] Define operation-to-audit-evidence mapping format.
- [ ] Create one worked implementation artefact set from the Customer Management pilot.

### 7. Governance and Review

- [ ] Define how CBCM changes are proposed, reviewed, and accepted.
- [ ] Define status levels for draft, reviewed, approved, deprecated, and superseded model elements.
- [ ] Define how source evidence is tracked for capability changes.
- [ ] Define how capability changes affect indexes, RFP mappings, and implementation artefacts.
- [ ] Decide whether model decisions should be tracked in ADR-style records.

### 8. PoC Output Package

- [ ] CBCM charter.
- [ ] Three-level taxonomy.
- [ ] Capability-feature-operation template.
- [ ] Customer Management operation decomposition.
- [ ] Retail payment account scenario map.
- [ ] CBCM-aligned RFP matrix draft.
- [ ] Example implementation artefact set.
- [ ] PoC findings and recommendations.

## Open Decisions

- [ ] Should operation documents live beside capability chapters or under a dedicated `operations/` folder?
- [ ] Should every capability eventually get an operations document, or only selected PoC capabilities first?
- [ ] Should the first PoC focus only on retail payment accounts?
- [ ] Should governed read operations be included selectively, or should operation docs contain only state-changing operations?
- [ ] Should operation specs have one standard depth, or a lightweight and full variant?
- [ ] Should RFP scoring roll up by CBCM capability, scenario, or both?
- [ ] Should CBCM include machine-readable YAML/JSON catalogues in addition to Markdown?
- [ ] Should implementation artefacts remain conceptual, or should the PoC include example OpenAPI/event-schema drafts?

## Parking Lot

- [ ] Full vendor evidence research expansion.
- [ ] Architecture diagrams per scenario.
- [ ] Machine-readable CBCM catalogue.
- [ ] Automated index generation.
- [ ] Automated RFP matrix generation from CBCM operations.
- [ ] Full capability scoring model.
- [ ] Vendor comparison dashboard.
- [ ] Regulatory localization packs.
- [ ] Migration and back-book conversion playbook.

## Review Notes

Use this section to capture review comments before turning them into changes.

- 

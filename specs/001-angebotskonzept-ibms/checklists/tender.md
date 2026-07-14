# Tender Requirements Checklist: Angebotskonzept iBMS 3.0

**Purpose**: Validate whether tender-related requirements are complete, clear, consistent, measurable, and review-ready before implementation and drafting work.
**Created**: 2026-07-01
**Feature**: [spec.md](../spec.md)

**Note**: This checklist validates the quality of written requirements, not system behavior.

## Requirement Completeness

- [ ] CHK001 Are input scope boundaries for source documents explicitly defined (PDF in scope, XLSX excluded) and justified for this iteration? [Completeness, Spec §FR-001, Spec §Assumptions]
- [ ] CHK002 Are mandatory chapter requirements for Angebotskonzept.md fully enumerated, not only listed as topic families? [Completeness, Spec §FR-002, Spec §FR-005, Gap]
- [ ] CHK003 Are requirements defined for how contradictions across tender sources must be resolved and documented? [Completeness, Spec §Edge Cases, Gap]
- [ ] CHK004 Are requirements specified for evidence freshness (for example verification date per source) in addition to source linkage? [Completeness, Constitution §II, Gap]

## Requirement Clarity

- [ ] CHK005 Is "nachvollziehbare Loesungsdarstellung" defined with objective criteria (required structure, minimum evidence density, or quality thresholds)? [Clarity, Spec §FR-004, Ambiguity]
- [ ] CHK006 Is "fachlich konsistent" for section outputs defined with measurable review criteria? [Clarity, Spec §User Story 1 Acceptance Scenario 2, Ambiguity]
- [ ] CHK007 Is "kritische Anforderungen" in SC-002 explicitly classified so reviewers can determine the 90% denominator unambiguously? [Clarity, Spec §SC-002, Ambiguity]
- [ ] CHK008 Is "zentrale Aussagen" in SC-004 precisely bounded so traceability coverage can be assessed consistently? [Clarity, Spec §SC-004, Ambiguity]

## Requirement Consistency

- [ ] CHK009 Do language requirements align across all sections (German-only output versus potential source-language quotations)? [Consistency, Spec §FR-003, Conflict]
- [ ] CHK010 Are traceability obligations consistent between FR-007/FR-008 and the dedicated Evidence and Traceability section without conflicting granularity? [Consistency, Spec §FR-007, Spec §FR-008, Spec §Evidence and Traceability]
- [ ] CHK011 Do compliance constraints in the specification align with constitutional confidentiality and source hierarchy requirements? [Consistency, Spec §Compliance and Confidentiality, Constitution §III, Constitution §Tender Data and Compliance Standards]

## Acceptance Criteria Quality

- [ ] CHK012 Can SC-001 (100% Pflichtkapitelabdeckung) be objectively verified from an explicit, versioned list of mandatory chapters? [Measurability, Spec §SC-001, Gap]
- [ ] CHK013 Are success criteria mapped to corresponding functional requirements so pass/fail decisions are traceable? [Traceability, Spec §Functional Requirements, Spec §Success Criteria, Gap]
- [ ] CHK014 Is the two-workday review target in SC-005 defined with start/end conditions and responsible roles? [Measurability, Spec §SC-005, Ambiguity]

## Scenario Coverage

- [ ] CHK015 Are primary authoring scenarios documented for extraction, structuring, and value-criterion mapping as separate requirement flows? [Coverage, Spec §User Story 1, Spec §User Story 2]
- [ ] CHK016 Are alternate scenarios defined for partial source availability (missing files, unreadable pages, delayed clarifications)? [Coverage, Spec §Edge Cases, Gap]
- [ ] CHK017 Are exception scenarios specified for unverifiable statements, including mandatory assumption workflow and escalation path? [Coverage, Spec §FR-008, Spec §Edge Cases]
- [ ] CHK018 Are recovery scenarios documented for correcting previously wrong assumptions after new tender clarifications appear? [Coverage, Recovery Flow, Gap]

## Edge Case Coverage

- [ ] CHK019 Are requirements defined for handling low OCR quality or non-machine-readable PDF sections, including manual evidence capture rules? [Edge Case, Spec §Edge Cases]
- [ ] CHK020 Are requirements defined for tie-break decisions when two authoritative sources conflict and no clarification is available before deadline? [Edge Case, Spec §Edge Cases, Gap]
- [ ] CHK021 Is fallback behavior specified when evidence cannot be linked at chapter level but only at document level? [Edge Case, Spec §Evidence and Traceability, Gap]

## Non-Functional Requirements

- [ ] CHK022 Are confidentiality requirements operationalized with explicit redaction/classification rules and reviewer responsibilities? [Non-Functional, Spec §Compliance and Confidentiality, Constitution §III]
- [ ] CHK023 Are reproducibility requirements defined for regenerating the same concept output from the same inputs and documented steps? [Non-Functional, Constitution §V, Gap]
- [ ] CHK024 Are quality-gate ownership and pass/fail criteria required for draft approval before downstream offer documents are derived? [Non-Functional, Constitution §IV, Plan §Constitution Check]

## Dependencies and Assumptions

- [ ] CHK025 Are external dependencies (official tender notices, authority clarifications, internal validated data) prioritized with mandatory conflict logging rules? [Dependency, Constitution §Tender Data and Compliance Standards]
- [ ] CHK026 Are assumptions required to include validation trigger, owner, and due date, rather than only a label? [Assumption, Spec §Assumptions, Gap]

## Ambiguities and Conflicts

- [ ] CHK027 Is there a defined requirement-ID and acceptance-ID cross-reference scheme for section-level traceability in review artifacts? [Traceability, Gap]
- [ ] CHK028 Are potentially conflicting goals (speed to first draft versus depth of source validation) explicitly prioritized in requirements? [Conflict, Spec §SC-005, Constitution §II, Ambiguity]

## Notes

- Use this checklist during specification and PR review before drafting or updating Angebotskonzept.md.
- Mark unresolved items with evidence links and required spec updates.

<!--
Sync Impact Report
- Version change: template (unversioned) -> 1.0.0
- Modified principles:
	- Principle slot 1 -> I. Tender Outcome Alignment
	- Principle slot 2 -> II. Traceable and Verifiable Information
	- Principle slot 3 -> III. Compliance and Confidentiality by Design
	- Principle slot 4 -> IV. Quality Gates for Submission Readiness
	- Principle slot 5 -> V. Reproducible Delivery Workflow
- Added sections:
	- Tender Data and Compliance Standards
	- Delivery Workflow and Review Gates
- Removed sections:
	- None
- Templates requiring updates:
	- ✅ updated: .specify/templates/plan-template.md
	- ✅ updated: .specify/templates/spec-template.md
	- ✅ updated: .specify/templates/tasks-template.md
	- ⚠ pending: .specify/templates/commands/*.md (directory not present)
- Follow-up TODOs:
	- None
-->

# ACRSOR-577 Constitution

## Core Principles

### I. Tender Outcome Alignment
Every requirement, decision, and deliverable MUST directly support preparing and
submitting a complete public tender offer. Work that does not improve offer
completeness, compliance, competitiveness, or submission confidence MUST be
deferred. Rationale: strict alignment prevents scope drift and protects deadline
focus.

### II. Traceable and Verifiable Information
All facts used in offer content MUST cite their authoritative source and last
verification date. Derived assumptions MUST be explicitly marked as assumptions.
Any generated narrative, pricing input, or qualification claim MUST be linked to
source evidence so reviewers can audit it quickly. Rationale: traceability is
required for internal approval and external tender defensibility.

### III. Compliance and Confidentiality by Design
The project MUST treat tender instructions, legal constraints, and data handling
rules as non-negotiable. Access controls, redaction rules, and data retention
boundaries MUST be defined before sharing or publishing any tender artifacts.
Potentially sensitive or partner-owned information MUST be classified and
handled according to least-privilege access. Rationale: compliance failures can
invalidate bids and create legal risk.

### IV. Quality Gates for Submission Readiness
No artifact is submission-ready until it passes explicit quality gates: accuracy
review, compliance check, completeness check, and stakeholder approval. Each
gate MUST have a named owner and objective pass/fail criteria. If a gate fails,
the artifact MUST return to revision with a tracked remediation note. Rationale:
formal gates reduce last-minute defects in bid packages.

### V. Reproducible Delivery Workflow
The tender package build process MUST be reproducible from documented inputs,
steps, and tooling versions. Any generated document set MUST include a change
log and a manifest of included files. Team members MUST be able to recreate the
same package content from the same inputs without hidden manual steps.
Rationale: reproducibility improves auditability, handover, and deadline safety.

## Tender Data and Compliance Standards

- Source hierarchy MUST be followed: official tender notice and annexes first,
	then contracting authority clarifications, then internal validated data.
- Contradictions between sources MUST be logged and resolved before proposal
	text is finalized.
- Mandatory submission criteria (format, language, declarations, signatures,
	deadlines, channels) MUST be tracked in a checklist mapped to evidence files.
- Retention and deletion handling for working documents MUST follow the tender
	lifecycle and organizational policy.

## Delivery Workflow and Review Gates

- Every feature spec MUST include compliance constraints, evidence sources, and
	measurable submission-readiness outcomes.
- Every implementation plan MUST define constitution gates and identify owners
	for compliance, legal, and quality reviews.
- Tasks MUST include traceability updates, review checkpoints, and packaging
	validation before final delivery milestones.
- Pull requests and review approvals MUST confirm constitutional compliance,
	including source traceability and confidentiality controls.

## Governance

This constitution overrides conflicting local practices for this repository.
Amendments require a documented proposal, reviewer approval by project owners,
and an explicit impact statement for templates and active work items.

Versioning policy for this constitution follows semantic versioning:
- MAJOR: incompatible governance changes or principle removals/redefinitions.
- MINOR: new principle or materially expanded mandatory guidance.
- PATCH: wording clarifications and non-semantic refinements.

Compliance review expectations:
- At plan time, constitution gates MUST be checked before implementation.
- At review time, each pull request MUST record pass/fail status for applicable
	principles.
- Before submission, a final readiness review MUST confirm all mandatory gates
	are passed and evidence links are current.

**Version**: 1.0.0 | **Ratified**: 2026-07-01 | **Last Amended**: 2026-07-01

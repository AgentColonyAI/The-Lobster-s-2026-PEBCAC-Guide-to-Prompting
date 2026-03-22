---
doc_type: verification_evaluation
doc_id: VERIFY-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: acceptance_validation_testing_and_evidence_rules
source_of_truth_priority: 6
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - MISSION-001
  - GOV-001
  - SPEC-TEST-001
supersedes: []
superseded_by: null
---

# Verification and Evaluation

## Acceptance Gate
- final_status_can_be_complete_only_if:
  - <ACCEPTANCE CONDITION>
  - <ACCEPTANCE CONDITION>
  - <ACCEPTANCE CONDITION>

## Validation Checks
- structural_validation:
  - <CHECK>
  - <CHECK>
- completeness_validation:
  - <CHECK>
  - <CHECK>
- constraint_compliance_validation:
  - <CHECK>
  - <CHECK>

## Evidence Rules
- every_requirement_must_trace_to:
  - <SOURCE RULE>
- every_claim_must_include:
  - <CITATION|TRACE ID|TEST EVIDENCE|NOT APPLICABLE RULE>
- unsupported_claim_behavior: <FAIL|LABEL_AS_UNKNOWN|ESCALATE>

## Testing Requirements
- required_test_types:
  - <TEST TYPE>
  - <TEST TYPE>
- minimum_pass_threshold: <THRESHOLD>
- required_test_artifacts:
  - <ARTIFACT>
  - <ARTIFACT>

## Regression Rules
- rerun_regression_when:
  - <TRIGGER>
  - <TRIGGER>
- regression_baseline_source: <LOCATION OR DOC_ID>

## Failure Handling
- if_validation_fails: <REQUIRED ACTION>
- if_tests_fail: <REQUIRED ACTION>
- if_evidence_is_missing: <REQUIRED ACTION>
- fail_closed_for:
  - <CONDITION>
  - <CONDITION>

## Required Output Report
The final verification report must include:
- scope_checked
- checks_run
- pass_fail_result
- failed_checks
- evidence_references
- unresolved_risks
- recommendation: <COMPLETE|REVISE|ESCALATE>

## Audit Storage Requirements
- store_prompt_version: <YES|NO>
- store_context_version: <YES|NO>
- store_tool_logs: <YES|NO>
- store_test_outputs: <YES|NO>
- store_intermediate_artifacts: <YES|NO>

## Final Instruction to Agent
Do not mark work complete based on plausibility. Mark work complete only after the required checks, tests, and evidence rules pass.

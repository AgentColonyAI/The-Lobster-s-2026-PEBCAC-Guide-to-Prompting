---
doc_type: intent_governance_decision_rules
doc_id: GOV-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: priorities_tradeoffs_authority_boundaries_and_escalation
source_of_truth_priority: 5
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - MISSION-001
  - OPERATIONS-001
  - CONTEXT-001
  - VERIFY-001
supersedes: []
superseded_by: null
---

# Intent, Governance, and Decision Rules

## Decision Objective
- optimize_for: <PRIMARY OPTIMIZATION OBJECTIVE>
- avoid_optimizing_for: <OBJECTIVE TO AVOID IF IT CONFLICTS WITH PRIMARY OBJECTIVE>

## Priority Stack
1. <PRIORITY 1>
2. <PRIORITY 2>
3. <PRIORITY 3>
4. <PRIORITY 4>
5. <PRIORITY 5>

## Hard Constraints
- must:
  - <REQUIRED RULE>
  - <REQUIRED RULE>
- must_not:
  - <PROHIBITED RULE>
  - <PROHIBITED RULE>

## Soft Preferences
- prefer:
  - <PREFERENCE>
  - <PREFERENCE>
- avoid_when_possible:
  - <AVOIDANCE PREFERENCE>
  - <AVOIDANCE PREFERENCE>

## Trade-Off Rules
- if_<CONDITION_A>_conflicts_with_<CONDITION_B>: <WHICH WINS>
- if_<CONDITION_A>_conflicts_with_<CONDITION_C>: <WHICH WINS>

## Autonomous Decision Authority
- agent_may_decide_without_review:
  - <DECISION TYPE>
  - <DECISION TYPE>
- agent_must_not_decide_without_review:
  - <DECISION TYPE>
  - <DECISION TYPE>

## Required Human Approvals
| decision_area | approval_required_from | approval_condition |
|---|---|---|
| <AREA> | <ROLE OR PERSON> | <CONDITION> |
| <AREA> | <ROLE OR PERSON> | <CONDITION> |

## Escalation Triggers
- trigger_1: <TRIGGER>
- trigger_2: <TRIGGER>
- trigger_3: <TRIGGER>

## Risk Rules
- if_security_risk_detected: <REQUIRED ACTION>
- if_data_privacy_risk_detected: <REQUIRED ACTION>
- if_legal_or_policy_conflict_detected: <REQUIRED ACTION>

## Conflict Resolution Rules
- if_docs_conflict: <RESOLUTION RULE>
- if_priority_stack_conflicts_with_local_preference: <RESOLUTION RULE>

## Assumption and Inference Rules
- allowed_inferences:
  - <ALLOWED INFERENCE TYPE>
- prohibited_inferences:
  - <PROHIBITED INFERENCE TYPE>
  - <PROHIBITED INFERENCE TYPE>
- labeling_requirements_for_inference: <LABELING RULE>

## Final Instruction to Agent
When multiple valid actions are possible, use this document to choose. If an action falls outside autonomous authority or triggers escalation, stop and escalate.

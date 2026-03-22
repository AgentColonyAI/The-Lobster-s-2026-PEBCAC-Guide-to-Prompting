---
doc_type: mission_document
doc_id: MISSION-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: mission_and_business_outcome
source_of_truth_priority: 1
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - OPERATIONS-001
  - CONTEXT-001
  - SPEC-PRODUCT-001
supersedes: []
superseded_by: null
---

# Mission Document

## Agent Read Rules
- Treat this document as authoritative for product purpose, target users, top-level outcomes, and non-goals.
- Do not use this document to infer technical architecture unless the architecture document explicitly confirms it.
- If this document conflicts with a lower-priority document, follow this document and report the conflict.
- If this document conflicts with a document of equal or higher priority, stop and escalate.

## Project Identity
- project_name: <PROJECT_NAME>
- product_name: <PRODUCT_NAME>
- project_stage: <DISCOVERY|MVP|V1|V2|ENTERPRISE_EXPANSION>
- delivery_mode: <GREENFIELD|REBUILD|EXTENSION|MIGRATION>

## Core Mission
- one_sentence_mission: <ONE SENTENCE MISSION>
- primary_problem_statement: <PRIMARY USER OR BUSINESS PROBLEM>
- why_this_exists: <WHY THE SYSTEM IS BEING BUILT>

## Target Users
### Primary User Segments
- segment_1: <USER_SEGMENT>
- segment_2: <USER_SEGMENT>

### Secondary User Segments
- segment_1: <USER_SEGMENT>
- segment_2: <USER_SEGMENT>

## User Outcomes
- outcome_1: <USER OUTCOME>
- outcome_2: <USER OUTCOME>
- outcome_3: <USER OUTCOME>

## Business Outcomes
- outcome_1: <BUSINESS OUTCOME>
- outcome_2: <BUSINESS OUTCOME>
- outcome_3: <BUSINESS OUTCOME>

## Success Definition
- primary_success_metric: <METRIC + TARGET>
- secondary_success_metric_1: <METRIC + TARGET>
- secondary_success_metric_2: <METRIC + TARGET>

## Phase Definition
- current_phase: <PHASE NAME>
- in_scope_for_current_phase:
  - <ITEM>
  - <ITEM>
- out_of_scope_for_current_phase:
  - <ITEM>
  - <ITEM>

## Non-Goals
- non_goal_1: <NOT PART OF THIS PROJECT OR PHASE>
- non_goal_2: <NOT PART OF THIS PROJECT OR PHASE>
- non_goal_3: <NOT PART OF THIS PROJECT OR PHASE>

## Priority Order
1. <HIGHEST PRIORITY>
2. <NEXT PRIORITY>
3. <NEXT PRIORITY>
4. <LOWEST PRIORITY OF TOP TIER>

## Critical Assumptions
- assumption_1: <ASSUMPTION>
- assumption_2: <ASSUMPTION>
- assumption_3: <ASSUMPTION>

## Known Unknowns
- unknown_1: <UNKNOWN THAT MAY AFFECT EXECUTION>
- unknown_2: <UNKNOWN THAT MAY AFFECT EXECUTION>

## Escalation Triggers
- trigger_1: <WHEN AGENT MUST STOP AND REQUEST HUMAN INPUT>
- trigger_2: <WHEN AGENT MUST STOP AND REQUEST HUMAN INPUT>

## Final Instruction to Agent
Execute only work that advances the mission, current phase scope, and success definition above. Reject or escalate work that contradicts mission, phase scope, or stated non-goals.

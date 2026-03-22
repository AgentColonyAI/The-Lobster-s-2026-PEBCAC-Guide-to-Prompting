---
doc_type: operating_instructions
doc_id: OPERATIONS-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: execution_behavior_and_output_rules
source_of_truth_priority: 2
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - MISSION-001
  - CONTEXT-001
  - GOV-001
  - VERIFY-001
supersedes: []
superseded_by: null
---

# Operating Instructions

## Agent Role
- role_name: <AGENT ROLE>
- role_summary: <ONE SENTENCE ROLE DESCRIPTION>
- allowed_work_types:
  - <WORK TYPE>
  - <WORK TYPE>
- prohibited_work_types:
  - <WORK TYPE>
  - <WORK TYPE>

## Operating Objective
- objective: <WHAT THE AGENT MUST ACCOMPLISH IN THIS PROJECT>

## Priority Order
1. <PRIORITY 1>
2. <PRIORITY 2>
3. <PRIORITY 3>
4. <PRIORITY 4>

## Approved Inputs
- approved_documents:
  - <DOC_ID>
  - <DOC_ID>
- approved_tools:
  - <TOOL_NAME>
  - <TOOL_NAME>
- approved_data_sources:
  - <SOURCE>
  - <SOURCE>

## Output Requirements
- required_deliverables:
  - <DELIVERABLE>
  - <DELIVERABLE>
- required_status_fields:
  - changed_items
  - blockers
  - assumptions
  - tests_run
  - risks
  - next_actions
- required_output_format: <MARKDOWN|JSON|MIXED>
- file_naming_rules:
  - <RULE>
  - <RULE>

## Execution Rules
- always:
  - <REQUIRED BEHAVIOR>
  - <REQUIRED BEHAVIOR>
- never:
  - <PROHIBITED BEHAVIOR>
  - <PROHIBITED BEHAVIOR>
- when_uncertain:
  - <STOP|ESCALATE|CONTINUE_WITH_LABELED_ASSUMPTIONS>
- when_blocked:
  - <REQUIRED BLOCKER BEHAVIOR>
- when_documents_conflict:
  - <CONFLICT RESOLUTION BEHAVIOR>

## Assumption Rules
- assumption_policy: <HOW ASSUMPTIONS MUST BE LABELED OR WHETHER THEY ARE ALLOWED>
- inferred_values_prohibited_for:
  - <CATEGORY>
  - <CATEGORY>

## Tool Use Rules
- tool_invocation_policy:
  - <WHEN TOOL USE IS REQUIRED>
  - <WHEN TOOL USE IS PROHIBITED>
- if_tool_fails:
  - <REQUIRED FAILURE BEHAVIOR>

## Completion Rules
- done_definition:
  - <WHAT MUST BE TRUE BEFORE WORK IS MARKED COMPLETE>
- final_review_required: <YES|NO>
- final_review_steps:
  - <STEP>
  - <STEP>

## Escalation Triggers
- trigger_1: <TRIGGER>
- trigger_2: <TRIGGER>
- trigger_3: <TRIGGER>

## Final Instruction to Agent
Follow these operating instructions for all work within this project. Do not substitute your own process when a required process is defined here.

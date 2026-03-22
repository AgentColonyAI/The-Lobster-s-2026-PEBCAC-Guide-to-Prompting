---
doc_type: execution_handoff_audit
doc_id: EXEC-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: active
authoritative_scope: current_state_progress_decisions_handoff_and_audit
source_of_truth_priority: 7
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - MISSION-001
  - OPERATIONS-001
  - GOV-001
  - VERIFY-001
supersedes: []
superseded_by: null
---

# Execution, Handoff, and Audit

## Current Execution State
- current_phase: <PHASE>
- current_milestone: <MILESTONE>
- current_status: <NOT_STARTED|IN_PROGRESS|BLOCKED|READY_FOR_REVIEW|COMPLETE>
- active_workstream: <WORKSTREAM>

## Work Completed
| task_id | task_name | completion_date | evidence_reference | validation_status | notes |
|---|---|---|---|---|---|
| <TASK_ID> | <TASK NAME> | <YYYY-MM-DD> | <REF> | <PASS|FAIL|PARTIAL> | <NOTES> |

## Work In Progress
| task_id | task_name | current_state | blocker | next_action |
|---|---|---|---|---|
| <TASK_ID> | <TASK NAME> | <STATE> | <BLOCKER OR NONE> | <NEXT ACTION> |

## Blockers
| blocker_id | blocker_description | impact | required_resolution | owner |
|---|---|---|---|---|
| <BLOCKER_ID> | <DESCRIPTION> | <IMPACT> | <RESOLUTION> | <OWNER> |

## Decision Log
| decision_id | decision | reason | source_reference | approved_by | date |
|---|---|---|---|---|---|
| <DECISION_ID> | <DECISION> | <REASON> | <DOC_ID OR REF> | <APPROVER> | <YYYY-MM-DD> |

## Change Log
| change_id | change_summary | affected_components | reason | date |
|---|---|---|---|---|
| <CHANGE_ID> | <SUMMARY> | <COMPONENTS> | <REASON> | <YYYY-MM-DD> |

## Handoff Instructions
- resume_from_task_id: <TASK_ID>
- must_read_before_resuming:
  - <DOC_ID>
  - <DOC_ID>
- do_not_repeat:
  - <WORK ALREADY COMPLETED>
- immediate_next_actions:
  - <ACTION>
  - <ACTION>

## Final Delivery Status
- delivery_readiness: <NOT_READY|READY_FOR_REVIEW|READY_FOR_DEPLOYMENT>
- known_limitations:
  - <LIMITATION>
  - <LIMITATION>
- unresolved_risks:
  - <RISK>
  - <RISK>

## Audit References
- output_artifacts_location: <PATH OR URI>
- test_artifacts_location: <PATH OR URI>
- logs_location: <PATH OR URI>
- evidence_index_location: <PATH OR URI>

## Final Instruction to Agent
Update this document whenever state changes. Use it to preserve continuity across sessions and to hand off work without reconstruction.

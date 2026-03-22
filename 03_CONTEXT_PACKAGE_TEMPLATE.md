---
doc_type: context_package
doc_id: CONTEXT-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: active_context_and_source_authority
source_of_truth_priority: 3
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - MISSION-001
  - OPERATIONS-001
  - GOV-001
supersedes: []
superseded_by: null
---

# Context Package

## Agent Read Rules
- Use only the documents, datasets, and tools listed in this package unless a higher-priority document explicitly authorizes additional context.
- Treat documents listed under superseded, archived, or non-authoritative as reference only and not as execution authority.
- If two active documents conflict, resolve using the authority order below or escalate if unresolved.

## Source Authority Order
1. <DOC_ID OR DOC TYPE>
2. <DOC_ID OR DOC TYPE>
3. <DOC_ID OR DOC TYPE>
4. <DOC_ID OR DOC TYPE>

## Active Authoritative Documents
| doc_id | document_name | version | authority_scope | location | notes |
|---|---|---:|---|---|---|
| <DOC_ID> | <NAME> | <VERSION> | <SCOPE> | <PATH OR URI> | <NOTES> |
| <DOC_ID> | <NAME> | <VERSION> | <SCOPE> | <PATH OR URI> | <NOTES> |

## Active Datasets
| dataset_id | dataset_name | purpose | authority_level | location | freshness_requirement |
|---|---|---|---|---|---|
| <DATASET_ID> | <NAME> | <PURPOSE> | <LEVEL> | <PATH OR URI> | <RULE> |

## Approved Tools
| tool_name | purpose | required_inputs | expected_outputs | when_to_use | when_not_to_use | failure_behavior |
|---|---|---|---|---|---|---|
| <TOOL_NAME> | <PURPOSE> | <INPUTS> | <OUTPUTS> | <WHEN> | <WHEN NOT> | <FAILURE RULE> |

## Stable Project Facts
- fact_1: <STABLE FACT>
- fact_2: <STABLE FACT>
- fact_3: <STABLE FACT>

## Open Questions
- question_1: <OPEN QUESTION>
- question_2: <OPEN QUESTION>

## Superseded or Non-Authoritative Documents
| doc_id | document_name | status | reason_non_authoritative | allowed_use |
|---|---|---|---|---|
| <DOC_ID> | <NAME> | <ARCHIVED|SUPERSEDED|DRAFT> | <REASON> | <REFERENCE ONLY|DO NOT USE> |

## Context Exclusions
- excluded_context_1: <CONTEXT TO IGNORE>
- excluded_context_2: <CONTEXT TO IGNORE>

## Memory Policy
- store_as_persistent_memory_only_if:
  - <RULE>
  - <RULE>
- do_not_store_as_persistent_memory:
  - <RULE>
  - <RULE>

## Escalation Triggers
- trigger_1: <TRIGGER>
- trigger_2: <TRIGGER>

## Final Instruction to Agent
Use this context package as the authority map for what to read, trust, ignore, and escalate.

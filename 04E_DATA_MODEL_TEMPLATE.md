---
doc_type: data_model_spec
doc_id: SPEC-DATA-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: entities_fields_relationships_constraints_and_data_lifecycle
source_of_truth_priority: 4
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - SPEC-PRODUCT-001
  - SPEC-ARCH-001
  - SPEC-API-001
  - SPEC-SEC-001
supersedes: []
superseded_by: null
---

# Data Model Specification

## Data Model Scope
- canonical_store_types:
  - <STORE TYPE>
- canonical_identifiers:
  - <ID TYPE>

## Entities
| entity_id | entity_name | purpose | primary_key | owner |
|---|---|---|---|---|
| ENT-001 | <NAME> | <PURPOSE> | <KEY> | <OWNER> |
| ENT-002 | <NAME> | <PURPOSE> | <KEY> | <OWNER> |

## Fields by Entity
### <ENTITY_NAME>
| field_name | type | required | default | validation_rules | pii_classification |
|---|---|---|---|---|---|
| <FIELD> | <TYPE> | <YES|NO> | <DEFAULT> | <RULES> | <NONE|LOW|MEDIUM|HIGH> |

## Relationships
| from_entity | relation | to_entity | cardinality | delete_behavior |
|---|---|---|---|---|
| <ENTITY> | <RELATION> | <ENTITY> | <1:1|1:N|N:N> | <RULE> |

## Constraints
- uniqueness_constraints:
  - <CONSTRAINT>
- foreign_key_constraints:
  - <CONSTRAINT>
- business_constraints:
  - <CONSTRAINT>

## Data Lifecycle
- creation_rules: <RULE>
- update_rules: <RULE>
- retention_rules: <RULE>
- archival_rules: <RULE>
- deletion_rules: <RULE>

## Migration Rules
- agent_may_create_new_migrations: <YES|NO|WITH_APPROVAL_ONLY>
- breaking_schema_change_policy: <RULE>

## Escalation Triggers
- trigger_1: <TRIGGER>
- trigger_2: <TRIGGER>

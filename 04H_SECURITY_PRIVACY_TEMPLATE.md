---
doc_type: security_privacy_spec
doc_id: SPEC-SEC-001
project_id: <PROJECT_ID>
project_name: <PROJECT_NAME>
version: 0.1
status: draft
authoritative_scope: security_controls_privacy_requirements_auth_access_and_sensitive_data_handling
source_of_truth_priority: 4
owner: <OWNER_NAME_OR_ROLE>
last_updated: <YYYY-MM-DD>
related_docs:
  - SPEC-STACK-001
  - SPEC-ARCH-001
  - SPEC-DATA-001
  - SPEC-API-001
supersedes: []
superseded_by: null
---

# Security and Privacy Specification

## Security Objectives
- objective_1: <OBJECTIVE>
- objective_2: <OBJECTIVE>

## Authentication and Authorization
- auth_model: <MODEL>
- required_roles:
  - <ROLE>
- permission_model: <MODEL>
- session_rules: <RULE>

## Sensitive Data Rules
- pii_categories_present:
  - <CATEGORY>
- prohibited_storage:
  - <DATA TYPE>
- encryption_at_rest_rule: <RULE>
- encryption_in_transit_rule: <RULE>
- secrets_handling_rule: <RULE>

## Application Security Controls
- input_validation_rule: <RULE>
- output_encoding_rule: <RULE>
- rate_limiting_rule: <RULE>
- audit_logging_rule: <RULE>
- dependency_vulnerability_rule: <RULE>

## Privacy Requirements
- data_minimization_rule: <RULE>
- retention_rule: <RULE>
- deletion_request_rule: <RULE>
- consent_or_notice_rule: <RULE>

## Incident and Risk Handling
- if_secret_exposure_detected: <REQUIRED ACTION>
- if_data_leak_risk_detected: <REQUIRED ACTION>
- if_security_requirement_conflicts_with_other_requirement: <RESOLUTION RULE>

## Prohibited Agent Actions
- prohibited_action_1: <ACTION>
- prohibited_action_2: <ACTION>

## Escalation Triggers
- trigger_1: <TRIGGER>
- trigger_2: <TRIGGER>
- trigger_3: <TRIGGER>

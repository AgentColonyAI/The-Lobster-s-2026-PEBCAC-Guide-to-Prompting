# The Lobster’s 2026 PEBCAC Guide to Agent-Ready Development Documents

This guide is written for humans.

Its purpose is to teach a human operator, founder, product lead, architect, or manager how to create a document package that autonomous agents can reliably use to design, build, test, and refine sophisticated applications.

The guide is not the template set itself. The guide explains **what each document category is, why it exists, what belongs inside it, best practices for writing it, and what good agent-ready documentation looks like**.

The markdown templates included with this package are written for **agent understanding**, not for human comfort. They are structured to minimize ambiguity, define authority clearly, encode escalation rules, and make execution auditable.

---

## Table of Contents

1. [What This Package Is](#what-this-package-is)
2. [Why Agent-Ready Documents Are Now Required](#why-agent-ready-documents-are-now-required)
3. [How to Use This Package](#how-to-use-this-package)
4. [What Makes a Document Agent-Ready](#what-makes-a-document-agent-ready)
5. [The Seven Document Categories](#the-seven-document-categories)
   - [1. Mission Documents](#1-mission-documents)
   - [2. Operating Instructions](#2-operating-instructions)
   - [3. Context Package](#3-context-package)
   - [4. Specification Documents](#4-specification-documents)
   - [5. Intent, Governance, and Decision Rules](#5-intent-governance-and-decision-rules)
   - [6. Verification and Evaluation Documents](#6-verification-and-evaluation-documents)
   - [7. Execution, Handoff, and Audit Package](#7-execution-handoff-and-audit-package)
6. [Recommended Writing Order](#recommended-writing-order)
7. [Failure Patterns](#failure-patterns)
8. [Included Template Files](#included-template-files)

---

## What This Package Is

This package contains two things:

1. **A human guide**  
   This document explains how to think about agent-ready development documents and how to write them properly.

2. **A set of agent-facing markdown templates**  
   These are the working templates a human fills in so an agent can read them and execute reliably.

The seven categories are:

1. Mission Documents  
2. Operating Instructions  
3. Context Package  
4. Specification Documents  
5. Intent, Governance, and Decision Rules  
6. Verification and Evaluation Documents  
7. Execution, Handoff, and Audit Package  

Six of those categories use **one template file each**.  
The Specification category uses **multiple template files**, because serious application development requires more than one build document.

---

## Why Agent-Ready Documents Are Now Required

The old workflow assumed a human stayed in the loop constantly.

A person gave the model a request, watched the output in real time, corrected drift immediately, supplied missing background, clarified priorities, and judged quality manually. That workflow can still work for short tasks, but it breaks down the moment an agent is expected to operate for extended periods, interact with tools, write code across multiple files, or continue work across sessions.

Long-running agents expose every hidden weakness in documentation.

If the product goal is vague, the agent will solve the wrong problem.  
If the rules are incomplete, the agent will invent them.  
If source authority is unclear, the agent will mix drafts, guesses, and stale material.  
If “done” is not defined, the agent will stop early or continue badly.  
If escalation rules are missing, the agent will make decisions it was never authorized to make.

This is why agent-ready documents are now required.

You are no longer writing “supporting notes” for a human team member who can fill in the blanks.  
You are writing the operating environment for a system that executes literally against the document set you give it.

That means your documentation must do five things:

- define the objective precisely
- define the rules clearly
- define authority and sources explicitly
- define verification mechanically
- define continuity across time and sessions

When those are missing, people often call the result “hallucination,” “alignment failure,” or “agent drift.” In practice, many of those failures are documentation failures.

Poor agent performance is often a document design problem before it is a model problem.

---

## How to Use This Package

Use the guide first.  
Use the templates second.

Recommended workflow:

1. Read this guide end to end.
2. Decide what application or system the agent is being asked to build.
3. Fill in the templates in the recommended writing order.
4. Review the completed documents for conflicts, ambiguity, and missing approvals.
5. Hand the completed set to the agent as the authoritative execution package.
6. Update the package as decisions change. Do not let stale versions remain active.

Important distinction:

- The **guide** is written for humans.
- The **templates** are written for agents.

The templates are intentionally structured, repetitive, and explicit. That is not a flaw. That is what makes them operational.

---

## What Makes a Document Agent-Ready

A document is agent-ready when an autonomous system can read it and use it without relying on missing social context, implied preferences, or informal human back-and-forth.

An agent-ready document has these properties:

### 1. Clear authority
The document states what it controls and what it does not control.

### 2. Explicit scope
It defines what is in scope, out of scope, and not yet decided.

### 3. Unambiguous language
It avoids loose language such as “make it better,” “keep it clean,” “modern,” “robust,” or “optimize” without definitions.

### 4. Conflict handling
It tells the agent what to do if documents disagree.

### 5. Escalation triggers
It tells the agent when to stop and ask for human review.

### 6. Testable completion
It defines what “done” means in a way that can be checked.

### 7. Traceability
It makes it possible to trace outputs, decisions, and claims back to a source or rule.

### 8. Session continuity
It allows another agent or the same agent in a later run to resume without guessing.

A useful mental model:

**Human-readable** documents aim for convenience.  
**Agent-ready** documents aim for execution reliability.

---

## The Seven Document Categories

## 1. Mission Documents

### What this category is
Mission documents define what the agent is building and why.

This is the top strategic layer. It tells the agent what problem matters, who the target user is, what outcome counts as success, and what is explicitly not part of the assignment.

### Why it matters
If this category is weak, the agent may build an impressive system that solves the wrong problem.

### What this category needs
The mission document should define:

- product or system name
- one-sentence mission
- target users
- user problem
- business problem
- primary success outcomes
- top priorities
- phase boundaries
- non-goals
- major assumptions

### Best practices
- Keep the mission crisp and explicit.
- Separate goals from non-goals.
- State phase boundaries clearly.
- Write success in observable terms.
- Avoid vague product language such as “best-in-class” unless it is measured.

### Example
Weak:
> Build an AI tool for research.

Stronger:
> Build a browser-based AI research workspace for analysts who need citation-backed summaries from approved internal and external sources. Phase 1 focuses on source ingestion, retrieval, and report generation. Phase 1 excludes collaboration, billing, and voice interaction.

### Template in this category
- `01_MISSION_DOCUMENT_TEMPLATE.md`

---

## 2. Operating Instructions

### What this category is
Operating instructions tell the agent how to behave while carrying out the work.

This is the reusable execution layer. It defines role, process expectations, output rules, stop rules, escalation behavior, and prohibited behaviors.

### Why it matters
Without operating instructions, the agent improvises process. Improvised process creates drift.

### What this category needs
The operating document should define:

- agent role
- execution objective
- priority order
- approved inputs
- required deliverables
- process rules
- behavior when blocked
- behavior when uncertain
- prohibited actions
- final review steps

### Best practices
- Use hard rules for must and must-not behavior.
- Define stop conditions.
- Require explicit reporting of blockers and assumptions.
- Separate style preferences from hard constraints.
- Do not leave uncertainty handling implicit.

### Example
Weak:
> Build the feature and keep me posted.

Stronger:
> Build only against approved specification documents. Do not invent endpoints, data fields, vendors, or credentials. If a required dependency is missing, stop and report it in the blockers section. Final output must include changed files, tests run, pass/fail status, unresolved risks, and next actions.

### Template in this category
- `02_OPERATING_INSTRUCTIONS_TEMPLATE.md`

---

## 3. Context Package

### What this category is
The context package defines what information the agent sees and trusts.

This includes the source-of-truth map, background documents, architecture context, dependencies, memory, and tool contracts.

### Why it matters
Agents do not benefit from random information dumps. Precision degrades when signal is buried in noise.

### What this category needs
The context document should define:

- active source documents
- authority ranking
- superseded documents
- relevant background
- technical environment context
- tool contracts
- known open questions
- stable memory items

### Best practices
- Separate active docs from archive docs.
- Explicitly mark superseded documents.
- Define source precedence.
- Keep only high-signal context in the active package.
- Use consistent document identifiers.

### Example
Weak:
> Here are all our notes and old drafts.

Stronger:
> The active context set for this build consists of the current mission document, approved architecture spec, current API contract, security rules, and milestone log. All drafts dated before the approved version list are non-authoritative unless referenced explicitly by a current document.

### Template in this category
- `03_CONTEXT_PACKAGE_TEMPLATE.md`

---

## 4. Specification Documents

### What this category is
This category contains the build documents.

Unlike the other categories, serious application development cannot be handled with one generic specification file. The agent needs a multi-document build package that covers the major technical and product surfaces of the application.

This is the category where the system becomes buildable.

### Why it matters
A single vague “spec” is not enough for a sophisticated application. The agent needs separate documents for architecture, stack, data, APIs, workflows, UI rules, security, testing, and deployment if you want reliable output across a real build.

### What this category needs
At minimum, the specification set should cover:

- product or system requirements
- technology stack
- architecture
- build logic and workflows
- data model
- API contracts
- UI and UX rules
- security and privacy rules
- testing and quality requirements
- deployment and operations

### Best practices
- Keep each spec focused on one domain of authority.
- Cross-reference documents by identifier.
- Never let two docs silently own the same rule.
- Put source precedence at the top of each file.
- Define acceptance criteria inside or alongside specs.
- Use exact field names, routes, states, and interfaces where possible.

### Example
Weak:
> Build a secure full-stack SaaS platform.

Stronger:
> Use separate documents for architecture, data model, API, auth flow, UI states, testing rules, and deployment requirements. Each document should define what it controls, what it depends on, and what the agent must do if requirements conflict.

### Templates in this category
- `04A_PRODUCT_SYSTEM_SPEC_TEMPLATE.md`
- `04B_TECH_STACK_TEMPLATE.md`
- `04C_SYSTEM_ARCHITECTURE_TEMPLATE.md`
- `04D_BUILD_LOGIC_AND_WORKFLOWS_TEMPLATE.md`
- `04E_DATA_MODEL_TEMPLATE.md`
- `04F_API_CONTRACT_TEMPLATE.md`
- `04G_UI_UX_SPEC_TEMPLATE.md`
- `04H_SECURITY_PRIVACY_TEMPLATE.md`
- `04I_TESTING_QA_TEMPLATE.md`
- `04J_DEPLOYMENT_OPERATIONS_TEMPLATE.md`

---

## 5. Intent, Governance, and Decision Rules

### What this category is
This category defines how the agent should make decisions when multiple valid actions exist.

It encodes priorities, trade-offs, escalation thresholds, decision boundaries, and approval requirements.

### Why it matters
Even with perfect context and good specs, the agent still has to choose. If you do not specify what it should optimize for, it will create its own implicit priority stack.

### What this category needs
This document should define:

- ordered priority stack
- trade-off rules
- hard constraints
- soft preferences
- escalation triggers
- authority boundaries
- required approvals
- prohibited autonomous decisions

### Best practices
- Order priorities explicitly.
- Split hard constraints from preferences.
- Define what the agent may do autonomously.
- Define what requires review.
- Write escalation triggers as observable conditions.

### Example
Weak:
> Use your best judgment.

Stronger:
> Prioritize security, correctness, and traceability above implementation speed. Do not introduce new vendors, change authentication architecture, or modify production data models without human approval. If source documents conflict, stop and report the conflict using the escalation format.

### Template in this category
- `05_INTENT_GOVERNANCE_DECISION_RULES_TEMPLATE.md`

---

## 6. Verification and Evaluation Documents

### What this category is
This category defines how the system proves that work is correct.

It covers validation, testing, acceptance checks, evidence rules, regression expectations, and output auditability.

### Why it matters
Without verification, the team is relying on plausibility. Plausibility is not a deployment standard.

### What this category needs
The verification document should define:

- acceptance gates
- validation checks
- test plan expectations
- evidence rules
- citation or traceability requirements
- regression rules
- failure handling rules
- pass/fail thresholds

### Best practices
- Define mechanical checks where possible.
- Require explicit pass/fail outcomes.
- Distinguish final acceptance from draft completion.
- Store test evidence.
- Fail closed when key checks fail.

### Example
Weak:
> Review output for quality.

Stronger:
> Final status may be marked COMPLETE only if required sections are present, acceptance criteria pass, tests listed in the testing spec pass, and all requirement references are traceable to approved source documents.

### Template in this category
- `06_VERIFICATION_EVALUATION_TEMPLATE.md`

---

## 7. Execution, Handoff, and Audit Package

### What this category is
This category preserves continuity across time, runs, and agents.

It records progress, decisions, blockers, state, handoff conditions, and delivery status.

### Why it matters
Without execution and handoff records, every new session begins with reconstruction rather than progress.

### What this category needs
The execution document should define or record:

- current phase
- current status
- tasks completed
- tasks in progress
- blockers
- decisions made
- next actions
- handoff instructions
- final delivery summary
- audit references

### Best practices
- Log decisions with reasons.
- Record blockers explicitly.
- Capture next-step state for the next run.
- Use stable IDs for tasks and decisions.
- Keep the log current; stale execution logs are worse than no logs.

### Example
Weak:
> Worked on auth. More later.

Stronger:
> Completed login route wiring and password reset UI. GitHub OAuth remains blocked pending credentials. Auth acceptance tests passed for email login and logout only. Next agent should resume at AUTH-07 after reviewing the current API contract and security spec.

### Template in this category
- `07_EXECUTION_HANDOFF_AUDIT_TEMPLATE.md`

---

## Recommended Writing Order

Write the documents in this order:

1. Mission Documents  
2. Operating Instructions  
3. Context Package  
4. Specification Documents  
5. Intent, Governance, and Decision Rules  
6. Verification and Evaluation Documents  
7. Execution, Handoff, and Audit Package  

Why this order works:

- Mission defines what matters.
- Operating instructions define behavior.
- Context defines what the agent can rely on.
- Specifications make the build concrete.
- Governance controls agent choice.
- Verification defines what counts as correct.
- Execution and handoff preserve continuity.

---

## Failure Patterns

Use this diagnosis model when agent output is poor:

### Failure 1: Wrong product or wrong feature
Usually a mission problem.

### Failure 2: Strange process behavior or sloppy deliverables
Usually an operating instructions problem.

### Failure 3: Ignored facts that were “somewhere in the docs”
Usually a context packaging problem.

### Failure 4: Output stops at 70–80% useful
Usually a specification problem.

### Failure 5: Agent makes unauthorized trade-offs
Usually a governance problem.

### Failure 6: Output looks good but cannot be trusted
Usually a verification problem.

### Failure 7: Progress disappears between runs
Usually an execution and handoff problem.

A simple rule:

If the agent failed, inspect the document system before assuming the model is the problem.

---

## Included Template Files

### Human guide
- `00_THE_LOBSTERS_2026_PEBCAC_GUIDE_TO_AGENT_READY_DEVELOPMENT_DOCUMENTS.md`

### Single-template categories
- `01_MISSION_DOCUMENT_TEMPLATE.md`
- `02_OPERATING_INSTRUCTIONS_TEMPLATE.md`
- `03_CONTEXT_PACKAGE_TEMPLATE.md`
- `05_INTENT_GOVERNANCE_DECISION_RULES_TEMPLATE.md`
- `06_VERIFICATION_EVALUATION_TEMPLATE.md`
- `07_EXECUTION_HANDOFF_AUDIT_TEMPLATE.md`

### Multi-template specification category
- `04A_PRODUCT_SYSTEM_SPEC_TEMPLATE.md`
- `04B_TECH_STACK_TEMPLATE.md`
- `04C_SYSTEM_ARCHITECTURE_TEMPLATE.md`
- `04D_BUILD_LOGIC_AND_WORKFLOWS_TEMPLATE.md`
- `04E_DATA_MODEL_TEMPLATE.md`
- `04F_API_CONTRACT_TEMPLATE.md`
- `04G_UI_UX_SPEC_TEMPLATE.md`
- `04H_SECURITY_PRIVACY_TEMPLATE.md`
- `04I_TESTING_QA_TEMPLATE.md`
- `04J_DEPLOYMENT_OPERATIONS_TEMPLATE.md`

---

Use the guide to teach the human.  
Use the templates to instruct the agent.

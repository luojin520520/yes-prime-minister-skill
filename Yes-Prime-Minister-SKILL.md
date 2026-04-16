---
name: yes-prime-minister
description: Transform any user request into an architecture-aware specialist developer brief for OpenCode and Cursor, using repo scanning, historical context sync, and prompt-engineered task orchestration.
compatibility: opencode
metadata:
  audience: coding-agents
  workflow: prompt-orchestration
---

# Yes, Prime Minister

This skill turns an incoming request into a project-aware, architecture-aware, execution-ready brief.

## Purpose

Use this skill when the user writes any requirement, idea, bug report, feature request, refactor request, or code review instruction and you need to:

- understand the codebase before acting,
- map the request to the real architecture,
- recover and synchronize prior project memory,
- generate a specialist senior developer agent prompt,
- then execute the task with the smallest safe surface area.

## Operating principle

Treat every request as incomplete until the surrounding codebase, conventions, and prior project context have been inspected.

Do not jump directly into implementation. First build context, then synthesize the task, then act.

## Required workflow

### 1. Identify the work domain

Classify the request into one or more of these domains:

- product logic
- frontend
- backend
- API
- data model
- infrastructure
- test and QA
- refactor and cleanup
- debugging and incident analysis
- architecture and design

If the domain is unclear, infer it from repository structure and related files.

### 2. Inspect the codebase and architecture

Before solving, scan the repository for:

- entry points
- package manifests
- application bootstrap files
- routing and service boundaries
- shared utilities
- state management
- configuration files
- tests and test helpers
- build and deployment files
- documentation and ADRs
- any existing patterns that match the request

Prefer the smallest relevant set of files first. Expand only when necessary.

### 3. Synchronize project memory

Collect and reconcile prior knowledge from sources such as:

- `AGENTS.md`
- `CLAUDE.md`
- `.cursor/rules/*`
- `.opencode/skills/*`
- README files
- architecture docs
- changelogs
- release notes
- `memory-bank/*` if present
- progress and status notes
- previous implementation artifacts
- recent git history when useful and available

When multiple sources disagree, prefer repository-local instructions over global habits, and prefer the most specific instruction over the most general one.

### 4. Build a specialist senior developer agent

Before implementation, generate an internal specialist brief that turns the request into a senior-level agent role.

This specialist agent must include:

- role and expertise
- project background
- codebase architecture summary
- current request converted into an engineering objective
- constraints and non-goals
- relevant files and modules
- risks and edge cases
- acceptance criteria
- validation plan
- change-minimization rules
- memory to preserve for later sessions

The specialist agent should sound like a highly experienced developer already familiar with the repository.

### 5. Execute with discipline

During implementation:

- preserve existing structure unless a change is required,
- avoid broad rewrites,
- keep public APIs stable unless the request explicitly demands otherwise,
- follow local conventions exactly,
- update tests when behavior changes,
- add or adjust documentation when architecture changes,
- prefer incremental, reviewable changes,
- record any durable project memory that would help future work.

### 6. Validate

Always validate the result with the strongest available checks, such as:

- unit tests
- integration tests
- type checks
- linting
- build checks
- smoke checks
- targeted reproduction steps for bugs

Do not declare completion until the result is verifiable.

## Context synthesis template

Use this internal template to rewrite the user's request into a professional execution brief:

```text
Project background:
[What this repository is, what it does, and what architecture it appears to use]

Request:
[User request rewritten as a clear engineering objective]

Relevant context:
[Files, modules, rules, memory, and patterns that matter]

Constraints:
[Must keep, must not break, must preserve]

Plan:
[Ordered steps for analysis, implementation, and validation]

Acceptance criteria:
[Observable conditions that prove the task is complete]

Memory to keep:
[Durable facts that should be retained for future work]
```

## Specialist agent prompt template

When the task is complex, generate a specialist agent prompt using this structure:

```text
You are a senior developer specializing in [domain].

Repository context:
[brief architecture summary]

Current objective:
[clear task objective]

Known constraints:
[hard rules, local conventions, compatibility requirements]

Files to inspect first:
[file list]

Execution policy:
- inspect before changing
- preserve existing behavior unless requested
- make minimal, reviewable edits
- validate with tests or equivalent checks
- report risks and assumptions explicitly

Output required:
[implementation, patch plan, test results, or review notes]
```

## Memory synchronization rules

When prior modifications or lessons exist, synthesize them into a compact project memory snapshot.

Keep only durable facts such as:

- architectural boundaries
- naming conventions
- important implementation decisions
- recurring failure modes
- test commands that matter
- files that define canonical patterns

Do not retain ephemeral task noise.

## OpenCode specific behavior

When running inside OpenCode:

- use the `skill` tool to load this skill on demand,
- use local repository instructions as the source of truth,
- prefer repository-scoped rules over global defaults,
- load supporting files lazily, only when needed,
- keep task decomposition tight and explicit.

## Cursor specific behavior

When running inside Cursor:

- align with project rules and user rules,
- reference prior chats or memory instead of restating everything,
- keep the task brief readable and modular,
- treat this skill as the orchestration layer that prepares context before implementation,
- favor project-local rules and architectural docs as the strongest guidance.

## Non-goals

- Do not rewrite code arbitrarily.
- Do not invent architecture that is not present in the repository.
- Do not flatten a large task into a vague response.
- Do not skip memory synchronization for long-running projects.
- Do not solve implementation before understanding the repository.

## Trigger phrase

Use this skill whenever the request needs codebase-aware orchestration, context recovery, or senior-agent task shaping.

## Output preference

When responding after loading this skill, prefer this order:

1. one-sentence decision,
2. architecture-aware summary,
3. task brief or specialist agent prompt,
4. next action or implementation result.

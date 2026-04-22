# AI Development Guidelines

A reusable playbook for AI-assisted software development using **ChatGPT as the architecture brain**, **Cursor as the execution layer**, and **GitHub as the memory and collaboration layer**.

## Goal

This repository stores the operating guidelines for a repeatable AI development workflow:

- ChatGPT defines architecture, scope, sequencing, and acceptance criteria
- Cursor implements, refactors, tests, and reports results
- GitHub stores project memory, templates, decisions, issues, PRs, and execution history
- The human remains the final decision-maker for key technical and product choices

This is **not** a business-code repository. It is a **methodology repository**.

## Core Principles

1. **Separate thinking from execution**
   - ChatGPT handles architecture, decomposition, and prompt design
   - Cursor handles implementation and iteration

2. **Keep tasks small**
   - A single execution round should target one clear outcome
   - Avoid vague goals like "build the whole system"

3. **Always define boundaries**
   - State what Cursor may change
   - State what Cursor must not change
   - State what success looks like

4. **Document decisions outside the chat**
   - Long-term project memory belongs in GitHub docs, not only in conversations

5. **Human review remains mandatory**
   - Architecture changes, database changes, security-sensitive changes, and production-impacting changes must be reviewed explicitly

## Recommended Workflow

1. Define the task
2. Choose the model strategy: Auto vs manual model selection
3. Ask ChatGPT to generate a Cursor prompt
4. Let Cursor execute within a narrow scope
5. Capture the result: changed files, test output, blockers
6. Feed the result back into ChatGPT for the next round
7. Record key decisions and status in the project repository

## Repository Structure

```text
/docs
  WORKFLOW.md
  MODEL_SELECTION.md
  TASK_BREAKDOWN.md
  HANDOFF_PROTOCOL.md
/templates
  ARCHITECTURE_TEMPLATE.md
/prompts
  cursor_execute_prompt.md
/rules
  cursor_rules.md
/.github
  PULL_REQUEST_TEMPLATE.md
  ISSUE_TEMPLATE/
```

## How to Use This Repository

### For a new project

1. Copy the relevant templates into the project repository
2. Add project-specific architecture, roadmap, tasks, and decisions
3. Use the model selection guide to decide Auto vs manual model
4. Use the Cursor prompt template for each implementation round

### For an active project

1. Summarize the current state into GitHub docs
2. Ask ChatGPT to plan the next round
3. Have Cursor execute a constrained task
4. Feed results back for the next step

## Minimum Project Docs Recommended in Each Business Repository

- `docs/ARCHITECTURE.md`
- `docs/ROADMAP.md`
- `docs/TASKS.md`
- `docs/DECISIONS.md`
- `docs/HANDOFF.md`
- `docs/CURSOR_RULES.md`

## Execution Policy

Use Cursor for implementation, but do **not** let it define product direction on its own.

Good example:
- "Implement SQLite persistence for lineage records under `backend/app/models` and `backend/app/api`, do not touch frontend, and report changed files plus test results."

Bad example:
- "Build the whole data platform automatically."

## What This First Version Contains

This initial version includes:

- a collaboration workflow
- model selection guidance
- task sizing rules
- a result handoff protocol
- a project architecture template
- a reusable Cursor execution prompt
- baseline Cursor operating rules
- GitHub PR and issue templates

Future versions can add:

- bugfix prompt templates
- refactor prompt templates
- review checklists
- automation/webhook conventions
- branch and release policies

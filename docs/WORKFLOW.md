# Workflow

This workflow defines how **human + ChatGPT + Cursor + GitHub** collaborate during software development.

## Roles

### Human
- defines business priority
- approves key architectural changes
- reviews important pull requests
- decides whether to continue, rollback, or change direction

### ChatGPT
- acts as architect and task orchestrator
- decomposes work into small execution rounds
- chooses whether a round should use Auto or a manually selected model
- generates Cursor-ready prompts
- interprets Cursor output and plans the next round

### Cursor
- acts as execution engineer
- reads repository context
- makes code changes within scope
- runs tests or validation commands
- reports changed files, results, and blockers

### GitHub
- stores long-term project memory
- holds docs, issues, PRs, templates, and decision logs
- provides a stable source of truth outside transient chat context

## Standard Round Protocol

### Step 1: Input
The human provides:
- task name
- target outcome
- current state
- scope
- constraints
- whether the task is critical

### Step 2: Planning
ChatGPT returns:
- recommended model mode: Auto or manual
- task boundary
- allowed files or directories
- forbidden files or directories
- acceptance criteria
- a Cursor-ready prompt

### Step 3: Execution
Cursor should:
1. read the relevant project docs
2. summarize the execution plan
3. implement the smallest viable change set
4. run the relevant test or validation commands
5. report changed files and outcomes

### Step 4: Handoff
The human returns one or more of:
- Cursor summary
- changed files
- git diff
- test output
- logs
- blocker description

### Step 5: Iteration
ChatGPT decides whether to:
- continue
- fix a failed round
- split the task further
- switch models
- move to the next phase

## Recommended Input Format

```text
[Task Name]
[Goal]
[Background]
[Current State]
[Touched Modules]
[Constraints]
[Desired Output of This Round]
[Critical Task] yes/no
[Auto Allowed] yes/no
```

## Recommended Output Format for Cursor

```text
1. Execution plan
2. Changed files
3. Summary of changes
4. Validation or test results
5. Unfinished items
6. Risks or blockers
```

## Branch Strategy

Use one branch per task round or feature slice.

Examples:
- `feat/lineage-parser-mvp`
- `fix/api-timeout-handling`
- `refactor/service-layer-cleanup`

## Key Rule

Do not let Cursor decide product direction independently. Use it to implement a well-defined step, not to redefine the roadmap.
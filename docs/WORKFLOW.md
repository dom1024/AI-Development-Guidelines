# Workflow

This workflow defines how **human + ChatGPT + Cursor + GitHub** collaborate during software development, integrating Claude-inspired multi-round practices.

## Roles

### Human
- Defines business priorities
- Approves key architectural changes
- Reviews critical pull requests
- Determines whether to continue, rollback, or change direction

### ChatGPT
- Acts as architect and task orchestrator
- Decomposes work into small execution rounds
- Determines if a round should use Auto or a manually selected model
- Generates Cursor-ready prompts
- Interprets Cursor output and plans next round

### Cursor
- Acts as execution engineer
- Reads repository context
- Makes code changes within scope
- Runs tests or validation commands
- Reports changed files, results, and blockers

### GitHub
- Stores long-term project memory
- Holds docs, issues, PRs, templates, and decision logs
- Provides a stable source of truth outside transient chat context

## Standard Round Protocol

### Step 1: Input
The human provides:
- Task name
- Target outcome
- Current state
- Scope
- Constraints
- Whether the task is critical

### Step 2: Planning
ChatGPT returns:
- Recommended model mode: Auto or manual
- Task boundary and allowed/forbidden files
- Acceptance criteria
- Cursor-ready prompt

### Step 3: Execution
Cursor should:
1. Read relevant project docs
2. Summarize the execution plan
3. Implement minimal changes
4. Run tests/validation
5. Report changed files, test results, and blockers

### Step 4: Handoff
The human collects output:
- Cursor summary
- Changed files
- Git diff
- Test results
- Blocker description

### Step 5: Iteration
ChatGPT decides whether to:
- Continue
- Fix a failed round
- Split the task further
- Switch models
- Move to next phase

## Phase-based Execution
- Plan Phase: Generate execution plan
- Execute Phase: Implement changes
- Verify Phase: Validate output and report results

## Recommended Input Format
```
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
```
1. Execution Plan
2. Summary of Changes
3. Changed Files
4. Test Results
5. Blockers / Risks
```

## Branch Strategy
- One branch per task round or feature slice
- Examples: feat/lineage-parser-mvp, fix/api-timeout-handling, refactor/service-layer-cleanup

## Key Rule
- Cursor executes tasks but does not define roadmap or product direction
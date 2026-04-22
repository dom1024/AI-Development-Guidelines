# State Tracker Template

This file defines how to persist the multi-round AI execution state for ChatGPT + Cursor + GitHub workflow with low token consumption in mind.

## Purpose
- Maintain long-term context for multi-round tasks
- Record the current status of each task, including completion, blockers, and outputs
- Provide a short summary for ChatGPT input to reduce token usage

## Template Structure

### Task Overview
- Task Name:
- Assigned Round Number:
- Goal:
- Background / Context:
- Involved Modules:
- Critical Task: Yes/No
- Auto Allowed: Yes/No

### Execution Summary
- Cursor Execution Plan:
- Changed Files:
- Test Results / Validation:
- Blockers / Risks:
- Notes / Comments:

### Status Tracking
- Completed: Yes/No
- Pending Actions:
- Next Round Assigned:
- Responsible Party:
- Remarks:

### Phase Tracking
- Phase: Plan / Execute / Verify
- Phase Status: Pending / In Progress / Completed
- Phase Notes:

### Summary for Next Round
- Short summary of completed phases and key results (to feed ChatGPT)
- Key blockers or pending tasks
- Critical decisions
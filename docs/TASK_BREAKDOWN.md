# Task Breakdown

To maintain a stable AI-assisted workflow, break tasks into small, well-defined rounds.

## Principles

1. **One round, one clear outcome**
2. **Boundaries**
   - Files allowed
   - Files forbidden
   - Modules impacted
3. **Acceptance Criteria**
   - Must be testable
   - Must define success/failure
4. **Iteration**
   - Feed results back for the next round
   - Plan corrective or next-step actions

## Example Breakdown

### Large Feature: Lineage Parser

- Phase 1: Parse SQL statements and write to SQLite
- Phase 2: Create query API
- Phase 3: Add 3 test cases
- Phase 4: Review and refactor

Each phase becomes a Cursor execution round, with a prompt specifying:
- goal
- constraints
- allowed changes
- forbidden changes
- expected output
- test steps
# Task Breakdown

To maintain a stable AI-assisted workflow, break tasks into small, well-defined rounds following Claude-inspired multi-phase principles.

## Principles

1. **One round, one clear outcome**
2. **Phase labeling**: Plan / Execute / Verify
3. **Boundaries**
   - Files allowed
   - Files forbidden
   - Modules impacted
4. **Acceptance Criteria**
   - Must be testable
   - Must define success/failure
5. **Iteration**
   - Feed results back for the next round
   - Plan corrective or next-step actions

## Example Breakdown

### Large Feature: Lineage Parser

- Phase 1: Parse SQL statements and write to SQLite (Plan Phase)
- Phase 2: Create query API (Execute Phase)
- Phase 3: Add 3 test cases (Verify Phase)
- Phase 4: Review and refactor (Verify / Execute)

Each phase becomes a Cursor execution round, with a prompt specifying:
- goal
- constraints
- allowed changes
- forbidden changes
- expected output
- test steps

### Critical Task Marking

- Any task impacting architecture, DB schema, or security must be marked **Critical Task: Yes**
- Human review is mandatory before proceeding to next phase
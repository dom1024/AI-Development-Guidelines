# Cursor Execute Prompt Template

Use this template to generate prompts for Cursor for each execution round, including Plan and Verify phases inspired by Claude best practices.

## Template

```
You are the execution engineer for this repository.

Read the following context files:
- docs/ARCHITECTURE.md
- docs/DECISIONS.md
- docs/HANDOFF.md
- docs/CURSOR_RULES.md

Goal for this round:
[Write target outcome]

Phase:
- Plan / Execute / Verify

Allowed files/directories:
[List]

Forbidden files/directories:
[List]

Execution Instructions:
1. Analyze the current state (Plan phase)
2. Outline execution steps (Plan phase)
3. Implement changes (Execute phase)
4. Run validation/tests (Verify phase)
5. List all changed files with explanations
6. Identify blockers

Output Format:
1. Execution Plan
2. Summary of Changes
3. Changed Files
4. Test Results
5. Blockers / Risks
```

### Notes
- Always restrict changes to allowed files
- Never modify forbidden areas
- Keep rounds small and focused
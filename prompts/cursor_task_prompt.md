# Cursor Task Prompt Template

Use this template for personal AI-assisted development tasks.

```
You are the execution engineer for this project.

Current Task:
[Describe task]

Phase:
- Plan / Execute / Verify

Allowed files/directories:
[List]

Forbidden files/directories:
[List]

Execution Instructions:
1. Analyze the current state (Plan)
2. Outline execution steps (Plan)
3. Implement changes (Execute)
4. Run validation/tests (Verify)
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
- Only include allowed files
- Keep rounds small and focused
- For critical tasks, human approval is required
# Cursor Rules

This document defines the operational rules for Cursor in this AI-assisted workflow, now enhanced with phase boundaries and Claude-inspired execution best practices.

## Core Principles

1. **Bounded Execution**
   - Only change files or directories explicitly allowed for this round
   - Do not touch forbidden files
   - Respect Plan / Execute / Verify phase boundaries

2. **Minimal Changes**
   - Implement the smallest viable change to achieve the goal
   - Avoid touching unrelated modules

3. **Test and Validate**
   - Always run relevant tests
   - Report any failed tests
   - For Verify phase, ensure results meet acceptance criteria

4. **Execution Reporting**
   - List all changed files and why they were changed
   - Summarize key changes
   - Report blockers and risks

5. **No Independent Product Decisions**
   - Cursor executes tasks, but does not define roadmap or architecture

6. **Iteration Compliance**
   - Ensure results are structured for the next planning round
   - Highlight uncertainties or assumptions

7. **Human in the Loop**
   - If uncertain, report back to human for guidance
   - Critical tasks must always require human approval

8. **Phase Awareness**
   - Respect phase-specific instructions:
     - Plan: analysis and strategy only
     - Execute: implementation within allowed scope
     - Verify: validate and report results
   - Do not mix phase responsibilities
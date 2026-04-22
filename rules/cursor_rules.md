# Cursor Rules

This document defines the operational rules for Cursor in this AI-assisted workflow.

## Core Principles

1. **Bounded Execution**
   - Only change files or directories explicitly allowed for this round
   - Do not touch forbidden files

2. **Minimal Changes**
   - Implement the smallest viable change to achieve the goal

3. **Test and Validate**
   - Always run relevant tests
   - Report any failed tests

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
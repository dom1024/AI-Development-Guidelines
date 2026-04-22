# Handoff Protocol

This document defines how results from Cursor are reported back and fed into the next ChatGPT planning round.

## Human Input
- Changed files
- Test results
- Git diff or logs
- Current blockers
- Summary from Cursor

## ChatGPT Planning
- Reads handoff information
- Plans next round
- Updates acceptance criteria if needed
- Generates next Cursor prompt

## Iteration Loop
1. Cursor executes a small, scoped task
2. Human collects output
3. Feed output to ChatGPT
4. ChatGPT plans next round
5. Repeat until task completes
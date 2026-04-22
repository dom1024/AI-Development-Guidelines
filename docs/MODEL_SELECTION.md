# Model Selection

This guide explains when to use **Cursor Auto** and when to manually select a model.

## Default Rule

- Use **Auto** for small, low-risk, high-frequency implementation tasks
- Use **manual model selection** for high-impact, long-horizon, architecture-sensitive tasks

## Use Auto When

Auto is appropriate for:
- small bug fixes
- simple refactors
- test additions
- log investigation
- minor API adjustments
- documentation updates tied to code
- routine implementation steps where style consistency is less critical

Auto is best when:
- the task is short
- the risk is low
- speed matters more than absolute consistency
- you do not want to manage model choice yourself

## Use Manual Model Selection When

Manual selection is recommended for:
- architecture-level changes
- cross-module refactors
- database schema changes
- security-sensitive code
- infrastructure or deployment changes
- complex debugging requiring deep reasoning
- large multi-step implementation rounds
- work where reproducibility matters

Manual selection is best when:
- you already know the type of reasoning required
- the task spans many files or phases
- you want stable style and behavior across the round
- the task is expensive to get wrong

## Practical Team Rule

Use this heuristic:

- **small chores** -> Auto
- **critical battles** -> manual

## Suggested Development Split

### ChatGPT
Use for:
- architecture
- design tradeoffs
- sequencing
- task decomposition
- writing the Cursor prompt

### Cursor Auto
Use for:
- scoped execution rounds
- low-risk implementation work
- repetitive edits
- ordinary coding flow

### Cursor with Manual Model
Use for:
- large refactors
- first-pass implementation plan
- critical fixes
- tasks with strict output expectations

## Anti-Pattern

Do not use Auto for the first round of a large, ambiguous task like:

> Build the full platform and improve the structure as needed.

Instead, first define:
- target scope
- file boundaries
- acceptance criteria
- validation steps

Then decide Auto or manual.

## Round-by-Round Checklist

Before each Cursor round, answer:

1. Is this task critical?
2. Is the task multi-step?
3. Does it touch architecture or data design?
4. Do I need reproducible behavior?
5. Would a model switch midstream be risky?

If two or more answers are **yes**, prefer manual model selection.
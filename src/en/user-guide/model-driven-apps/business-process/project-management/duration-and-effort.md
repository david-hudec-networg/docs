---
author: David Hudec
---

# Duration and effort

At the start of a project, tasks only have estimated start and end dates. Those dates are calculated from the project start, template durations, and dependencies.

When users begin a task, they set the **Actual Start**. When they finish it, they set the **Actual End**. From that information, the task **Duration** is derived.

## Duration is not the same as work time

A task duration of seven days does not mean someone worked seven full days without interruption. It only reflects the number of working days between the first time work started and the point when the task was finished.

## Two ways to track more precise work

### Task splitting

Task splitting can model pauses in work:

- by summing the durations of subtasks
- or by recording pauses and subtracting their duration from the task

The source notes that this is **not recommended**, because parent duration can already be represented by child task duration.

### Effort

Effort is tracked separately through:

- original estimate
- effort spent
- effort remaining

This can also be used to calculate percentage completion. Once **Effort Remaining** reaches `0`, the task is completed.

## Prototype scenarios

- In a project, open a task on a Gantt layout and set the start and end date.
- Show duration updating automatically.

### Variant 1: Duration

- Show duration calculated from child task durations.
- Show a pauses subgrid as an example of how alternative tracking could work.

### Variant 2: Effort

- Show fields for original estimate, effort spent, effort remaining, and progress percentage.
- Set original estimate to `30`, effort spent to `20`, and effort remaining to `20`, then show progress as `50%`.
- Set effort spent to `35` and effort remaining to `0`, then show progress as `100%` and mark the task as done automatically.

## Figma prototypes

- [Duration variant](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN?node-id=24197-43032&viewport=3806%2C-7773%2C0.22&t=F9p33na19NL3Q5Np-0&scaling=contain&content-scaling=fixed&starting-point-node-id=24197%3A43032&show-proto-sidebar=1)
- [Effort variant](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN?node-id=24203-51429&viewport=3806%2C-7773%2C0.22&t=F9p33na19NL3Q5Np-0&scaling=contain&content-scaling=fixed&starting-point-node-id=24203%3A51429&show-proto-sidebar=1)

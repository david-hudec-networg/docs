---
author: David Hudec
---

# Parent task aggregations

> TL;DR: Parent tasks derive their start and end dates from their children by taking the earliest child start and the latest child end.

## Scheduling behavior

As soon as a task has child tasks, it is no longer scheduled directly. Its scheduling properties are derived from its children rather than edited individually.

That includes:

- start
- end
- duration

## Progress and effort

If effort tracking is enabled, the parent task can derive progress from the effort spent and remaining across child tasks.

## Ownership and dependencies

The parent task still keeps its own owner so accountability remains visible for larger parts of the project. Dependencies can also exist on parent tasks, which makes it possible to keep a high-level process flow even when the work is split into subtasks.

This also means the main critical path can exist at any depth:

- upper levels act like folders
- lower levels act like the partial steps needed for completion

## Prototype scenarios

- In a project, open the Gantt layout.
- Take a task without children and add a child task.
- Show the parent converting in the Gantt chart and locking its duration and dates.
- Add a second child task with a later end date and stretch the parent task to cover the whole child range.
- Open the parent task and show duration, start, and end as locked fields while still allowing a separate owner.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN?node-id=24081-59669&viewport=4725%2C-9036%2C0.28&t=EjXlkr61GTLlknUk-0&scaling=contain&content-scaling=fixed&starting-point-node-id=24081%3A59669&show-proto-sidebar=1)

---
author: David Hudec
---

# Critical path

> Note: This page is based on an AGTDSV Loop snapshot dated **19.03.2026**. The source note says a copy was moved into the Cetin tenant.

In most projects, there is a main chain of tasks linked by dependencies that determines when the project can finish. That chain is the **critical path**.

If any task on that path is delayed, the whole project is delayed.

## How the source describes it

If the project is treated as a tree of tasks, the critical path acts like the **trunk** of that tree.

Users need a fast way to see which tasks are on that path. In the Gantt layout, they should be able to turn on a setting that highlights:

- tasks on the critical path with red corners
- dependencies on the critical path with red arrows

Any change to a task or dependency should immediately recalculate the path.

## Prototype scenarios

- In a project, open the timeline layout.
- Turn on the **Critical Path** setting.
- Show the critical path tasks and dependencies with red visual highlighting.
- Add a new task in the middle of the chain with a later end date and redraw the critical path.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN)

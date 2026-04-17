---
author: David Hudec
---

# Milestones

> Note: This page is based on an AGTDSV Loop snapshot dated **19.03.2026**. The source note says a copy was moved into the Cetin tenant.

If tasks represent the work to be done, milestones represent the deadlines that need to be met.

## How milestones work

- A milestone has a specific date.
- A milestone can be linked to many tasks.
- A task marked as relevant to a milestone stores which milestone it relates to.
- A milestone can be closed once all connected tasks are complete.

## Planning implications

Milestones are harder to move than tasks, because changing them usually requires agreement with the party expecting the deadline.

By comparing the latest task end date with the milestone date, project leads can see:

- remaining runway if the tasks still finish before the milestone
- the number of days overdue if they do not

That helps project leads decide whether to shorten some task durations or negotiate a milestone change.

## Baselines and visuals

Like tasks, milestones can be stored in a baseline so later comparisons stay possible.

The source describes two visual options:

- on a Gantt chart, milestones appear as vertical lines crossing the task bars
- on a hierarchical task grid, connected tasks show a colored marker, and tasks ending after the milestone are underlined in red

## Prototype scenarios

- In a project, open the timeline layout.

### Variant 1: Top marks

- Show milestone markers as colored arrows at the top of the layout.
- Hover over a milestone and extend a line across the whole layout.
- Click the milestone and open a dialog with its details.

### Variant 2: Dashed or thin lines

- Show milestone markers together with lines across the layout.
- Show a task connected to a milestone.
- Show how a task becomes overdue compared with the milestone.
- In the task grid, highlight tasks whose end date passes the milestone date.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002---CETIN?page-id=23163%3A51994&node-id=23935-47667&viewport=12278%2C-18424%2C0.73&t=YuDvHeZBdJm74Qjz-1&scaling=contain&content-scaling=fixed&starting-point-node-id=23935%3A47667&show-proto-sidebar=1)

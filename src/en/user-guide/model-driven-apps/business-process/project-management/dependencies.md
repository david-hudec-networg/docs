---
author: David Hudec
---

# Dependencies

> Note: This page is based on an AGTDSV Loop snapshot dated **19.03.2026**. The source note says a copy was moved into the Cetin tenant.

Most tasks are not freely available from the start of a project. To start or finish, they depend on other tasks. This is handled through dependencies.

## Dependency details

A task can have multiple dependencies in both directions:

- tasks it depends on
- tasks that depend on it

Each dependency has a type:

- **SS** - Start to Start
- **SF** - Start to Finish
- **FS** - Finish to Start
- **FF** - Finish to Finish

Dependencies can also contain an offset, usually expressed as a number of days of delay between the connected tasks.

## Circular dependencies

Users must be prevented from creating circular dependencies, even when the cycle spans many tasks.

If a circular dependency would be created, the user should receive an error explaining the problem.

The source also notes that child tasks behave as if the parent had a finish-to-finish dependency on them for scheduling purposes.

## Dependency timing cascade

If a task timing value changes and another task depends on that value, the connected task should update automatically.

For example, if **Task 1** finishes on Thursday at 5 PM and **Task 2** has an **FS** dependency, **Task 2** should be moved so it does not start before that point.

Timing cascades must also respect working days. A two-day task moved to Friday should still end on Monday while keeping its duration at two working days.

If a task on the critical path moves, the cascade can push later work beyond milestone deadlines.

## Parent task dependencies

Parent tasks can also have dependencies. This makes it possible to split work into more granular tasks without losing the higher-level process flow.

During scheduling, the system effectively treats parent tasks as if they had finish-to-finish dependencies on all child tasks.

### Draft technical proposal

The Loop note includes a draft proposal where:

- parent tasks are not scheduled directly
- parent tasks do not participate directly in the dependency graph or critical path calculation
- a virtual gateway task is created when dependencies exist on a parent task
- only leaf tasks and gateway tasks participate in dependency graph construction, date cascading, and critical path calculation

## Visuals

Dependencies are intended to appear:

- as a list on the task
- as lookup values or quick-look icons in project task views
- as arrows between tasks in a Gantt chart

## Prototype scenarios

- In a project, open the timeline layout.
- Show tasks linked with dependency arrows.
- Let the user drag from one task connection point to another.
- Show the dependent task move because its schedule now follows the source task.
- Hover over the dependency arrow and show its type and lag.
- Open a task and show dependencies in a subgrid.
- Add a new dependency from the dialog.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/dQjme4zF8W5HxYdMnIiuW4/NETWORG-Project-Management)

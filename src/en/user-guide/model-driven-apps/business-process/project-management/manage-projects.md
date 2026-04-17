---
author: David Hudec
---

# Project Management

In essence, it is a widely standardized area of work.

- Projects are grouped into Programs (by logical synergies) or Portfolios (by finance strategies) and have Tasks
- Tasks have estimated dates and eventually actual dates, and dependencies on each other — these move subsequent estimated dates
- These frequently moving Tasks are compared to Milestones, which act as promised deadlines — these can also move, if agreed on, but usually this requires external agreement (contracts, events, etc)
- Both Tasks and Templates are created individually, or from Templates, which only keep basic dynamic information — Project Roles of Assignees, Durations, and Dependencies

However, there are features not seen in Project Management commonly:

- Start linking dependencies at any level — all parent tasks will simply act as "folders" and all subtasks will act as partial steps for completion (while still carrying all task attributes — unlike checklists)
- Keep specific Tasks linked to Milestones — so their estimates can be easily compared to deadlines
- Dynamically render necessary info and input fields based on original task template definitions — to avoid Tasks tracked separately from actual data input; this allows users to finish work directly from the task and submit it + mark the task as complete at the same time

> **Note:** As of writing, there is no solution for auto-closing tasks for users inputting necessary info directly into target entities without touching the corresponding Task.

![[Project Management Diagram.png]]

## Core Concepts

Projects are organized into programs or portfolios and executed through **Tasks** with estimated and actual dates, dependencies, and Milestones. As tasks move, their dependent tasks automatically shift, and these changes are compared against fixed or contract-bound Milestones.

Parent tasks function as **containers**, with their dates and duration derived from their subtasks. Subtasks remain full tasks with all attributes, unlike checklists.

## Task Templates

Templates define reusable structures that drive project creation. They include:

- **Duration-based scheduling** rather than fixed dates
- **Dependencies** for calculating start/end dates
- **Role-based assignment** instead of specific users
- **Dynamic fields** determining what appears in each task form

When a project is created, the system generates tasks down the entire dependency hierarchy, calculates dates from durations, and maps roles to actual people.

Templates can be bundled into larger hierarchies, supporting multi-stage processes without duplication.

Once used, a template becomes **locked** and must be replaced rather than modified.

## Dynamic Task Forms

Each task links back to its originating template, allowing the system to render context fields for reading and input fields for writing directly on the Task dialog. This eliminates the need to navigate multiple tables or forms.

Users can complete required work and mark the task done in the same step, ensuring clean data entry and consistent workflow.

## Scheduling, Cascading & Critical Path

The system supports dependency linking at any level. Task date changes cascade automatically, enabling accurate evaluation of delays and planning impact.

Critical Path and Baselines provide standardized reporting and scenario comparison.

## Milestones

Milestones represent contractual or externally agreed deadlines. They compare shifting task estimates with fixed expectations.

Milestone Templates store their tasks but have **no duration** — their final date is derived from the end of the last task.

## Execution & Governance

- Coordinators manage execution via Task Grids and Gantt charts
- Tasks created from templates can be adjusted but **not deleted**
- Task statuses (Planned, Active, Blocked, Completed, etc.) support consistent project tracking
- Parent task progress aggregates from child task durations and effort

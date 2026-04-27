---
author: David Hudec
---

# Project Management

Over the last 20 years, managing projects has become a widely standardized area of work.

- Projects are grouped into Programs (by logical synergies) or Portfolios (by finance strategies), are optionally split into Stages, and have Tasks
- Tasks have estimated dates and eventually actual dates, and depend on each other — moving a driving task will also move subsequent dependent tasks
- Tasks, which move frequently, are compared to Deadlines, representing external obligations, which move only once agreed upon
- Both Tasks and Deadlines are created ad-hoc or from Templates - these only keep basic dynamic information — Project Roles, Durations, and Dependencies

However, there are features not seen in Project Management commonly:

- create Dependencies at any Task level — all parent Tasks will simply act as "folders" and all subtasks will act as partial steps for completion (while still carrying all Task attributes, unlike Checklists)
- Keep specific Tasks linked to Deadlines — so the estimated delivery can be easily compared to the deadline
- keep multiple Baselines for history, reporting or projecting potential future scenarios
- Dynamically render necessary info and input fields based on original Task Template definitions, to avoid Tasks tracked separately from actual data input, allowing users to finish work directly from the Task and submit it + mark it as complete at the same time

> **Note:** As of writing, there is no solution for auto-closing tasks for users inputting necessary info directly into target entities without touching the corresponding Task.

## Core Concepts

Projects are organized into Programs or Portfolios, split into Stages and executed through Tasks with estimated and actual dates and Dependencies. As Tasks move, their dependent Tasks automatically move as well, and these changes are compared against fixed or contract-bound Deadlines.

Parent Tasks function as **containers**, with their dates and duration derived from their child Tasks. Subtasks remain full Tasks with all attributes (unlike Checklists).

## Deadlines

Deadlines represent contractual or externally agreed dates. They compare shifting task estimates with fixed expectations.

Deadline Templates store their tasks but have **no duration** — their final date is derived from the end of the last task.

## Task Templates

Templates define reusable structures that drive Project creation. They include:

- **Duration-based scheduling** rather than fixed dates
- **Dependencies** for calculating start/end dates
- **Role-based assignment** instead of specific users
- **Dynamic fields** determining what appears in each task form

**Task Template Pointers** allow pointing to any Task Template, or multiple ones, and acts as the package for the reusable hierarchy. The actual Tasks are generated from the Template Tasks inside their hierarchy, and carry the scheduling, dependency, stage, role, and dynamic form rules.

When a project is created, the system generates Tasks down the entire dependency hierarchy, calculates dates from durations, and maps roles to actual people.

Once used, a Task Template becomes **locked** and must be replaced rather than modified, in order to prevent losing dynamic form definitions.

## Dynamic Task Forms

Each Task links back to its originating Task Template, allowing the system to render context fields for reading and input fields for writing directly on the Task dialog. This eliminates the need to navigate multiple tables or forms.

Users can complete required work and mark the Task as done in the same step, ensuring clean data entry and consistent workflow.

## Scheduling, Cascading & Critical Path

The system supports dependency linking at any level. Task date changes cascade automatically, enabling accurate evaluation of delays and planning impact.

Critical Path and Baselines provide standardized reporting and scenario comparison.

## Execution & Governance

- Coordinators manage execution via Task Grids and Gantt charts
- Tasks created from Task Templates can be adjusted but **not deleted**
- Task statuses (Planned, Active, Blocked, Completed, etc.) support consistent project tracking
- Parent Task progress aggregates from child Task durations and effort

---
author: David Hudec
---

# Task templates

> Note: This page is based on an AGTDSV Loop snapshot dated **19.03.2026**. The source note says a copy was moved into the Cetin tenant.

Task templates package repeatable task structures so projects can generate consistent work with the right durations, dependencies, roles, and required inputs.

## Covered topics

The source page covers:

- headers
- creating templates
- creating tasks
- task template stages
- template hierarchies
- task template dependencies
- dynamic dates using durations, dependencies, and offsets
- dynamic assignees from roles
- dynamic readable or writeable fields, subgrids, and documents
- milestone templates
- dynamic durations and repeating tasks

## Headers

The source notes that templates are currently built from a top-level task. To support a clearer user experience, it proposes a separate **Task Template Header** where users provide:

- the template header name
- the tasks that should be included under it

## Creating templates

Two approaches are described for adding subtasks to a new template:

- only include the explicitly selected tasks
- make all selected tasks top-level template tasks and recursively include all of their children

The source recommends the second approach.

When a template is created, users should see a dialog that:

- captures the template header name
- shows the full structure that will be included
- lets the user exclude specific child tasks before saving

## Dependencies in templates

Task templates can keep dependencies in the same way as regular tasks. The dependency type and offset should be preserved so later task generation can calculate dates correctly.

## Creating tasks from templates

When users apply a template to a project, the system should open a dialog that shows the tasks to be created together with pre-filled:

- dates
- tags
- dependencies
- assignees

The user can then select the start date or the dependent task used for date calculation, adjust task values, and deselect tasks that should not be created.

## Stages and hierarchies

Task templates reference stages so reporting stays standardized, and templates should be stackable into larger bundles without forcing duplicated maintenance.

## Dynamic template behavior

Templates can define:

- durations instead of fixed dates
- child offsets to preserve total parent duration
- roles instead of concrete users
- dynamic readable or writeable fields, subgrids, and documents shown in the generated task form
- milestone templates that keep tasks but do not carry duration
- range-based or rule-based durations, including repeating tasks

## Figma prototypes

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN)
- [Variant 2](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN)

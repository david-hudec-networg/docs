---
author: David Hudec
---

# Task templates

Task templates package repeatable task structures so projects can generate consistent work with the right durations, dependencies, roles, and required inputs.

## Covered topics

- headers
- creating templates
- creating tasks
- task template stages
- template hierarchies
- task template dependencies
- dynamic dates using durations, dependencies, and offsets
- dynamic assignees from roles
- dynamic readable or writeable fields, subgrids, and documents
- deadline templates
- dynamic durations and repeating tasks

## Pointers

Task templates mirror actual tasks, and so exist in a hierarchy. They can be artibtratily complex and form one giant tree or multiple distinct ones.

However, generating tasks from templates can require spawning the entire tree, spawning only a specific part of the template tree, spawning multiple template trees next to each other, or a combination of the above. To solve this, templates are spawned from pointers.

A task template pointer allows selecting one or multiple template tasks, and for each one selected, a task will be spawned for the enitre hierarchy living under the selected task template.

- if an entire task template tree needs to be used, the pointer keeps the top level task
- if only a part of the tree needs to be used, the pointer keeps reference to only the task where it should start
- if multiple trees should be spawned, the pointer references all the tasks which ashould become the starting "top level tasks" spawned

This allows templates to be kept in a single hierarchy, while enabling spawning tasks from any point inside it. This means one template task tree can allow spawning the entire task tree or only one or multiple specific parts of it.

## Creating templates

Users can select one or multiple tasks in a project, provide a name and create a template from them. Optionally, the user can choose to create a pointer to all the new task templates.

The app will take each selected task and create a new template from it, and from each child task in the original task's hierarchy.

If two tasks converted into templates keep a dependency, it will also be converted into a template dependency.

In order to keep logical connections, task templates can be grouped into an arbitrary parent tak template.

## Dependencies in templates

Task templates can keep dependencies in the same way as regular tasks. The dependency type and offset should be preserved so later task generation can calculate dates correctly.

If a template dependency exists and both its task templates are used to spawn tasks, the dependency will also be spawned.

## Creating tasks from templates

Users can select a pointer to spawn tasks, either as top-level or as children under a specific task. The app presents a dialog showing all the tasks to be spawned, along with pre-filled:

- start and end dates
- tags
- dependencies
- assignees

The user can then select the start date or the driving task used for date calculation, adjust task values, and deselect tasks that should not be created.

## Dynamic template behavior

Since template tasks serve as an absraction, they define:

- durations instead of fixed dates
- child offsets to preserve total parent duration
- roles instead of specific users
- dynamic readable or writeable fields, subgrids, and documents shown in the generated task form
- deadline templates that keep tasks but do not carry duration
- range-based or rule-based durations, including repeating tasks

These behaviors belong to the relevant template tasks in the hierarchy. That includes duration-based scheduling, dependencies, stage references, role-based assignment, and dynamic task form behavior.

## Figma prototypes (to be updated)

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN)
- [Variant 2](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN)

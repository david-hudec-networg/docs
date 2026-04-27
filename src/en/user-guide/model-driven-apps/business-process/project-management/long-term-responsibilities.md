---
author: David Hudec
---

# Long term responsibilities

Companies usually have rules for who is responsible for which Task, but those rules can depend on different business factors. For example, Sales can divide responsibilities by geography, while Finance can divide them by budget size.

## Responsibility matrix

To support those combinations, the design uses a single **Responsibility Matrix**. Each entry specifies:

- the role being used
- the conditions that must be met
- the user who should be selected
- the responsibility type, such as **Responsible**, **Accountable**, **Consulted**, or **Informed**

## Conditions

Conditions are built similarly to filters in views:

- each condition specifies a table
- each condition contains a list of filters

This makes the matrix flexible enough to support many condition types and even overlaps.

## How it is used

The matrix is the main source for selecting people for tasks.

When a new task is created and a role is already known, for example from a task template, the matrix can return:

- no matching people
- one matching person
- multiple matching people

The matching can use information from the Project, Stage, and any other available context. This makes the matrix useful not only for building the initial project team, but also for ad-hoc Task assignments.

---
author: David Hudec
---

# Task ownership

> Note: This page is based on an AGTDSV Loop snapshot dated **19.03.2026**. The source note says a copy was moved into the Cetin tenant.

In advanced scenarios, tasks can have both **Responsible** and **Accountable** people.

## Ownership model

The source makes these assumptions:

- there is always one accountable person
- there can be multiple responsible people
- responsible people might not have access to the system

With that model:

- the **Accountable** person becomes the task **Owner**
- the **Responsible** people become the task **Assignees**

## Notifications

Some people should only be **Informed** when a task reaches a certain point or finishes. In those cases, the system should send a notification that the user can dismiss or follow back to the originating record.

## Prototype scenarios

- In a project, open a task on a Gantt layout.
- Open the task form and show both Owner and Responsible fields.
- Select a single owner through a lookup.
- Select multiple responsible people through a multi-lookup from users or contacts.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN?node-id=24057-42361&viewport=3886%2C-6697%2C0.22&t=EjXlkr61GTLlknUk-0&scaling=contain&content-scaling=fixed&starting-point-node-id=24057%3A42361&show-proto-sidebar=1)

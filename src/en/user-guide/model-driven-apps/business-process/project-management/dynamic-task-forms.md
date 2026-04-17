---
author: David Hudec
---

# Dynamic task forms

Tasks centralize and coordinate work, but they do not directly store all of the business inputs and outputs needed to finish that work. Dynamic task forms solve that by showing the relevant information directly on the task.

## Why dynamic forms matter

Dynamic forms reduce navigation away from the task and help users:

- see the information they need
- update the correct related data
- close the task from the same working context

The definition of what is shown is stored on the originating **Task Template**, not on the task itself. That lets admins update the behavior directly in the app without deploying a new version.

## Information that can be shown

- display sections, for example as a stepper dialog
- read-only fields
- read-only subgrids
- required fields
- optional fields
- conditional subgrids
- file storage

Closing the task stores the provided data into the originating tables so the work result and the task status stay aligned.

## Previews

When admins define the dynamic layout, they should see an immediate rendered preview. That helps both with error detection and with making the configuration easier to author.

## Prototype scenarios

- In admin settings, open a task template layout.
- Show fields for defining the dynamic form with text-based notation.
- Render a live preview of the dynamic form.
- In a project on the timeline layout, show two UI variants.

### Variant 1: Tabs

- The main tab shows the template-driven dynamic information.
- A second tab shows the static task form.

### Variant 2: Stepper

- The whole window is a custom stepper based on the task template definition.
- A special action opens the static task information separately.

## Figma prototype

- [Variant 1](https://www.figma.com/proto/FyhtWnUnVBljNOM2L5dq4r/PCT24002-CETIN?node-id=23815-38948&viewport=3015%252C-3419%252C0.16&t=F9p33na19NL3Q5Np-0&scaling=contain&content-scaling=fixed&starting-point-node-id=23815%253A38948&show-proto-sidebar=1)

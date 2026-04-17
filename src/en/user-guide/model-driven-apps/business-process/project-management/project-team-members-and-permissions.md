---
author: David Hudec
---

# Project team members and permissions

Not everyone in a project has the same access. Each company can define its own roles, so some users can work across the whole project, some are limited to a specific stage, and others only see tasks assigned to them.

## Project membership

Companies may keep long-term teams, but they can also onboard temporary members to balance workload or cover for missing colleagues.

After creating a project, one of the most important next steps is selecting:

- the member
- the role
- the join date
- an optional end date for access
- an optional stage restriction

This also helps preserve the historical view of who participated in the project over time.

## Assigning people outside the current project team

When a task is assigned to someone as **Accountable** or **Responsible**, and that person is not already part of the project team, the assigning user should be required to confirm:

- the role
- the access dates
- the optional stage restriction

## Prototype scenarios

- Open a project and review the project team members.
- Add a member by selecting the user, role, optional stage, start date, and optional end date.
- Assign two people who are not currently members to a task.
- Show a dialog that lets the user add both people to the project with the missing role and access details.

## Technical options

The frontend model is described as:

**Project + Member + Role + Stage (optional) + From + To (optional)**

### Dynamic rulesets (preferred)

This option adds users to security teams that carry rulesets and business units, with one business unit per project. Plugins then evaluate those security teams and rulesets and only return matching records.

### Sharing and unsharing

This is a more manual option, likely implemented through flows, and it requires explicit unsharing when a user no longer meets the access requirements.

### Custom business units (Yungo-style)

- Each project gets its own business unit.
- Each stage gets its own sub-business unit.
- Team members are added to or removed from the project business unit based on role and access dates.

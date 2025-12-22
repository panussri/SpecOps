# Feature: Sprint Management
**ID**: FEAT-002

## Overview
Allows the team to plan, start, and complete sprints. Sprints provide the "pulse" of the development cycle.

## Scope
- Create new Sprint
- Set Sprint dates
- Start Sprint (make active)
- Complete Sprint (move unfinished tickets to backlog or next sprint)
- Backlog management (assign tickets to sprints)

## Business Rules
1. Only one sprint can be 'active' at a time.
2. Sprints cannot overlap dates (soft warning).
3. "Completing" a sprint requires a decision on open tickets.

## User Stories
- [STY-002-A](stories/STY-002-A_Sprint_Lifecycle.md): Create and Manage Sprint Cycle
- [STY-002-B](stories/STY-002-B_Backlog_Planning.md): Sprint Planning (Backlog)

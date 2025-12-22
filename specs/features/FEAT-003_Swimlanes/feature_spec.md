# Feature: Board Swimlanes & Filtering
**ID**: FEAT-003

## Overview
Enhances the main Kanban board with swimlane capabilities to visualize tickets grouped by different dimensions (primarily Sprints). This enables easier planning and moving tickets between sprints via drag-and-drop.

## Scope
- Group Board by "Sprint" (Swimlanes)
- Filter Board to show multiple sprints (e.g. "Active" + "Next Sprint")
- Drag and drop tickets across swimlanes (updates `sprintId`)

## Business Rules
1. Changing a ticket's swimlane updates its `sprintId`.
2. Collapsed swimlanes should show a summary of ticket counts.

## User Stories
- [STY-003-A](stories/STY-003-A_Swimlanes.md): View Board with Swimlanes
- [STY-003-B](stories/STY-003-B_Cross_Sprint_Drag.md): Drag Tickets between Swimlanes

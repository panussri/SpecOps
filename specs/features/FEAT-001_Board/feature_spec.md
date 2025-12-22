# Feature: Kanban Board
**ID**: FEAT-001

## Overview
The core visualization of the project. A drag-and-drop interface representing the current state of work in the Active Sprint.

## Scope
- Display Columns (Board Columns)
- Display Tickets within columns
- Drag and drop reordering / status updates

## Business Rules
1. Tickets must always belong to a column.
2. Completing a ticket (Drag to Done) updates `Ticket.updatedAt`.

## User Stories
- [STY-001-A](stories/STY-001-A_Kanban_View.md): View Kanban Board
- [STY-001-B](stories/STY-001-B_Drag_Status_Update.md): Drag & Drop Status Updates

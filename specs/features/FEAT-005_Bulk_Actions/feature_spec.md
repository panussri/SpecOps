# Feature: Bulk Actions
**ID**: FEAT-005

## Overview
Allows users to perform actions on multiple tickets simultaneously. This boosts productivity for tasks like moving tickets between sprints, assigning users during grooming, or housekeeping.

## Scope
- Multi-select mechanism on the Board (Shift+Click, Command+Click).
- "Bulk Action Bar" that appears when more than one ticket is selected.
- Supported Actions:
  - Change Status (Move column)
  - Change Assignee
  - Change Priority
  - Delete Tickets

## Business Rules
1. **Selection Visibility**: Selected cards must be visually distinct (highlight/border).
2. **Contextual Action Bar**: The floating action bar must appear only when > 0 items selected.
3. **Safety**: "Delete" must require a double confirmation for bulk operations.
4. **Validation**: If an action is invalid for one of the selected items (e.g. strict status transitions), the operation should be blocked or warned? *Decision*: Simplify for now - assume all transitions valid OR fail all.
5. **Deselection**: Clicking outside a card deselects all. Escape key deselects all.

## User Stories
- [STY-005-A](stories/STY-005-A_Bulk_Selection.md): Multi-select interaction
- [STY-005-B](stories/STY-005-B_Bulk_Operations.md): Performing bulk updates

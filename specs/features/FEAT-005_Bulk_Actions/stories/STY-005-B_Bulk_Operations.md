---
feature_id: FEAT-005
---

# Story: Bulk Operations
**ID**: STY-005-B

## Narrative
As a user, I want to apply changes to all selected tickets efficiently from a central menu.

## Acceptance Criteria
1.  **Action Bar**:
    -   Appears floating at the bottom center (or top) of the screen when ONE or MORE items are selected.
    -   Contains buttons: "Change Status", "Assign", "Priority", "Delete".
2.  **Change Status**:
    -   Dropdown showing all available columns.
    -   Selecting a column moves all selected tickets to that column.
    -   Updates `statusId` for each ticket.
3.  **Change Assignee**:
    -   Dropdown with user list.
    -   Updates `assigneeId`.
4.  **Change Priority**:
    -   Dropdown with 'low', 'medium', 'high', 'critical'.
5.  **Delete**:
    -   Clicking Delete shows a confirmation modal: "Are you sure you want to delete X tickets?".
    -   Confirming permanently removes them.
6.  **Optimistic UI**:
    -   Changes reflect immediately on the board.

## Verification Steps
1.  Select 3 tickets.
2.  Click "Change Priority" -> "High".
3.  Verify all 3 tickets show "High" priority icon.

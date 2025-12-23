---
feature_id: FEAT-005
---

# Story: Bulk Selection
**ID**: STY-005-A

## Narrative
As a user, I want to select multiple tickets on the board so that I can perform actions on them all at once.

## Acceptance Criteria
1.  **Selection Mode Toggle**: (Optional) or Implicit?
    -   *Decision*: Implicit.
2.  **Mouse Interaction**:
    -   Clicking a ticket selects it (and deselects others).
    -   `Cmd/Ctrl + Click` adds/removes a ticket from selection.
    -   `Shift + Click` selects a range of tickets (in the same column).
3.  **Visual State**:
    -   Selected cards have a distinct border color (primary color) and subtle background tint.
    -   Non-selected cards remain distinct.
4.  **Deselection**:
    -   Clicking the board background (empty space in column) clears selection.
    -   Pressing `Escape` clears selection.


## Verification Steps
1.  Click Ticket A -> Selected.
2.  Cmd+Click Ticket B -> A and B Selected.
3.  Click Empty Space -> Selection Cleared.

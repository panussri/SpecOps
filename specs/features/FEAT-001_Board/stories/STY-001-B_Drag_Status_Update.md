# Story: Drag and Drop Tickets
**ID**: STY-001-B
**Parent Feature**: FEAT-001

## Description
As a User, I want to drag tickets between columns to update their status intuitively.

## Acceptance Criteria
1. **Interaction**: User can click and hold a ticket to drag it.
2. **Drop Zones**: Valid columns highlight when dragging a ticket over them.
3. **Update**: On drop, update the `Ticket.statusId` to the new column.
4. **Optimistic UI**: Move the card immediately, then sync with backend (or local store).

## UI/UX Notes
- Use smooth animations (e.g. `framer-motion`).
- Card should slightly rotate or lift when dragged.

## Verification Steps
1. Drag a ticket from 'To Do' to 'In Progress'.
2. Verify the ticket stays in the new column.
3. Refresh page (if persistence implemented) and verify position.

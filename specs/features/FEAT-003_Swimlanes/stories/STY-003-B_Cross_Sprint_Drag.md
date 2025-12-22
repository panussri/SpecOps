# Story: Drag Tickets between Swimlanes
**ID**: STY-003-B
**Parent Feature**: FEAT-003

## Description
As a User, I want to drag a ticket from one Sprint's swimlane to another to reschedule it.

## Acceptance Criteria
1. **Interaction**: Drag ticket from "Sprint A" swimlane to "Sprint B" swimlane.
2. **Update**: Ticket's `sprintId` updates to the target Sprint.
3. **Feedback**: Visual indication of the target swimlane accepting the drop.

## UI/UX Notes
- Highlight the target swimlane background slightly.

## Verification Steps
1. Create two Sprints: A and B.
2. Drag ticket T1 from Swimlane A to Swimlane B.
3. Verify T1's `sprintId` is now Sprint B.

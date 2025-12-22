# Feature 03: Drag and Drop

## User Story
As a user, I want to drag cards between columns to update their status.

## Acceptance Criteria
- [ ] **Visual Feedback:** When dragging, the card being dragged should rotate slightly (3deg) and have a drop-shadow.
- [ ] **Ghosting:** A gray "ghost" placeholder must appear in the drop target zone.
- [ ] **Persistence:** Dropping a card updates the `columnId` in the store immediately.
- [ ] **Constraint:** Users cannot drop a card outside of a valid column.

## Library Preference
- Use `@hello-pangea/dnd` (fork of beautiful-dnd) or `dnd-kit`.
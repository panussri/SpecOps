# Feature 01: Board & Columns

## User Story
As a user, I want to see a board with default columns so that I can visualize my workflow.

## Acceptance Criteria
- [ ] **Default State:** On first load, generate 3 columns: Todo, In Progress, Done.
- [ ] **Layout:** Columns must be arranged horizontally and scroll horizontally on small screens.
- [ ] **Empty State:** If a column has no cards, show a subtle "No tasks" placeholder.
- [ ] **Header:** Each column must have a sticky header with the Title and a "Count" badge (e.g., "Todo (3)").

## Technical Notes
- Use CSS Grid for the board layout.
- Column width should be fixed (e.g., 280px) or responsive min-width.
# Story: View Kanban Board
**ID**: STY-001-A
**Parent Feature**: FEAT-001

## Description
As a Team Member, I want to view the Active Sprint's tickets on a columnar board so that I can see the status of work at a glance.

## Acceptance Criteria
1. **Columns**: Display columns for 'To Do', 'In Progress', 'Done'.
2. **Filtering**: Show ONLY tickets belonging to the currently 'active' Sprint.
3. **Card Detail**: Each card shows Title, Assignee Avatar, Priority Icon, and Ticket ID.
4. **Empty State**: If no active sprint, show a "Plan a Sprint" value proposition.

## UI/UX Notes
- **Layout**: Horizontal scrolling if many columns (though default is 3).
- **Aesthetics**: Glassmorphism background for columns. Cards should have subtle drop shadows.

## Verification Steps
1. Navigate to Dashboard.
2. Ensure an Active Sprint exists with tickets.
3. Verify tickets appear in correct columns based on `statusId`.
4. Verify ticket details match `01_DOMAIN_MODEL.md` properties.

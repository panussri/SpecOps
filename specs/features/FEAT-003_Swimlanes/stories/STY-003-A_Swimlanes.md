# Story: View Board with Swimlanes
**ID**: STY-003-A
**Parent Feature**: FEAT-003

## Description
As a Product Owner, I want to see tickets grouped by Sprint in horizontal swimlanes so that I can visualize work distribution across time.

## Acceptance Criteria
1. **Grouping**: Toggle to "Group by Sprint".
2. **Display**: Each Sprint gets a horizontal row (Swimlane) spanning all columns.
3. **Sorting**: Swimlanes are sorted by Sprint Date (Active first, then Future).
4. **Headers**: Swimlane headers show Sprint Name and Dates.

## UI/UX Notes
- Sticky Swimlane Headers when scrolling.
- Collapsible Swimlanes to hide content.

## Verification Steps
1. Enable "Group by Sprint".
2. Check that tickets belonging to Sprint A are in the Sprint A swimlane.
3. Check that Backlog items (no sprint) appear in a "Backlog" swimlane if configured.

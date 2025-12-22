# Story: Create Ticket Form
**ID**: STY-004-A
**Parent Feature**: FEAT-004

## Description
As a User, I want a dedicated button to open a "Create Ticket" form so that I can add new tasks to the board.

## Acceptance Criteria
1. **EntryPoint**: A "Create Ticket" button is always visible (e.g. in the global header or board header).
2. **Default State**: New tickets are automatically assigned to the "To Do" column.
3. **Form Fields**:
    - **Title** (Required, Text)
    - **Description** (Required, Rich Text/Markdown - supports hyperlinks)
    - **Priority** (Required, Default: Medium)
    - **Type** (Required, Default: Task)
    - **Assignee** (Optional, Select User)
    - **Sprint** (Optional, Select Sprint - Default: Backlog)
    - **Parent Issue** (Optional, Search/Select existing ticket)
4. **Validation**: Submit button is disabled or shows error if Title or Description is empty.
5. **Output**: On success, the ticket is added to the "To Do" column and the modal closes.

## UI/UX Notes
- Modal dialog for focus.
- Auto-focus the "Title" field on open.

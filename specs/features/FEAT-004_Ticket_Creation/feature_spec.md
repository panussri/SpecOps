# Feature: Ticket Creation
**ID**: FEAT-004

## Overview
Provides a centralized way for users to create new work items (Tickets). This feature focuses on capturing essential information, validating inputs, and handling rich assets like attachments.

## Scope
- "Create Ticket" Modal/Form
- Validation rules (Required fields)
- Rich text Support (Hyperlinks)
- File Attachments (Images, PDFs)
- Parent/Child Linking

## Business Rules
1. **Single Entry Point**: Tickets are created via a global "Create Ticket" button. No per-column create buttons.
2. **Default Status**: All new tickets start in the "To Do" column.
3. **Comprehensive Input**: Users can set all non-system fields (Assignee, Sprint, Priority, etc.) during creation.
4. If `sprintId` is not specified, it defaults to Backlog (null).
3. Attachments must be previewable if Image.
4. Tickets must have at least a Title and Priority.

## User Stories
- [STY-004-A](stories/STY-004-A_Create_Ticket_Form.md): Create Ticket Form & Validation
- [STY-004-B](stories/STY-004-B_File_Attachments.md): File Attachments & Previews

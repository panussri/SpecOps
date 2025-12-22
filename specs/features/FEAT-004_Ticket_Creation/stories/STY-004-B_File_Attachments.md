# Story: File Attachments & Previews
**ID**: STY-004-B
**Parent Feature**: FEAT-004

## Description
As a User, I want to attach files (Images, PDFs, Text) to a ticket so that I can provide context like mockups or spec documents.

## Acceptance Criteria
1. **Upload**: Drag & Drop zone or "Browse" button in the Create Ticket form.
2. **Supported Types**: Images (PNG, JPG), PDF, Text.
3. **Preview**:
    - **Images**: Show a thumbnail preview in the form.
    - **PDF/Text**: Show a file icon with the filename.
4. **Validation**: Max file size limit (e.g., 5MB).
5. **Persistence**: Attachments are saved with the Ticket.

## UI/UX Notes
- Nice drop zone with dashed border.
- Ability to remove an attachment before submitting.

# Story: Sprint Lifecycle Management
**ID**: STY-002-A
**Parent Feature**: FEAT-002

## Description
As a Team lead, I want to create, start, and end sprints.

## Acceptance Criteria
1. **Create**: Form to input Sprint Name, Start Date, End Date. Status defaults to 'planned'.
2. **Start**: Button to "Start Sprint". Changes status to 'active'.
    - Error if another sprint is already active.
3. **Complete**: Button to "Complete Sprint".
    - Modal appears summarizing completed vs. open tickets.
    - Option to move open tickets to: New Sprint OR Backlog.

## Verification Steps
1. Create a sprint "Sprint 1".
2. Start "Sprint 1". Verify status is 'active'.
3. Try to start "Sprint 2". Verify error/warning.
4. Complete "Sprint 1". Move items to Backlog. Verify "Sprint 1" is 'completed'.

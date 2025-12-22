# 2. User Flows

## Creating and Moving a Task

```mermaid
sequenceDiagram
    participant User
    participant UI as Board UI
    participant Store as LocalStore

    User->>UI: Click "Add Card" in "Todo"
    UI->>User: Show Input Field
    User->>UI: Type "Fix Login Bug" + Enter
    UI->>Store: Save new Card object
    Store-->>UI: Return success
    UI->>User: Render new Card in "Todo" column
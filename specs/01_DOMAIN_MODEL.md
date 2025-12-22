# Domain Model

## Core Types

### Ticket
Represents a task or unit of work.
```typescript
interface Ticket {
  id: string;            // Unique identifier (e.g., "TKT-101")
  title: string;         // Short summary
  description: string;   // Markdown content
  type: TicketType;      // 'story' | 'bug' | 'task'
  statusId: string;      // ID of the Column it currently resides in
  sprintId?: string;     // ID of the Sprint (null if backlog)
  assigneeId?: string;   // ID of the User assigned
  priority: 'low' | 'medium' | 'high' | 'critical';
  parentId?: string;     // ID of parent ticket (for subtasks/epics)
  childrenIds?: string[]; // IDs of child tickets
  attachments?: Attachment[];
  createdAt: string;     // ISO Date
  updatedAt: string;     // ISO Date
}

export interface Attachment {
  id: string;
  name: string;
  url: string;
  type: 'image' | 'pdf' | 'text' | 'other';
  size: number; // in bytes
}
```

### TicketType
```typescript
type TicketType = 'story' | 'bug' | 'task';
```

### BoardColumn
Represents a vertical column on the Kanban board.
```typescript
interface BoardColumn {
  id: string;            // Unique identifier (e.g., "col-todo")
  title: string;         // Display name (e.g., "To Do")
  order: number;         // Visual sorting order (0, 1, 2...)
  limit?: number;        // Optional WIP limit
}
```

### Sprint
Represents a time-boxed iteration.
```typescript
interface Sprint {
  id: string;            // Unique identifier
  name: string;          // e.g., "Sprint 23"
  goal?: string;         // Optional sprint goal
  startDate: string;     // ISO Date
  endDate: string;       // ISO Date
  status: SprintStatus;  // 'planned' | 'active' | 'completed'
}
```

### SprintStatus
```typescript
type SprintStatus = 'planned' | 'active' | 'completed';
```

### User
Represents a team member.
```typescript
interface User {
  id: string;
  name: string;
  avatarUrl?: string;
  email: string;
}
```

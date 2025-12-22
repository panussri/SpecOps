# 1. Data Model (TypeScript Interfaces)

## Core Entities

```typescript
type Status = 'todo' | 'in-progress' | 'review' | 'done';

interface Board {
  id: string;
  title: string;
  columns: Column[];
}

interface Column {
  id: string;
  title: string;
  status: Status; // Mapped status
  cardIds: string[]; // Order of cards
}

interface Card {
  id: string;
  title: string;
  description?: string;
  tags: string[];
  assigneeId?: string;
  createdAt: string; // ISO Date
}

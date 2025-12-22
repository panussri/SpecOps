# Product Context

## Vision
**SpecOps** is a streamlined, high-performance Kanban board designed for development teams who reject the complexity of enterprise tools like Jira but demand more power than Trello. It focuses purely on the "Shipping Code" lifecycle: Planning, Board Management, and Sprints.

**Core Philosophy:**
- **Zero Config**: It works out of the box. Opinionated but sensible defaults.
- **Premium Feel**: Glassmorphism, fluid 60fps animations, instant interactions.
- **Developer First**: Keyboard shortcuts, markdown support, strict typing.

---

## Architecture & Tech Stack

### Frontend Core
- **Framework**: [React 18+](https://react.dev/) with [Vite](https://vitejs.dev/)
- **Language**: [TypeScript](https://www.typescriptlang.org/) (Strict Mode enabled)
- **Styling**: [TailwindCSS v3](https://tailwindcss.com/) (using `prettier-plugin-tailwindcss`)
- **State Management**: [Zustand](https://github.com/pmndrs/zustand)
  - Selected for its minimal boilerplate and ability to easily segregate stores (e.g., `useTicketStore`, `useBoardStore`).

### UI Component Layer
- **Headless UI**: [Radix UI](https://www.radix-ui.com/) (Primitives for Dialogs, Popovers, Dropdowns)
- **Component Library**: [shadcn/ui](https://ui.shadcn.com/) (Copy-paste base components)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Drag & Drop**: [dnd-kit](https://dndkit.com/) (Modern, accessible, lightweight)

### Forms & Validation
- **Forms**: [React Hook Form](https://react-hook-form.com/)
- **Schema Validation**: [Zod](https://zod.dev/)
  - Used for both form validation and runtime data validation.

### Data Persistence (Phased)
- **Phase 1 (MVP)**: LocalStorage + Mock Data.
  - Architecture must decouple the UI from the data source using a "Service Pattern" or separate API hooks layer, allowing an easy swap to a backend later.
- **Phase 2**: Supabase (PostgreSQL + Realtime).

---

## Project Structure

The project follows a "Feature-Based" architecture to keep related code colocated.

```text
src/
├── assets/             # Static assets (images, global css)
├── components/
│   ├── ui/             # Generic UI components (Button, Input, Dialog) - mostly shadcn
│   └── layout/         # Application shells (Sidebar, Navbar)
├── config/             # Environment variables, constants
├── features/           # Feature-based modules
│   ├── board/          # FEAT-001: Kanban Board
│   │   ├── components/ # Board-specific components (Column, TicketCard)
│   │   └── stores/     # Board state
│   ├── tickets/        # FEAT-004: Ticket Creation/Management
│   │   ├── components/ # (CreateTicketModal)
│   │   └── types/      # Feature-specific types
│   └── sprints/        # Sprint management
├── hooks/              # Global shared hooks (useTheme, useLocalStorage)
├── lib/                # Utilities (cn, date formatting)
├── types/              # Global domain types (syncs with 01_DOMAIN_MODEL.md)
└── main.tsx            # Entry point
```

---

## Coding Standards

### 1. TypeScript Strictness
- **No `any`**. Use `unknown` if necessary, but prefer strict unions.
- **Type Sharing**: Domain entities (`Ticket`, `User`, `Sprint`) must be imported from `@/types` (which reflects `specs/01_DOMAIN_MODEL.md`).

### 2. Component Design
- **Functional Components** only.
- **Composition over Inheritance**: Use props and children.
- **Tailwind Classes**: Use the `cn()` utility for class merging.

### 3. Documentation "Spec-Driven Development"
- **Golden Rule**: Code must implement the Spec. If the code requires a change in logic, **update the Spec first**, then the code.
- **ID Referencing**: Comments should reference Story IDs where complex logic exists.
  ```typescript
  // STY-001-B: Handle cross-column drag and drop
  const handleDragEnd = (...) => { ... }
  ```

---

## Development Workflow
1.  **Pick a Story**: Select a `STY-XXX` from the specs.
2.  **Implementation**:
    - Create/Update types in `src/types`.
    - Build UI Components in `components/ui` or `features/.../components`.
    - Implement Logic/State.
3.  **Verification**:
    - Verify against rules in `PROJECT_CONTEXT` and the specific Feature Spec.

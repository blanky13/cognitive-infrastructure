# System Architecture

The architecture separates capture, storage, processing, execution, and recovery so that a thought does not need to remain active in cognition merely because it has not yet been processed.

## Pipeline

```mermaid
flowchart TD
    A[Thought / Task / Interruption] --> B[Capture]
    B --> C[Persist]
    C --> D[Normalize / Clarify]
    D --> E[Classify]
    E --> F[Task Queue]
    E --> G[Knowledge Store]
    E --> H[Idea Parking Lot]
    E --> I[Decision Log]
    F --> J[Active Work]
    J --> K[Checkpoint]
    K --> J
    J --> L[Complete / Archive]
    H --> M[Periodic Review]
    G --> N[Future Retrieval]
```

## System layers

| Layer | Purpose | Typical implementation |
| --- | --- | --- |
| Capture | Accept thoughts with minimal friction | Quick note, voice note, inbox |
| Persistence | Prevent loss before organization | Notes database, task inbox, file |
| Processing | Clarify and classify | Manual review or automation |
| Task queue | Hold executable work | Task manager / backlog |
| Knowledge store | Hold reference material | Notes / document repository |
| Idea parking lot | Hold non-active ideas | Separate reviewable list |
| Active work | Current execution context | One primary workstream |
| Context checkpoint | Preserve resumption state | Structured note |
| Review | Reconcile queues and stale state | Periodic review |
| Archive | Remove completed or obsolete state | Archive / cold storage |

## State model

```text
CAPTURED
   ↓
PERSISTED
   ↓
CLARIFIED
   ↓
CLASSIFIED
   ├── TASK → QUEUED → ACTIVE → CHECKPOINTED → COMPLETE
   ├── REFERENCE → KNOWLEDGE
   ├── IDEA → PARKED → REVIEWED
   └── DECISION → DECISION LOG
```

## Context packet

The context packet should answer:

> “If I return to this later, what do I need to know to continue without reconstructing the whole task?”

Keep it compact. Optimize for **cheap resumption**, not exhaustive documentation.

## Reliability patterns

### Idempotency
Repeated captures should not automatically create repeated work. Detect duplicates and merge them where appropriate.

### Rate limiting
Limit notifications and incoming requests when they repeatedly interrupt active work.

### Backpressure
If capture or review backlog grows beyond what can reasonably be processed, simplify the system and defer nonessential processing.

### Queue aging
Review parked items periodically. Old items can be clarified, scheduled, merged, or archived.

### Checkpointing
Checkpoint frequency should reflect interruption risk and task complexity. There is no universal timer that works for every task.

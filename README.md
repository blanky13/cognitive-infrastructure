# Cognitive Infrastructure

A practical framework for externalizing cognitive state, reducing working-memory load, preserving context, and recovering from interruptions.

The project uses distributed-systems concepts as **design metaphors** for building a personal system that is easier to capture into, easier to resume, and harder to lose state from. It is ADHD-informed, but intended to be useful wherever attention, working memory, interruptions, or task initiation create friction.

## Core idea

Do not rely on active cognition to hold everything required for future action.

**capture → persist → clarify → route → execute → checkpoint → recover → review**

## Architecture

```mermaid
flowchart TD
    A[Thought / Task / Interruption] --> B[Capture]
    B --> C[Durable Externalization]
    C --> D[Clarify / Classify]
    D --> E{Type}
    E -->|Task| F[Task Queue]
    E -->|Reference| G[Knowledge Store]
    E -->|Idea| H[Idea Parking Lot]
    E -->|Decision| I[Decision Log]
    F --> J[Active Work]
    J --> K[Context Checkpoint]
    K --> J
    J --> L[Complete / Archive]
    F --> M[Recovery]
    M --> J
    G --> N[Future Retrieval]
    H --> O[Periodic Review]
```

## Design principles

1. **Externalize state** — move nonessential information out of the active cognitive workspace.
2. **Capture before organizing** — capture should be faster than organization.
3. **Persist before processing** — preserve information before cleaning or classifying it.
4. **Keep active work small** — limit simultaneous execution rather than assuming a fixed biological slot count.
5. **Make resumption explicit** — use a compact context packet.
6. **Park, do not suppress** — defer competing ideas into a reviewable location.
7. **Design for recovery** — interruptions and disrupted routines are normal conditions.
8. **Keep the infrastructure cheap** — the system must not become another project to maintain.

## Repository

- [Cognitive mechanics](docs/01-cognitive-mechanics.md)
- [System architecture](docs/02-system-architecture.md)
- [Core principles](docs/03-core-system-principles.md)
- [Cloud mapping](docs/04-cloud-infrastructure-mapping.md)
- [Workflows and patterns](docs/05-system-workflows-and-patterns.md)
- [Deployment roadmap](docs/06-deployment-roadmap.md)
- [Templates](templates/)
- [Example](examples/project-resumption.md)

## Scope and limitations

This is an engineering-inspired cognitive support framework, not a clinical model or treatment.

Cloud terminology is intentionally metaphorical. AWS services and distributed-systems behavior should not be read as literal descriptions of how the brain works. Individual cognitive profiles vary; the system should be adapted based on observed friction rather than rigid rules.

## License

MIT

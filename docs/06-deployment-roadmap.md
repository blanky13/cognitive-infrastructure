# Deployment Roadmap

The system should be deployed incrementally. The first stage should solve the cognitive bottleneck before automation is added.

## Stage 1 — Minimum viable system
Implement:
- one frictionless capture inbox;
- one task queue;
- one context-checkpoint template;
- one regular review point.

**Success condition:** important thoughts can leave active cognition without being lost, and active work can be resumed from a checkpoint.

## Stage 2 — Reliable operating loop
Add:
- explicit task states;
- an idea parking lot;
- duplicate cleanup;
- archive rules;
- interruption-aware checkpointing.

**Success condition:** the system remains usable after interruptions and disrupted routines.

## Stage 3 — Automation
Only automate repetitive processing such as:
- voice transcription;
- capture normalization;
- duplicate detection;
- classification;
- reminders;
- archive suggestions.

Automation should reduce friction rather than create another interface to maintain.

## Stage 4 — Measurement
Track a small set of operational metrics:

| Metric | What it tells you |
| --- | --- |
| Capture latency | How easy it is to externalize information |
| Capture-to-action conversion | Whether captured items become useful actions |
| Active task count | Whether the active workset is becoming overloaded |
| Stale queue count | Whether backlog is accumulating |
| Backlog age | How long deferred work remains unresolved |
| Recovery time | How quickly work resumes after disruption |
| Resumption success rate | Whether checkpoints contain enough information |

These metrics describe system behavior. They are not clinical measurements.

## Failure conditions
- Capture tool becomes unavailable.
- Review backlog becomes overwhelming.
- Notifications flood the active workstream.
- Automation creates duplicate or incorrect tasks.
- Checkpoints become too detailed to maintain.
- Task decomposition creates excessive overhead.
- Maintaining the system becomes a substitute for doing the work.

## Operating rule
Start with the smallest system that reliably preserves state.

Add infrastructure only when a repeated failure mode justifies it.

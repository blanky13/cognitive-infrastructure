# Cognitive Mechanics

This project starts with a simple constraint: active cognition has limited capacity, while external storage is much larger and more persistent.

The goal is not to model the brain as a computer. The goal is to identify cognitive bottlenecks and design external supports around them.

## Working memory

Working memory is the limited mental workspace used to temporarily maintain and manipulate information during ongoing activity. Capacity is constrained and depends on factors such as task complexity, attention, prior knowledge, and interference.

A useful engineering interpretation is:

> Keep the active working set small and move nonessential state into durable external storage.

This does **not** require assuming a universal number of working-memory slots.

## Attention and control

Attention determines what receives processing priority. Interruptions, notifications, competing thoughts, and environmental cues can compete for limited control.

The system therefore treats attention as a routing problem:

- choose what is active;
- defer what is not active;
- make deferred material recoverable;
- reduce unnecessary interrupts.

## Externalization

Writing, recording, reminders, checklists, and other external representations can reduce the need to retain information internally.

The important distinction is:

- **Working memory:** active cognitive workspace.
- **External memory:** durable representation outside that workspace.
- **Context packet:** the minimum state needed to resume an activity.

## Interruptions and context restoration

An interruption can leave the original task partially specified. If the next action, open questions, or relevant resources are no longer obvious, resumption requires reconstruction.

The system addresses this with checkpointing.

A useful checkpoint records the objective, current state, last completed action, next physical action, blockers, open questions, resources, and important decisions.

## ADHD-informed design

ADHD can involve difficulties with attention regulation, inhibition, working memory, planning, time management, and task initiation, but presentation varies substantially between people.

This project therefore does not treat ADHD as a single cognitive architecture or reduce it to an “interest/dopamine priority queue.” ADHD is treated as an important design case for systems that reduce initiation friction, preserve state across interruptions, reduce unnecessary context switching, and support recovery after disrupted routines.

## Analogy ≠ mechanism

A systems analogy can be useful without being scientifically equivalent.

A cache analogy illustrates volatile active state; a queue illustrates deferred work; checkpointing illustrates resumability; rate limiting illustrates interrupt control.

These are design tools, not claims that corresponding AWS services or software mechanisms exist inside the brain.

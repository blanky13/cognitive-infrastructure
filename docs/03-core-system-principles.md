# Core System Principles

## 1. Externalize before competition
If a thought is important but not relevant to the current action, capture it rather than repeatedly holding it in mind.

## 2. Separate capture from organization
Capture should be fast. Classification, cleanup, tagging, and prioritization can happen later.

## 3. Persist before processing
The first requirement is preservation. Organization is a second-stage concern.

## 4. Maintain a small active workset
Use one primary execution thread when possible. Additional information should support that thread rather than silently becoming parallel work.

This is a design constraint, not a claim about the number of things a person can biologically hold in working memory.

## 5. Make the next action physical
“Work on report” is an objective. “Open the report and draft the introduction” is an executable next action.

When initiation fails, reduce ambiguity before increasing effort.

## 6. Checkpoint before switching
When leaving an interruptible task, record enough state to resume without reconstructing the task.

## 7. Park competing work
A distracting idea is not a failed message. It is simply work that is not currently active.

Use a parking lot, backlog, or queue. A **dead-letter queue is not the default analogy**, because DLQs are specifically designed for messages that failed processing.

## 8. Recover instead of catching up
After disruption, do not attempt to replay every missed item immediately.

Reconcile the system, remove stale work, select the next useful action, and resume.

## 9. Minimize maintenance
If operating the system requires substantial effort, the infrastructure is competing with the work it was designed to support.

## 10. Measure system behavior
Useful operational metrics include capture latency, capture-to-action conversion, active task count, stale queue count, backlog age, interruption count, recovery time, and resumption success rate.

These are system metrics, not clinical measurements.

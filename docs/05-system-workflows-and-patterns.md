# System Workflows and Patterns

## Pattern 1: Quick capture
**Problem:** A thought competes with the current task because it has not been recorded.

**Procedure:**
1. Capture the raw thought in the fastest available channel.
2. Do not require full metadata.
3. Return to the active task.
4. Process the capture during review.

**Goal:** preserve information without turning capture into another task.

## Pattern 2: Context checkpoint
**Problem:** An interruption makes the original task expensive to reconstruct.

```text
Project:
Objective:
Current state:
Last completed action:
Next physical action:
Open questions:
Blockers:
Relevant files / links:
Important decisions:
```

Write the smallest useful version.

## Pattern 3: Interruption recovery
1. Read the checkpoint.
2. Confirm the objective.
3. Perform the recorded next action.
4. Update the checkpoint if state changed.
5. Resume normal execution.

Do not rebuild the entire project history unless required.

## Pattern 4: Task-paralysis recovery
When the task becomes too ambiguous, large, or effortful to initiate:
1. State the desired outcome.
2. Remove unnecessary choices.
3. Define the smallest observable next action.
4. Reduce scope if needed.
5. Start from the prepared state.
6. Reassess after execution begins.

The system does not depend on a universal “two-minute” or “three-minute” threshold.

## Pattern 5: Distraction parking
```text
CAPTURE → PARK → RETURN → REVIEW LATER
```

The parking lot should be persistent and easy to review.

## Pattern 6: Duplicate suppression
```text
new capture → compare → merge / discard duplicate → retain canonical task
```

The goal is idempotent work, not perfect automated deduplication.

## Pattern 7: Missed-day recovery
1. Open the capture inbox and task queue.
2. Remove or archive stale items.
3. Merge duplicates.
4. Identify current commitments.
5. Select one primary workstream.
6. Create a fresh context checkpoint.
7. Resume from the next physical action.

Do not turn backlog reconciliation into a requirement to complete everything that was missed.

## Pattern 8: Review debt
A capture system that is never reviewed becomes storage without retrieval.

During review, each item should be actionable, scheduled, parked, merged, converted to reference, or archived.

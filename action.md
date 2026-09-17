# Action Type

**Action = an executable operation that changes a state, produces an effect, or requests an external effect.**

Action is the type of **DO** in the TYPE model.

## Structure

```yaml
type: Action
name: action_name
description: what the action does

input:
  - InputType

output:
  - OutputType

preconditions:
  - condition

effects:
  - state change

permissions:
  - required permission
```

## Examples

```text
Generate
Evaluate
Create
Update
Delete
Publish
Deploy
Review
Notify
```

An Action is a definition, not an execution instance.

```text
Action Type
    ↓
Action Instance
    ↓
Execution
    ↓
Effect
```

## Action and Agent

```text
Agent
  ↓ executes
Action
  ↓ produces
Effect / Output
```

An Agent is the execution subject; an Action is the operation being executed.

## Action and Work

```text
WorkType
  ↓
Task
  ↓
Action Instance
  ↓
Effect
```

A WorkType describes a unit of work, while Action describes an executable operation inside that work.

## Action and Workflow

```text
Workflow
  ↓ selects / sequences
Action
  ↓ transforms
State
```

> **Action = what is done.**

> **Workflow = how actions are sequenced and transitioned.**

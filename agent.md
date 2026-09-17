# Agent Type

**Agent = an execution主体 that observes context, reasons, decides, and executes work through actions.**

Agent is the type of **WHO / executor** in the TYPE model.

## Structure

```yaml
type: Agent
name: agent_name
description: what the agent is responsible for

input:
  - Request
  - Context

cognition:
  - Observe
  - Reason
  - Decide

work:
  - WorkType

actions:
  - ActionType

output:
  - OutputType

constraints:
  - constraint

permissions:
  - permission
```

## Core model

```text
Request
   ↓
Agent
   ├── Observe
   ├── Reason
   ├── Decide
   └── Execute
          ↓
       Action
          ↓
       Effect
          ↓
       Output / State
```

## Agent is a Type

An Agent definition describes a class of execution主体. A concrete running agent is an instance.

```text
Agent Type
    ↓
Agent Instance
    ↓
Observation
    ↓
Decision
    ↓
Action Instance
    ↓
Result
```

## Agent and Action

```text
Agent = who / what executes
Action = what is executed
```

The Agent may select an Action based on its cognition, available capabilities, permissions, context, and current work.

## Agent and Work

```text
WorkType
    ↓
Task
    ↓
Agent
    ↓
Action
    ↓
Output
```

Work describes the objective-oriented unit of work. Action describes the executable operation. Agent describes the executor.

## Agent and Workflow

```text
Agent
  ↓ operates
Workflow
  ↓ sequences
Action
  ↓ changes
State
```

A workflow may be executed by one Agent or coordinated across multiple Agents.

## Capability and Permission

```text
Capability   = can do
Permission   = is allowed to do
Authorization = may do now
```

An Agent should execute an Action only when the required capability and authorization conditions are satisfied.

## Examples

```text
ResearchAgent
CodingAgent
ReviewAgent
PMAgent
OperationAgent
MonetizationAgent
```

These are specialized Agent Types. Their concrete responsibilities, cognition, work types, actions, tools, and permissions may differ.

> **Agent = execution主体 that turns cognition and work into actions.**

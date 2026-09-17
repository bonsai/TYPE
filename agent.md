# Agent Type

**Agent = an operational entity that arrives in an environment, senses it, acts upon it, and improves the environment.**

An Agent is an entity that exists within an environment, senses its state, interprets what it senses, decides what to do, and acts through interfaces to change the environment.

Agent is the type of **WHO / executor** in the TYPE model.

## Core Definition

```text
Environment
    ↓
  Sensing
    ↓
Observation
    ↓
Cognition
    ↓
Decision
    ↓
Action
    ↓
Environment Change
    ↓
Improved / Updated Environment
    ↺
```

The essential Agent loop is:

**降り立つ → 感知する → 認識する → 判断する → 働きかける → 環境を改善する**

## Structure

```yaml
type: Agent
name: agent_name
description: what the agent is responsible for

environment:
  - Environment

input:
  - Request
  - Context
  - Observation

cognition:
  - Observe
  - Reason
  - Decide

actions:
  - ActionType

output:
  - OutputType
  - StateChange

constraints:
  - constraint

permissions:
  - permission
```

## Agent and Environment

An Agent does not merely execute an externally assigned operation. It exists **within an environment**, senses its current state, and acts to change that state.

```text
Agent × Environment
        ↓
     Sensing
        ↓
    Cognition
        ↓
      Action
        ↓
Environment Change
```

The environment may be physical, digital, social, organizational, or computational.

Examples:

```text
Human       ↔ Physical Environment
Robot       ↔ Physical Environment
Developer   ↔ Software Environment
Researcher  ↔ Knowledge Environment
AI Agent    ↔ Digital / Information Environment
PMAgent     ↔ Project Environment
```

## Agent is a Type

An Agent definition describes a class of operational entities. A concrete running agent is an instance.

```text
Agent Type
    ↓
Agent Instance
    ↓
Environment
    ↓
Observation
    ↓
Decision
    ↓
Action Instance
    ↓
Environment Change
```

## Agent and Action

```text
Agent = who / what acts
Action = what is done
```

The Agent selects and executes Actions according to its cognition, capabilities, permissions, context, and current work.

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
Output / State Change
```

Work describes the objective-oriented unit of work. Action describes the executable operation. Agent describes the operational entity that performs it.

## Agent and Interface

An Agent interacts with its environment through **Interfaces**.

```text
Agent
  ↓
Interface
  ↓
Environment
```

The interface may be physical or digital:

```text
Eye       ↔ Light / Air
Ear       ↔ Sound / Air
Voice     ↔ Air
Keyboard  ↔ Computer
API       ↔ Software
Agent     ↔ Agent
```

An Agent's ability to improve an environment depends on what it can sense, understand, and act through.

## Capability and Permission

```text
Capability    = can do
Permission    = is allowed to do
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
RobotAgent
```

These are specialized Agent Types. Their environments, sensing capabilities, cognition, work types, actions, interfaces, tools, and permissions may differ.

> **Agent = an operational entity that arrives in an environment, senses it, acts upon it, and improves the environment.**

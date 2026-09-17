# TYPE

**TYPE = a system of elastic categories for describing what something is, how it is structured, how it relates, how it operates, and how it participates in interaction.**

TYPE is not merely a programming-language type system. It is a vocabulary and structural framework for modeling a world of things, subjects, actions, data, work, relations, and interactions.

## Definition

> **Type（タイプ）とは、対象を捉えるための類型である。**

A Type is a category, not a fixed boundary. Its granularity is **elastic**: a Type can be abstracted, specialized, composed, or decomposed according to purpose and context.

```text
Type
  ↓
Family
  ↓
Type
  ↓
Sub-Type
  ↓
Instance
```

The same thing may be represented at different Type granularities depending on what is being observed or operated on.

## Type Families

TYPE contains multiple families rather than one flat classification.

```text
TYPE
├── Entity        person, organization, place, product, concept
├── Subject       human, agent, organization, actor
├── Object        physical or digital object
├── Environment   physical, digital, social, operational context
├── State         condition, configuration, knowledge state
├── Event         something that happens or changes state
├── Action        executable operation
├── Agent         operational subject
├── Data          values, records, documents, datasets
├── Request       question, command, instruction, demand
├── Work          research, build, fix, design, review
├── Cognition     observe, identify, classify, compare, infer, decide
├── Relation      semantic connection between Types
├── Interface     boundary through which Types interact
├── Protocol      structured rules for interaction
└── Output        answer, report, dataset, code, document, decision
```

Families are not mutually exclusive in every model. A concrete Type can participate in multiple structures and relations.

## Elastic Granularity

Type granularity changes with the modeling purpose.

```text
Agent
  ↓
AI Agent
  ↓
Research Agent
  ↓
Architecture Research Agent
  ↓
Specific Agent Instance
```

Or the abstraction may move in the opposite direction:

```text
Specific Tool
  ↓
Tool
  ↓
Object
  ↓
Entity
```

> **Type is a family-based, elastic classification rather than a rigid taxonomy.**

## Type, Ontology, and Topology

TYPE provides the categories. **Ontology** defines what those categories mean and how concepts are semantically related. **Topology** describes the structural arrangement and connectivity of those Types.

```text
TYPE
 │
 ├── Ontology
 │     └── meaning / concept / relation
 │
 └── Topology
       └── position / connectivity / structure
```

### Ontology

Ontology answers:

```text
What exists?
What kind of thing is it?
What properties does it have?
What is it related to?
What does the relation mean?
```

```text
Agent ──acts_on──> Environment
Agent ──performs──> Action
Action ──causes──> Event
Event ──changes──> State
```

### Topology

Topology answers:

```text
What is connected?
What is adjacent?
What is inside or outside?
What is upstream or downstream?
How does structure change while connectivity is preserved?
```

Topology can therefore represent the arrangement of a system independently from the semantic meaning assigned by its ontology.

```text
Topology
A ─ B ─ C
    │
    D
```

The same topology may be populated by different Types, while the same Type may appear in different topologies.

## Type and Structure

A Type can be described through several structural dimensions.

```text
Type
├── Identity      what it is
├── Structure     what it contains
├── Property      what it has
├── Constraint    what is allowed
├── Relation      what it connects to
├── Operation     what it can do
├── Transition    how it changes
└── Interface     how it interacts
```

## Type and Operand

**Operand is also a Type-level concept.**

An operand is a value, object, or input that an operation acts upon. It should not be confused with the operation itself.

```text
Operation
   ↓
Operator
   ↓
Operand
   ↓
Result
```

For example:

```text
add
 ├── operand: 1
 ├── operand: 2
 └── result: 3
```

At a higher level:

```text
Action
 ├── Operator / operation
 ├── Operand(s)
 ├── Context
 └── Effect / Output
```

This allows TYPE to describe both **what acts** and **what is acted upon**.

```text
Agent      = who / what acts
Action     = what is done
Operand    = what the operation acts upon
Output     = what is produced
```

## Type and Interface

An Interface is a Type boundary or interaction surface through which different Types exchange information, effects, or actions.

```text
Type A
  ↕
Interface
  ↕
Type B
```

Examples include:

```text
Human ↔ Interface ↔ Agent
Agent ↔ API ↔ Software
Display ↔ Interface ↔ Human
Agent ↔ Interface ↔ Agent
```

The Interface does not have to be a physical device. It may be an API, message format, command surface, language, protocol endpoint, or other interaction boundary.

## Type and Protocol

A **Protocol** structures interaction between Types through an Interface.

```text
Type A
  ↓
Interface
  ↓
Protocol
  ↓
Interaction
  ↓
State Change / Effect
```

A protocol can specify messages, ordering, constraints, roles, transitions, and expected effects.

Protocol granularity is also elastic:

```text
Protocol
  ↓
Interaction Protocol
  ↓
Agent Protocol
  ↓
Task Protocol
  ↓
Message / Action
```

Therefore:

> **Types are structured through Interfaces and can interact through elastic Protocols.**

## Agent as a Type

Agent belongs to the Agent family and represents an operational subject.

> **Agent is an operational entity that enters an environment, senses it, acts upon it, and improves or changes the environment.**

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
     ↺
```

An Agent interacts with the environment through Interfaces and Protocols.

```text
Environment
     ↕
 Interface
     ↕
   Agent
     ↕
 Interface
     ↕
   Agent
```

See [agent.md](agent.md).

## Type, Instance, and State

```text
Type
 ↓
Instance
 ↓
State
 ↓
Event
 ↓
New State
```

A Type describes a class of possible instances. An Instance is a concrete occurrence. State describes its current condition. Events explain state changes.

## Type and Workflow

A Workflow is a topology of typed work and transitions.

```text
Request
   ↓
Work
   ↓
Cognition
   ↓
Action
   ↓
Output
```

More explicitly:

```text
Request
   ↓
Work
   ↓
Agent
   ↓
Action
   ↓
Operand
   ↓
Effect
   ↓
State'
   ↓
Output
```

> **Workflow = a structured topology of typed transitions and interactions.**

## Type as a Modeling System

TYPE can be viewed through several complementary dimensions.

```text
                    TYPE
                     │
        ┌────────────┼────────────┐
        ↓            ↓            ↓
      Family      Ontology      Topology
        │            │            │
     classes       meaning     structure
        │            │            │
        └────────────┼────────────┘
                     ↓
                 Interface
                     ↓
                  Protocol
                     ↓
                 Operation
                     ↓
                  Operand
                     ↓
                   Effect
```

These dimensions answer different questions and should not be collapsed into one concept.

## JSON / YAML

TYPE is a conceptual system. JSON and YAML are representation formats used to formalize Type definitions and instances.

```text
TYPE
 ↓
Concept / Family
 ↓
Structure / Ontology / Topology
 ↓
JSON / YAML
 ↓
Machine-readable definition
 ↓
Implementation / Validation
```

Example:

```yaml
type: Agent
family: Agent
granularity: operational_subject

ontology:
  kind: operational_entity

structure:
  observes: Environment
  acts_through: Interface
  performs: Action

relations:
  - observes
  - acts_on
  - improves

protocols:
  - interaction

operations:
  - observe
  - decide
  - act
```

The format is replaceable; the Type concept is not tied to JSON or YAML.

## Core Vocabulary

```text
Family       = group of related Types
Type         = elastic category / classification
Instance     = concrete occurrence of a Type
Ontology     = semantic model of concepts and relations
Topology     = structural arrangement and connectivity
Structure    = composition of a Type
Relation     = semantic connection
Interface    = interaction boundary
Protocol     = rules and structure of interaction
Operation    = executable transformation
Operator     = operation that acts
Operand      = value/object acted upon
Action       = executable operation in a work context
Agent        = operational subject
State        = current condition
Event        = occurrence that changes or records State
Output       = produced result
```

## Principles

### 1. Type is a concept, not an instance

Type describes a class of possible things; an instance is a concrete occurrence.

### 2. Type is a family system

Types belong to families and may be composed across families.

### 3. Type granularity is elastic

A Type may be abstracted, specialized, decomposed, or composed according to purpose.

### 4. Ontology and topology are distinct

Ontology describes semantic meaning and relations. Topology describes structural arrangement and connectivity.

### 5. Interface connects Types

Different Types can interact through an Interface.

### 6. Protocol structures interaction

Interfaces become operationally meaningful through Protocols that structure exchanges, actions, and transitions.

### 7. Operand is part of the operation model

An operation has an operator and one or more operands, producing a result or effect.

### 8. JSON / YAML are representations

JSON and YAML express Type definitions; they are not the Type itself.

## One-line definition

> **TYPE is an elastic, family-based system of concepts for classifying, structuring, relating, connecting, and operating on things through ontology, topology, interfaces, protocols, operations, and operands.**

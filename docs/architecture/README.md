# Architecture

The Spearhead Platform follows a modular, event-driven architecture designed for long-term scalability and maintainability.

---

# Principles

- Modular Packages
- Event Driven
- Plugin First
- Cloud Native
- Type Safe
- API First
- Infrastructure as Code

---

# Documentation

## C4 Model

Located in:

```
docs/architecture/c4/
```

Includes:

- System Context
- Containers
- Components
- Deployment

---

## ADRs

Located in:

```
docs/architecture/decisions/
```

Architecture Decision Records document major design decisions.

---

## Diagrams

Located in:

```
docs/architecture/diagrams/
```

Contains:

- Event Flow
- Discord Bot
- Radio Pipeline
- Plugin System

---

# High-Level Architecture

```
                 Users
                    │
                    ▼
              Website / Admin
                    │
                    ▼
               REST API
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
    Discord     Radio      Dashboard
        │           │
        └──────┬────┘
               ▼
          Event Bus
               │
    ┌──────────┼──────────┐
    ▼          ▼          ▼
 Plugins    Scheduler   Metrics
               │
               ▼
          Infrastructure
```

---

# Core Packages

| Package | Purpose |
|----------|---------|
| core | Shared framework functionality |
| events | Event Bus |
| logger | Logging |
| config | Configuration |
| scheduler | Scheduled Jobs |
| telemetry | OpenTelemetry |
| media | Audio Metadata |
| platform | Application Bootstrap |

---

# Design Goals

- Loose coupling
- High cohesion
- Independent packages
- Extensible plugin model
- Horizontal scalability
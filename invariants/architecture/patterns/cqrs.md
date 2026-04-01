# CQRS
Reasoning: Separate read and write paths so each can be modeled and optimized for its own constraints.

```bash
jumbo invariant add --title "CQRS" --description "Separate write (events) and read (views) models. Read and write are separated by Command Query Responsibility Segregation" --enforcement "Code review"
```

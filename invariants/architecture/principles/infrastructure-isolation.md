# Infrastructure Isolation
Reasoning: Maintains clean architecture dependency rules and allows storage implementations to be swapped.

```bash
jumbo invariant add --title "Infrastructure Isolation" --description "Domain models must never contain infrastructure concerns like database IDs, sequence numbers, or file paths" --enforcement "Code review"
```

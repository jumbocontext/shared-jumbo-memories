# Avoid deep nesting — prefer early returns and guard clauses
Reasoning: Deep nesting forces readers to track multiple open conditions simultaneously, increasing cognitive load and the chance of logic errors.

```bash
jumbo invariant add --title "Avoid deep nesting — prefer early returns and guard clauses" --description "Limit nesting to no more than two or three levels. Validate preconditions at the top of a function and return or throw immediately when they are not met. This keeps the happy path unindented and obvious, and eliminates the need to trace matching braces to understand control flow." --enforcement "Code review"
```

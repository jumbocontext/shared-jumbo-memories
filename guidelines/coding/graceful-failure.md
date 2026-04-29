# Fail gracefully
Reasoning: How code behaves at its failure boundary is as important as how it behaves on the happy path. Unexpected errors that leak as raw stack traces or leave partial side-effects are harder to diagnose and erode trust in the system.

```bash
jumbo guideline add --category codingStyle --title "Fail gracefully" --description "When an operation cannot complete, fail explicitly: return or throw a well-typed error, surface a clear message to the caller or user, and leave no partial side-effects behind. Never let exceptions propagate as raw stack traces across a public boundary." --rationale "How code behaves at its failure boundary is as important as the happy path. Raw stack traces and partial side-effects are harder to diagnose and erode trust in the system."
```

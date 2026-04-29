# Decompose large units of work
Reasoning: Smaller units are easier to understand, test, and change than oversized protocols and sprawling test files.

```bash
jumbo invariant add --title "Decompose large units of work" --description "Don't have protocols that perform 10 categories of work that require test files that are 5000 lines long. Maintain a unit of work where possible and keep corresponding test file small."
```

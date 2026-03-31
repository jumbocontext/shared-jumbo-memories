# No magic strings - Use type inference where possible, constants where not
Reasoning: Reduces coupling, prevents inconsistent values, and turns widespread literal changes into a single edit.

```bash
jumbo invariant add --title "No magic strings - Use type inference where possible, constants where not" --description "Magic strings and numbers scattered through code create maintenance burdens. When flag names, numeric thresholds, or other literals appear in multiple places, changing them requires hunting through the entire codebase. Use type inference where possible. Where explicit values are needed, define them as named constants in a shared location."
```

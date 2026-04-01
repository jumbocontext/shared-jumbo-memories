# Prefer flags over positional arguments
Reasoning: Flags make intent explicit at the call site, are order-independent, and leave room to add new inputs later without breaking existing usage. Positional args make sense only for a small number of primary, well-understood inputs (e.g. `cp <source> <destination>`). Beyond that, they create ambiguity and make scripts harder to read.
Source: https://clig.dev/#arguments-and-flags

```bash
jumbo guideline add --category cli --title "Prefer flags over positional arguments" --description "Use named flags rather than positional arguments wherever possible. Flags make intent explicit at the call site, are order-independent, and make it easier to add new inputs in the future without breaking existing usage. Reserve positional args for a small number of primary, well-understood inputs." --rationale "Positional arguments become ambiguous as a command grows and make scripts harder to read at a glance. Flags are self-documenting and can be added or reordered without breaking existing callers."
```

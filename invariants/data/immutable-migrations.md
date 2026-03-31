# Never modify existing migration files
Reasoning: Modifying applied migrations causes checksum mismatches and can break both upgraded and fresh databases.

```bash
jumbo invariant add --title "Never modify existing migration files" --description "Existing migration files are immutable. To change schema, always add a new sequential migration file. Never edit a previously applied migration."
```

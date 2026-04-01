# Variable names must reflect their source
Reasoning: Preserving source concepts in names keeps code self-documenting and avoids needless mental translation.

```bash
jumbo guideline add --category codingStyle --title "Variable names must reflect their source" --description "When assigning a value to a variable, preserve the semantic meaning from the source. Do not introduce creative synonyms or arbitrary renamings. Example: const latestGoal = repository.getLatestGoal() (not const current = ...)" --rationale "Preserving source concepts in names keeps code self-documenting and avoids needless mental translation." --enforcement "Code review"
```

# No junk drawers
Reasoning: Clear domain boundaries improve discoverability and keep technical catch-alls from becoming architectural dumping grounds.

```bash
jumbo invariant add --title "No junk drawers" --description "NO services/, utils/, managers/, repositories/ catch-alls. Code should be organized by domain concept, not technical category" --enforcement "Code review"
```

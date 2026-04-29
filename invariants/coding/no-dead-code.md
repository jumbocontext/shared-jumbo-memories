# Delete dead code immediately
Reasoning: Dead code — unused functions, commented-out blocks, unreachable branches, obsolete variables — erodes trust in the codebase and raises the cost of every future read.

```bash
jumbo invariant add --title "Delete dead code immediately" --description "Remove unused functions, commented-out code blocks, unreachable branches, and obsolete variables as soon as they are identified. Version control preserves history; the repository is not an archive. Dead code in the codebase is noise that forces readers to question whether something is intentionally unused or just forgotten."
```

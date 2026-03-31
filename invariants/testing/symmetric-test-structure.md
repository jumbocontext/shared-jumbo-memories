# Test file names and namespaces must mirror src/ structure
Reasoning: Symmetric test layout makes tests immediately locatable from source and reinforces architectural boundaries.

```bash
jumbo invariant add --title "Test file names and namespaces must mirror src/ structure" --description "Test files in tests/ must follow the same directory structure and naming as their corresponding source files in src/. For example, src/application/goals/add/AddGoalCommandHandler.ts must have its test at tests/application/goals/add/AddGoalCommandHandler.test.ts. Namespace symmetry makes tests discoverable and reinforces architectural boundaries."
```

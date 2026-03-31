# Never pollute stdout with non-output content
Reasoning: Machine-readable output stops being reliable as soon as debug text or progress noise leaks into stdout.

```bash
jumbo invariant add --title "Never pollute stdout with non-output content" --description "When producing output for programmatic consumption (non-TTY, --format json, piped output), stdout MUST contain ONLY the final structured output. No debug statements, progress messages, warnings, or extraneous text."
```

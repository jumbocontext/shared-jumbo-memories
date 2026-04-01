# Send all diagnostics and logging to stderr
Reasoning: Keeping diagnostics on stderr preserves stdout for data and makes CLI output safer to pipe and automate.

```bash
jumbo invariant add --title "Send all diagnostics and logging to stderr" --description "All logging, debugging, warnings, progress indicators, and diagnostic output MUST use stderr (not stdout). Applies universally regardless of output format." --enforcement "Code review"
```

# JSON output must be exactly one complete payload
Reasoning: Automation can only trust JSON mode when commands emit exactly one complete payload and nothing else.

```bash
jumbo invariant add --title "JSON output must be exactly one complete payload" --description "When --format json is specified, stdout MUST contain exactly one complete valid JSON object. No fragments, no multiple objects, no streaming arrays unless NDJSON format."
```

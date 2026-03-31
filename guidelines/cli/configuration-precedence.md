# Configuration must follow a defined precedence order
Reasoning: When configuration can come from multiple sources, ambiguity about which one wins leads to confusing, hard-to-debug behaviour. A consistent, published order makes the tool predictable.
Source: https://clig.dev/#configuration

Apply configuration from highest to lowest precedence:

1. Flags (most specific, most intentional)
2. Environment variables
3. Project-level config (e.g. `.env`, `myapp.json` in the working directory)
4. User-level config (e.g. `~/.config/myapp`)
5. System-wide config (least specific)

```bash
jumbo guideline add --category cli --title "Configuration must follow a defined precedence order" --description "When configuration can come from multiple sources, apply it in this order (highest wins): flags, environment variables, project-level config, user-level config, system-wide config."
```

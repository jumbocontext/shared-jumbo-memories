# Always allow non-interactive use
Reasoning: A CLI that requires a TTY to function cannot be scripted, piped, or run in CI. Every prompt must have a flag equivalent. This is what separates a composable tool from one that only works for humans sitting at a terminal.
Source: https://clig.dev/#interactivity

```bash
jumbo guideline add --category other --title "Always allow non-interactive use" --description "Every interactive prompt must have a flag or argument equivalent. If stdin is not a terminal, skip prompting entirely and require those flags. If --no-input is passed, disable all prompts. Never require a TTY to run a command successfully." --rationale "A CLI that requires a TTY cannot be scripted, piped, or run in CI. Flag equivalents for every prompt are what separate a composable tool from one that only works for humans at a terminal."
```

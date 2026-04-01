# Confirm before dangerous operations
Reasoning: Destructive actions in a CLI are unforgiving. Calibrating the friction to the severity of the action protects users from accidents while keeping scripting possible.
Source: https://clig.dev/#arguments-and-flags

- **Mild** (e.g. delete a single file): a simple y/n prompt is sufficient, or skip confirmation if the command name already makes the action obvious.
- **Moderate** (e.g. delete a directory, modify a remote resource): prompt for confirmation and provide a `--dry-run` option so the user can preview what will happen.
- **Severe** (e.g. destroy an entire application or environment): require the user to type something non-trivial, such as the name of the resource being destroyed. Also accept `--confirm="resource-name"` so it remains scriptable.

```bash
jumbo guideline add --category other --title "Confirm before dangerous operations" --description "Calibrate confirmation friction to the severity of the action. Mild risk: a y/n prompt or none. Moderate risk: prompt and offer --dry-run. Severe risk: require typing the resource name, or passing --confirm=\"resource-name\" for scripted use." --rationale "Destructive actions in a CLI are unforgiving. Calibrating friction to severity protects users from accidents while keeping scripting possible." --enforcement "Code review"
```

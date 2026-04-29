# Names must be explicit and self-documenting
Reasoning: Clear naming distinguishes between command handlers that perform actions and event handlers that react, reducing confusion about responsibility and purpose.

```bash
jumbo invariant add --title "Names must be explicit and self-documenting" --description "A reader should understand what a class, file, or identifier does from its name alone—including its architectural role. Never require code inspection to decipher purpose. Examples: AddComponentCommandHandler (not AddComponentHandler), GoalProjectionStore (not GoalStore), SessionStartedEvent (not SessionStarted)."
```

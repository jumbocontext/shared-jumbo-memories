# Shared Jumbo Memories
A library of pluggable memories for rapidly priming a project with proven invariants, guidelines, and patterns.

## Contributing
Anyone can contribute. Just create a PR.

There are only two constraints:

1. Maintain the structure
2. One memory per file (to avoid conflicts and attribute contributors)

## Structure
- `invariants/` for non-negotiable rules
- `guidelines/` for recommended practices
- Each type uses one shallow category folder to keep browsing easy as the library grows

`architecture` is the deliberate exception: it spans enough distinct concerns that it supports one extra level of nesting (`patterns/`, `principles/`, `structure/`). No other category should nest deeper than one level.

Current categories:
- `architecture/` (invariants only)
  - `patterns/` — named design patterns (CQRS, Event Sourcing, …)
  - `principles/` — SOLID and derived rules
  - `structure/` — directory layout, layer naming, and organization conventions
- `cli`
- `coding`
- `data`
- `documentation`
- `process`
- `testing`

## How To Classify
Choose the category based on the primary reason someone would browse for the memory.

- `architecture`: boundaries, layering, composition, replaceability, design patterns, and structural principles. Sub-categorize into `patterns/`, `principles/`, or `structure/` based on the nature of the rule.
- `cli`: terminal behavior, stdout/stderr, flags, exit codes, interactivity, secrets handling, machine-readable output, command UX
- `coding`: naming, expression style, error handling, decomposition, and general code quality practices
- `data`: persistence, serialization, migrations, encoding, storage shape
- `documentation`: READMEs, web docs, and discoverability outside the tool itself
- `process`: workflow habits, cleanup, pre-implementation practices, and contributor conventions
- `testing`: test layout, coverage, and test maintenance expectations

If a memory could fit in multiple places, put it where a browser is most likely to look first. Keep the folder choice shallow and pragmatic. A future PR can always move a file if a better fit becomes obvious.

## Memory Template
Each memory should stay minimal:
- Reasoning
- `jumbo ... add` snippet

Example:

~~~md
# Names must be explicit and self-documenting
Reasoning: Clear naming keeps intent obvious without forcing readers to inspect implementation details.

```bash
jumbo invariant add --title "Names must be explicit and self-documenting" --description "A reader should understand what a class, file, or identifier does from its name alone—including its architectural role. Never require code inspection to decipher purpose. Examples: AddComponentCommandHandler (not AddComponentHandler), GoalProjectionStore (not GoalStore), SessionStartedEvent (not SessionStarted)."
```
~~~

## Memories
Browse by type, then category.

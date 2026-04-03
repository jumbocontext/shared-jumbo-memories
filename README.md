# Shared Jumbo Memories
A library of pluggable Jumbo memories for rapidly priming a project with proven invariants, guidelines, and patterns.

## Table of Contents
- [Memories](#memories)
- [Contributing](#contributing)
- [Structure](#structure)
- [How To Classify](#how-to-classify)
- [Memory Template](#memory-template)

## Memories

### Invariants
- architecture
  - patterns
    - [CQRS](invariants/architecture/patterns/cqrs.md)
    - [Event Sourcing](invariants/architecture/patterns/event-sourcing.md)
  - principles
    - [Common Closure Principle](invariants/architecture/principles/common-closure-principle.md)
    - [Dependency Inversion Principle](invariants/architecture/principles/dependency-inversion-principle.md)
    - [Infrastructure Isolation](invariants/architecture/principles/infrastructure-isolation.md)
    - [Interface Segregation Principle](invariants/architecture/principles/interface-segregation-principle.md)
    - [Law of Demeter](invariants/architecture/principles/law-of-demeter.md)
    - [Liskov Substitution Principle](invariants/architecture/principles/liskov-substitution-principle.md)
    - [Open-Closed Principle](invariants/architecture/principles/open-closed-principle.md)
    - [Infrastructure must be replaceable](invariants/architecture/principles/replaceable-infrastructure.md)
    - [Single Responsibility Principle](invariants/architecture/principles/single-responsibility-principle.md)
  - structure
    - [Clean Screaming Architecture](invariants/architecture/structure/clean-screaming-architecture.md)
    - [No junk drawers](invariants/architecture/structure/no-junk-drawers.md)
- cli
  - [JSON output must be exactly one complete payload](invariants/cli/json-output-completeness.md)
  - [Send all diagnostics and logging to stderr](invariants/cli/stderr-for-diagnostics.md)
  - [Never pollute stdout with non-output content](invariants/cli/stdout-purity.md)
- coding
  - [Avoid deep nesting — prefer early returns and guard clauses](invariants/coding/avoid-deep-nesting.md)
  - [Leave the code cleaner than you found it (Boy Scout Rule)](invariants/coding/boy-scout-rule.md)
  - [Comments must explain why, not what](invariants/coding/comments-explain-why.md)
  - [Decompose large units of work](invariants/coding/decompose-large-units-of-work.md)
  - [Don't Repeat Yourself (DRY)](invariants/coding/dry-no-duplication.md)
  - [Names must be explicit and self-documenting](invariants/coding/explicit-naming.md)
  - [Limit function argument count](invariants/coding/limit-function-arguments.md)
  - [No dead code — delete it immediately](invariants/coding/no-dead-code.md)
  - [No magic strings — use type inference where possible, constants where not](invariants/coding/no-magic-strings.md)
- data
  - [Never modify existing migration files](invariants/data/immutable-migrations.md)
  - [UTF-8 without BOM](invariants/data/utf-8-without-bom.md)
- testing
  - [Test file names and namespaces must mirror src/ structure](invariants/testing/symmetric-test-structure.md)

### Guidelines
- cli
  - [Always allow non-interactive use](guidelines/cli/always-allow-non-interactive-use.md)
  - [Configuration must follow a defined precedence order](guidelines/cli/configuration-precedence.md)
  - [Confirm before dangerous operations](guidelines/cli/confirm-before-dangerous-operations.md)
  - [CLI help must be discoverable](guidelines/cli/help-must-be-discoverable.md)
  - [Never read secrets from flags](guidelines/cli/never-read-secrets-from-flags.md)
  - [Prefer flags over positional arguments](guidelines/cli/prefer-flags-over-args.md)
- coding
  - [Fail gracefully](guidelines/coding/graceful-failure.md)
  - [Variable names must reflect their source](guidelines/coding/variable-names-reflect-their-source.md)
- process
  - [Clean up temporary artifacts](guidelines/process/clean-up-temporary-artifacts.md)
  - [Explore base classes before implementing derived classes](guidelines/process/explore-base-classes-first.md)
  - [Fix problems when encountered](guidelines/process/fix-problems-when-encountered.md)
- testing
  - [Unit test coverage required](guidelines/testing/unit-test-coverage-required.md)

## Contributing
Anyone can contribute. Just create a PR.

There are only two constraints:

1. Maintain the structure
2. One memory per file (to avoid conflicts and attribute contributors)

## Structure
- invariants/ for non-negotiable rules
- guidelines/ for recommended practices
- Each type uses one shallow category folder to keep browsing easy as the library grows

architecture is the deliberate exception: it spans enough distinct concerns that it supports one extra level of nesting (patterns/, principles/, structure/). No other category should nest deeper than one level.

Current categories:
- architecture/ (invariants only)
  - patterns/ — named design patterns (CQRS, Event Sourcing, …)
  - principles/ — SOLID and derived rules
  - structure/ — directory layout, layer naming, and organization conventions
- cli
- coding
- data
- documentation
- process
- testing

## How To Classify
Choose the category based on the primary reason someone would browse for the memory.

- architecture: boundaries, layering, composition, replaceability, design patterns, and structural principles. Sub-categorize into patterns/, principles/, or structure/ based on the nature of the rule.
- cli: terminal behavior, stdout/stderr, flags, exit codes, interactivity, secrets handling, machine-readable output, command UX
- coding: naming, expression style, error handling, decomposition, and general code quality practices
- data: persistence, serialization, migrations, encoding, storage shape
- documentation: READMEs, web docs, and discoverability outside the tool itself
- process: workflow habits, cleanup, pre-implementation practices, and contributor conventions
- testing: test layout, coverage, and test maintenance expectations

If a memory could fit in multiple places, put it where a browser is most likely to look first. Keep the folder choice shallow and pragmatic. A future PR can always move a file if a better fit becomes obvious.

## Memory Template
Each memory should stay minimal:
- Reasoning
- jumbo ... add snippet

Example:

~~~md
# Names must be explicit and self-documenting
Reasoning: Clear naming keeps intent obvious without forcing readers to inspect implementation details.

bash
jumbo invariant add --title "Names must be explicit and self-documenting" --description "A reader should understand what a class, file, or identifier does from its name alone—including its architectural role. Never require code inspection to decipher purpose. Examples: AddComponentCommandHandler (not AddComponentHandler), GoalProjectionStore (not GoalStore), SessionStartedEvent (not SessionStarted)."

~~~

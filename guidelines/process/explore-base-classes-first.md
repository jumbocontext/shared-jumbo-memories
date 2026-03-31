# Explore base classes before implementing derived classes
Reasoning: Misunderstanding a base contract leads to implementations that compile but still violate the intended pattern.

```bash
jumbo guideline add --category codingStyle --title "Explore base classes before implementing derived classes" --description "Before implementing a class that extends or depends on a base class/interface, read the base class implementation to understand its contract, usage patterns, and internal mechanics. Look for existing implementations as reference examples. Never assume behavior based on method names alone - verify the implementation."
```

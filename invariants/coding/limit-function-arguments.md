# Limit function argument count
Reasoning: Every additional parameter increases the number of combinations a caller must reason about and the number of test cases required for full coverage.

```bash
jumbo invariant add --title "Limit function argument count" --description "Functions should take as few parameters as possible. Niladic (zero) is ideal. Monadic (one) and dyadic (two) are normal. Triadic (three) requires justification. More than three is a strong signal the function is doing too much or that the parameters should be grouped into a dedicated parameter object or value type." --enforcement "Code review"
```

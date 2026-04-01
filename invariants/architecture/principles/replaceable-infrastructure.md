# Infrastructure must be replaceable
Reasoning: Treating infrastructure as a replaceable detail keeps core policy insulated from technology churn.

```bash
jumbo invariant add --title "Infrastructure must be replaceable" --description "Any infrastructure component must be replaceable with an alternative implementation without modifying code in presentation, application, or domain layers." --enforcement "Code review"
```

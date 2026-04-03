# Law of Demeter
Reasoning: Reaching into the internals of objects returned by other objects creates tight coupling chains that break whenever an intermediate object's structure changes.

```bash
jumbo invariant add --title "Law of Demeter" --description "A module should only invoke methods on objects it directly possesses: its own fields, parameters passed to it, objects it created locally, or well-known global singletons. Never chain calls into the internals of a returned object (e.g. order.getCustomer().getAddress().getCity()). Instead, ask the immediate collaborator for what you need, or introduce a method on that collaborator." --enforcement "Code review"
```

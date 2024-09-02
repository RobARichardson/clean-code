---
icon: function
---

# Method Names

## Use Verbs

Methods should have verb or verb phrase names (e.g. `postPayment`, `deletePage`, ``save`)``

## Constructors

Overloaded constructors should use static factory methods with names that describe their arguments.

```csharp
// Good
Complex fulcrumPoint = Complex.FromRealNumber(23.0);
// Bad
Complex fulcrumPoint = new Complex(23.0);
```

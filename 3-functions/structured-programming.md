# Structured Programming

## Edsger Dijkstra

Every function and every block within a function should have one entry and one exit. There should only be one return statement, no `break` or `continue` statements, and never `goto` statements.

### However...

<mark style="color:green;">**When Functions are small**</mark>, these rules provide no benefit.

Favor "return early" instead.

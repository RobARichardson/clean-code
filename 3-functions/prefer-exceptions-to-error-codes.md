# Prefer Exceptions to Error Codes

* Returning error codes from command functions is a subtle violation of Command Query Separation.
* It promotes commands being used as expressions in the predicates of if statements.
  * This leads to deeply nested structures.

## Extract Try/Catch Blocks

Try/Catch blocks are ugly in their own right. It's better to extract the bodies of the `try` and `catch` blocks into their own functions.

## Error Handling is "One Thing"

Functions should do one thing. A function that handles errors should do nothing else.

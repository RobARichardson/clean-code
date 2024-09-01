# Function Arguments

## Quantity

* The ideal number of arguments is zero (niladic).
* One argument (monadic).
* Two arguments (dyadic).
* Three arguments (triadic).&#x20;
  * Should be avoided.&#x20;
* More than 3 requires special justification and should be very rare.

## Arguments are hard

* They take a lot of conceptual power.
* Make testing harder since they require writing test cases for every combination.
  * The more you have, the harder it becomes.
* Output arguments are harder to understand than input args.

## Monadic Functions: Single Argument

### Common Forms

* Ask a question about the argument
* Operate on the argument, transforming it into something else and _returning_ it.
* Events: An input with no output. Used to alter the state of the system.
  * It should be obvious to the reader that this is an event through names & contexts.

### Flag Arguments

* Flag arguments are ugly. Passing a Boolean into a function is a terrible practice.
* Typically this is a sign that a function should be split in two.

## Dyadic Functions: Two Arguments

* A function with two arguments is harder to understand than a monadic function.
* They're not evil, but they come at a cost.&#x20;
  * We should consider mechanisms available to convert them to monads.

## Triadic Functions: Three Arguments

* Significantly harder to understand than dyads.
* Think carefully before creating triads.

## Argument Objects

* Use when a function needs more than two or three arguments.
* This isn't cheating.&#x20;
* Groups of variables that are passed together are likely a concept on their own and deserving of a dedicated class.

## Argument Lists

If the variable arguments are ALL treated identically, they are equivalent to a single argument.

## Verbs and Keywords

Choosing good names for a function can go a long way toward explaining intent of the function, and the order and intent of the arguments.

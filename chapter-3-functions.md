# Chapter 3: Functions

## Small!

* 1st Rule: Functions should be small.&#x20;
* 2nd Rule: They should be smaller then that.

### Blocks and Indenting

* Blocks within `if`, `else`, and `while` statements should ideally be one line long.
  * The line should probably be a function call.
* Functions should not be large enough to hold nested structures.
  * The indent level of a function should not be greater than one or two.
    * Why? Readability & comprehension.

## Do One Thing

{% hint style="success" %}
Functions should do one thing. They should do it well. They should do it only.
{% endhint %}

We write functions is to decompose a larger concept into a set of steps at the next level of abstraction.

### One Level of Abstraction per Function

* To ensure functions are doing "one thing", statements within should be at the same level of abstraction.
* Mixing levels of abstraction creates confusion.&#x20;
* Like broken windows, once these details are mixed with essential concepts, more & more details tend to accumulate within the function.

## Reading Code from Top to Bottom: _The Step Down Rule_

* We want code to read like a top-down narrative.&#x20;

### **The Step-down Rule**

* Every function should be followed by those at the next level of abstraction so that we can read the program, descending one level of abstraction at a time as we read down the list of functions.
* This rule is the key to keeping functions short and doing "one thing".

## Switch Statements

* It's hard to make a switch statement that is small and does one thing.
* How do we handle this? With _polymorphism._
  * Bury switch statements in an [Abstract Factory](https://refactoring.guru/design-patterns/abstract-factory).

## Use Descriptive Names

* The smaller and more focused a function is, the easier it is to choose a descriptive name.
* Don't be afraid to make the name long. A long descriptive name is better than a long descriptive comment.
* Don't be afraid to spend time choosing a name.
* It's not at all uncommon that hunting for a good name results in favorable restructuring of the code.
* Be consistent with names. Use the same phrases, nouns, and verbs.

## Function Arguments

* Quantity
  * The ideal number of arguments is zero (niladic).
  * One argument (monadic).
  * Two arguments (dyadic).
  * Three arguments (triadic).&#x20;
    * Should be avoided.&#x20;
  * More than 3 requires special justification and should be very rare.
* Arguments are hard
  * They take a lot of conceptual power.
  * Make testing harder since they require writing test cases for every combination.
    * The more you have, the harder it becomes.
  * Output arguments are harder to understand than input args.

### Monadic Functions: Single Argument

#### Common Forms

* Ask a question about the argument
* Operate on the argument, transforming it into something else and _returning_ it.
* Events: An input with no output. Used to alter the state of the system.
  * It should be obvious to the reader that this is an event through names & contexts.

#### Flag Arguments

* Flag arguments are ugly. Passing a Boolean into a function is a terrible practice.
* Typically this is a sign that a function should be split in two.

### Dyadic Functions: Two Arguments

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

## Have No Side Effects

* Side effects are lies because the function is doing more than it says.
* Side effects often create temporal coupling, where the method can only be called at certain time or order.

{% embed url="https://www.pluralsight.com/tech-blog/forms-of-temporal-coupling" %}

## Output Arguments

* Arguments are most naturally interpreted as _inputs_ to a function.
* Anything that forces you to check the function signature is equivalent to a _double-take;_ a cognitive break to be avoided.
* Output arguments should be avoided.&#x20;
  * Functions that must change the state of something should change the state of its owning object.

## Command Query Separation

* Functions should either do something or answer something, but not both.
* Doing has a tendency to create confusion

## Prefer Exceptions to Returning Error Codes

* Returning error codes from command functions is a subtle violation of Command Query Separation.
* It promotes commands being used as expressions in the predicates of if statements.
  * This leads to deeply nested structures.

### Extract Try/Catch Blocks

Try/Catch blocks are ugly in their own right. It's better to extract the bodies of the `try` and `catch` blocks into their own functions.

#### Error Handling is "One Thing"

Functions should do one thing. A function that handles errors should do nothing else.

## Don't Repeat Yourself

* Duplication is the root of all evil in software.
* Use principles/practices/strategies to mitigate it.
  * Structured Programming
  * Aspect Oriented Programming
  * Component Oriented Programming

### Structured Programming

* Edsger Dijkstra: Every function and every block within a function should have one entry and one exit. There should only be one return statement, no `break` or `continue` statements, and never `goto` statements.
* However, when Functions are small, these rules provide no benefit.
* Favor "return early" instead.

## How Do You Write Functions Like This?

* Follow an iterative process.
* Start with long & complicated functions with tests.
* Then refactor:  massage, refine, split, rename, and eliminate duplication.

## Conclusion

* Functions are the verbs & classes are the nouns.
* Master programmers think of systems as stories to be told.&#x20;
  * They use the facilities of the chosen programming language to construct a rich & expressive language to tell that story.

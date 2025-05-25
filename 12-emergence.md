---
icon: eye
---

# 12: Emergence

## Getting Clean via Emergent Design

Kent Beck has four rules of Simple Design for creating well designed software

## Rule 1: Runs All The Tests

A system that is comprehensively tested and passes all of its tests all of the time is a testable system.  Systems that aren't tested aren't verifiable. &#x20;

A system that cannot be verified should never be deployed.

Tight coupling makes it difficult to write tests.  The more tests we write, the more principles we must use including DIP and Dependency Injection.

## Rules 2-4: Refactoring

Because we have tests, we are empowered to keep code clean!  We do this by by incrementally refactoring. Tests eliminate the fear that cleaning up the code will break it.

For each few lines we add, we pause and reflect on the new design.  Did we degrade it?  Time to refactor.

We apply anything from the entire body of knowledge and good software design including...

* Increase Cohesion
* Decrease Coupling
* Separate Concerns
* Modularize System Concerns
* Shrink Functions and Classes
* Choose Better Names

This is the time to apply the three rules of simple design:

1. Eliminate Duplicate
2. Ensure Expressiveness
3. Minimize the number of classes & methods

### Rule 2: No Duplication

Duplication is the primary enemy of a well-designed system.  It brings additional work, risk, and unnecessary complexity.

Duplication has many forms. Lines of code that look alike. Duplicate implementation, etc.

Creating a clean system requires the will to eliminate duplication.

### Rule 3: Expressive

It's easy to write code that we understand; at the time we write it, we're deep in the understanding of the problem.  Future maintainers of the code aren't going to have this deep understanding. &#x20;

The majority of the cost of a software project is in long-term maintenance.  As systems become more complex, they take more time to understand - there's a greater opportunity for misunderstanding.&#x20;

Code should clearly express the intent of the author. The clearer an author can make the code, the less time others will spend understanding it. This will reduce the cost of maintenance.

#### How can we express ourselves?

* **Good Names:** We want to hear a class or function name and not be surprised by its behavior.
* **Small Functions and Classes:** Easy to name, write, and understand.
* **Standard Nomenclature:** Design Patterns are about communication and expressiveness. Using standard names (e.g. Command, Visitor, Decorator) allow us to succinctly describe the design to other developers.
* **Well-written Unit Tests:** Primary goal of tests is to act as documentation by example.&#x20;

{% hint style="success" %}
TRY! All too often we get our code working and then move on to the next problem without giving sufficient thought to making the code easy for the next person to read. Take pride in your workmanship.
{% endhint %}

### Rule 4: Minimal Classes and Methods

Elimination of duplication, code expressiveness, and the SRP can be taken too far. We may end up creating too many tiny classes & methods. High class & method counts are sometimes the result of dogmatism.  We should remember to be pragmatic.&#x20;

This rule is the lowest priority of the four. Although it's important to keep class & method counts low, it's more important to have tests, eliminate duplication, and express yourself.




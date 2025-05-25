---
icon: file-binary
---

# 10: Classes

## Class Organization

1. Variables
   * Public static constants, if any, should come first.
   * Private static variables
   * Private instance variables
     * There is seldom a good reason to have a public variable.
2. Functions
   1. Ordering should follow the ordering of variables.

### Encapsulation

* Utility functions should typically be private, but we're not fanatic about it.
* Sometimes a variable or utility function needs to be protected so it can be accessed by a test. If a test in the same package needs to call a function or access a variable, we'll make it protected or package (internal) scope.
* Loosening encapsulation should be a last resort.

## Classes Should be Small

* First Rule: Classes should be small! Second Rule: They should be smaller than that.
* Function size is measured by counting _lines_. With classes, we count _responsibilities._
* Class names should describe the responsibilities it fulfills.
  * If this is difficult, the class may be too large.
  * The more ambiguous the class name, the more likely it has too many responsibilities.
  * Avoid weasel words: `Processor`, `Manager`, or `Super`

### Single Responsibility Principle

{% hint style="info" %}
SRP: A class or module should have one, and only one, _reason to change._
{% endhint %}

* Getting Software to work and making software clean are two very different activities.
  * Too many of us think we are done once the program works.
  * We fail to switch to the other concern or organization & cleanliness - breaking down overstuffed classes into decoupled units that follow the SRP.
* Do a large number of small, single purpose classes make it more difficult to understand the bigger picture?
* Would we rather have tools organized into toolboxes with many small drawers each containing well-defined and well-labeled components? Or do we want several large junk drawers?
* The primary goal in managing complexity is to organize it so that a developer knows where to look to find things.

#### Summary

* We want our systems to be composed of many small classes.
* Each small class encapsulates a single responsibility, has a single reason to change, and collaborates with a few others to achieve the desired system behaviors.

### Cohesion

* Classes should have a small number of instance variables.
* Each of the methods should manipulate one or more of those variables.
  * A class in which each variable is used be each method is maximally cohesive, but it's not advisable nor possible to achieve this fully.
* When cohesion is high, methods and variables of the class are co-dependent.

### Maintaining Cohesion Results in Many Small Classes

* When classes lose cohesion, split them!
* Breaking large functions into many smaller functions often gives us the opportunity to the code into several smaller classes.

## Organizing for Change

* We want to structure our systems so that we muck with as little as possible when we update them with new or modified features.
  * Small cohesive classes help us do this.
* In an ideal system, we incorporate new features by extending the system, not by making modifications to existing code.

{% hint style="info" %}
Open Closed Principle: Classes should be open for extension but closed for modification.
{% endhint %}

### Isolating from Change

* A client class depending on concrete details is at risk when details change.
  * Interfaces & abstract classes help isolate the impact of those details.
* Dependencies on concrete details create challenges for testing our system.
  * A system that is decoupled enough to be tested will also be more flexible and promote more reuse.
* A lack of coupling means that elements of our system are better isolated from each other and from change.
  * Isolation makes it easier to understand each element of the system.
* Minimizing coupling helps us adhere to the **Dependency Inversion Principle (DIP)**.

{% hint style="info" %}
Dependency Inversion Principle: Classes should depend upon abstractions, not on concrete details.
{% endhint %}

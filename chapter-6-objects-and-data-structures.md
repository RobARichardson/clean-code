---
description: There's a reason we keep our variables private.
---

# Chapter 6: Objects and Data Structures

{% hint style="warning" %}
Why do so many programmers automatically add getters & setters to their objects, exposing private variables as if they were public?
{% endhint %}

## Data Abstraction

* Hiding implementation is more than putting a layer of functions between the variables.
* Hiding implementation is about abstractions.
* A class does not simply push its variables out through getters & setters.
* A class exposes abstract interfaces that allow users to manipulate the _essence_ of the data, without having to know the implementation.
* Serious thought should be put into the best way to represent data than an object contains.

{% hint style="danger" %}
The worst option is to blithely add getters & setters.
{% endhint %}

## Data/Object Anti-Symmetry

* There's a difference between objects & data structures
* Objects hide their data behind abstractions and expose functions that operate on that data.
* Data structures expose their data and have no meaningful functions.
* The difference may seem trivial, but it has far-reaching implications.

### The dichotomy between objects & data structures:

> Procedural code (code using data structures) makes it easy to add new functions without changing the existing data structures. OO code, on the other hand, make it easy to add new classes without changing existing functions.

### The complement is also true:

> Procedural code makes it hard to add new data structures because all the functions must change. OO code make it hard to add new functions because all the classes must change.

{% hint style="info" %}
In complex systems, there will be situations where one is more appropriate than the other. Mature programmers know that idea that everything is an object is _myth_. Sometimes you really do want simple data structures with procedures operating on them.
{% endhint %}

## The Law of Demeter (Talk to friends, not to strangers)

_A module should not know about the innards of the objects it manipulates_\
[https://en.wikipedia.org/wiki/Law\_of\_Demeter](https://en.wikipedia.org/wiki/Law\_of\_Demeter)

#### A method _f_ of class _C_ should only call the following methods:

* Methods belonging to `C`
* An object created by `f`
* An object pass as an argument to `f`
* An object held in an instance variable of `C`

{% hint style="danger" %}
The method should not invoke methods of an object returned by another method.&#x20;
{% endhint %}

For many modern object oriented languages that use a dot as field identifier, the law can be stated simply as "use only one dot".

```
// Breaks the law
a.m().n()
// Does not break the law
a.m() does not
```

## Train Wrecks

Chains of calls (below) are generally considered sloppy style and should be avoided.

```
var result = context.GetOptions().GetDirectory().GetAbsolutePath();
```

It's best to split them up such as:

```
var options = context.GetOptions();
var directory = options.GetDirector();
var path = directory.GetAbsolutePath();
```

## Hybrids

* Classes that are half object and half data structure containing functions that do significant things along with public variables/accessors.
* Hybrids make it hard to add new functions and data structures.
* Avoid them, they are the worst of both worlds.
  * Indicative of a muddled design who authors are unsure whether they need protection from functions or types.

## Hiding Structure

* Objects are supposed to hide their internal structure. We should not be able to navigate through them (via dot notation).
* How do we avoid this? Apply the [Tell vs. Ask Principle](https://martinfowler.com/bliki/TellDontAsk.html).
* Tell the object to do something rather than asking for variable and performing logic outside of the object.

## DTOs: Data Transfer Objects

* The quintessential form of a data structure.
* DTOs are useful structures, especially when communicating with a DB, data from sockets, etc.
* They often serve as the first stage in a series of translation stages that convert raw data in a DB into objects in Application Code.

## Active Record

* Special forms of DTOs
* Data structures with public variables and navigational methods including `Save` & `Find`_._
* They're typically a direct translation from DB Tables or other data sources.
* **Mistake**: Developers often treat these Data Structures as Objects by putting business rules in them - creating a hybrid between data structure & object.
* **Solution**: Treat Active Record as a Data Structure and create separate business objects that contain business rules that hide internal data (likely instances of Active Records)

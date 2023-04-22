---
description: Simple rules for creating good names
---

# Chapter 2: Meaningful Names

## Use Intention-Revealing Names

1. Choosing good names takes time, but saves more than it takes.
2. The name of a variable, function, or class should answer all the big questions.
   1. Why does it exist?
   2. What does it do?
   3. How it is used?

## Avoid Disinformation

* Programmers must avoid leaving false clues that obscure the meaning of the code.
* Spelling similar concepts similarly is _information._ Using inconsistent spellings is _disinformation_.

## Make Meaningful Distinctions

{% hint style="info" %}
Distinguish names in such a way that the reader knows what the differences offer.
{% endhint %}

1. It is not sufficient to add number series or noise words to satisfy the compiler. If names must be different, then they should also mean something.
2. Number-series naming (a1, a2, ...aN) is the opposite of intentional naming.
3. Noise words are a meaningless distinction (e.g. `Info` & `Data`)
4. Noise words are often redundant.
   1. The word `variable` should never appear in a variable name.
   2. The word `table` should never appears in a table name.

| Good          | Bad              |
| ------------- | ---------------- |
| `Customer`    | `CustomerInfo`   |
| `Money`       | `MoneyAmount`    |
| `Message`     | `TheMessage`     |
| `Product`     | `ProductData`    |
| `GetAccounts` | `GetAccountInfo` |

## Use Pronounceable Names

* Programming is a social activity. If you can't pronounce it, you can't discuss it without sounding like an idiot.
* Poor naming should not be tolerated. New developers should not have to have a variable explained to them.

## Use Searchable Names

* Longer names trump shorter names. Any searchable name trumps a constant in code.
* Single-letter names should ONLY be used as local variables inside short methods.
* Length of a variable name should correspond to the size of its scope.

## Avoid Encodings

* Encoding type or scope information into names adds an extra burden of deciphering.
* With the aid of modern IDEs, [Hungarian Notation](https://en.wikipedia.org/wiki/Hungarian\_notation) (HN) and other forms of encoding are simply impediments.&#x20;

## Member Prefixes

* Functions & classes should be small enough that they aren't needed anymore.
* IDEs should highlight & colorize members to make them distinct.
* Prefixes should be seen as clutter and a marker of older code.

## Avoid Mental Mapping

* Readers shouldn't have to mentally translate your names into other names they already know.
* This problem typically arises from using neither problem domain terms nor solution domain terms.
* One difference between a smart programmer and a professional programmer is that the professional understands that clarity is king. Professionals use their powers for good and write code that others can understand.

## Class Names

* Classes & objects should have noun or noun phrase names (e.g. `Customer`, `Product`, etc).
* Avoid words like `Manager`, `Processor`, `Data`, or `Info`.
* A class name should not be a verb.

## Method Names

* Methods should have verb or verb phrase names (e.g. `postPayment`, `deletePage`, ``save`)``
* Overloaded constructors should use static factory methods with names that describe their arguments.

```csharp
// Good
Complex fulcrumPoint = Complex.FromRealNumber(23.0);
// Bad
Complex fulcrumPoint = new Complex(23.0);
```

## Don't Be Cute

* Clever names are memorable only to people who share the author's sense of humor.
* Choose clarity over entertainment value.
* Cuteness in code often appears in slang and colloquialisms.
* Say what you mean. Mean what you say.

## Pick One Word per Concept

{% hint style="info" %}
A consistent lexicon is a great boon to the programmers who must use your code.
{% endhint %}

* Use one word for one abstract concept and stick with it.
* It's confusing to have `fetch`, `retrieve`, and `get` as equivalent methods of different classes.
* Likewise, it's confusing to have a `controller`, `manager`, and `driver` in the same code base.

## Don't Pun

* Avoid using the same word/term for two purposes. This is esentially a pun.
* Our goal, as authors, is to make our code as easy as possible to understand.&#x20;
* We want our code to be a quick skim, not an intense study.

## Use Solution Domain Names

{% hint style="info" %}
There are lots of very technical things that programmers have to do. Choosing technical names for those things is usually the most appropriate course.
{% endhint %}

* The audience of our code will be programmers.
* Use computer science terms, algorithm names, pattern names, math terms, and so forth.
* It is not wise to draw every name from the problem domain.

## Use Problem Domain Names

{% hint style="info" %}
When there's no "programmer-eese" for what you're doing, use the names of the problem domain.
{% endhint %}

* Code that has more to do with problem domain concepts should have names drawn from the problem domain.
* This allows readers of the code to ask a domain expert.
* Separating solution & problem domain concepts is part of the job of a good programmer & designer.

## Add Meaningful Context

* Place names in context for your reader by enclosing them in well-named classes, functions, and namespaces.
* When all else fails, prefixing the name may be necessary as a last resort.

## Don't Add Gratuitous Context

* Shorter names are generally better than longer ones, so long as they are clear.
* Add no more context to a name than is necessary.

## Final Words

* People are often afraid of renaming things for fear that some other developers will object.&#x20;
  * We do NOT share that fear and find that we are actually grateful when names change (for the better).
* You will probably end up surprising someone when you rename (just like any other code improvement).  Don't let it stop you in your tracks.


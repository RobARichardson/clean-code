---
description: Simple rules for creating good names
icon: input-text
---

# 2: Meaningful Names

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

* People are often afraid of renaming things for fear that some other developers will object.
  * We do NOT share that fear and find that we are actually grateful when names change (for the better).
* You will probably end up surprising someone when you rename (just like any other code improvement). Don't let it stop you in your tracks.

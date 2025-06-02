---
description: Techniques for defending systems from the problems of concurrent code
---

# Concurrency Defense Principles

## Single Responsibility Principle

Concurrency design is complex enough to be a reason to change in it's own right.&#x20;

Therefore, it deserves to be separated from the rest of the code.

* Concurrency-related code has its own life cycle of development, change & tuning.
* Concurrency-related code has its own challenges - different from and more complex than non-concurrency-related code.
* The number of ways in which miswritten concurrency-based code can fail makes it challenging enough without the added burden of surrounding application code.

{% hint style="success" %}
**Recommendation**:

Keep your concurrency-related code separate from other code.
{% endhint %}

## Corollary: Limit the Scope of Data

Two threads modifying the same field of a shared object can cause unexpected behavior.

Treating these areas as a critical section of code (e.g. `lock`), is an imperfect solution and should be used rarely.

The more places shared data gets updated, the more likely:

* We'll forget to protect those areas.
* There will be duplication of effort to ensure everything is guarded
* It will be difficult to find the source of failures.

{% hint style="success" %}
**Recommendation**:

Take data encapsulation to heart. Severely limit the access of any data that may be shared.
{% endhint %}

## Corollary: Use Copies of Data

Avoid sharing data in the first place. Copy objects and treat them as read-only (immutable).

#### What about memory overhead?

If avoiding shared data avoids synchronizing, the savings in avoiding intrinsic lock will likely make up for additional overhead (creation & garbage collection).

## Corollary: Threads Should Be as Independent as Possible

Consider writing code such that each thread exists in its own world, sharing no data with any other thread.

Of course, most applications eventually run into shared resources such as a database connections.

{% hint style="success" %}
**Recommendation**:&#x20;

Attempt to partition data into independent subsets that can be operated on by independent threads, possibly in different processors.
{% endhint %}

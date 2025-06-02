---
description: Graceful shutdown can be hard to get correct.
---

# Writing Correct Shut-Down Code is Hard

## Examples

#### Imagine a system where a parent spawns child threads

* The parent waits for all to finish before it shuts down.
* What if one of the spawned threads is deadlocked?
* The parent will likely wait forever.

#### A similar system is instructed to shut down.&#x20;

* The parent thread tells spawned child threads to abandon their tasks and finish. &#x20;
* What if two children were operating as a producer/consumer pair?
* Producer receives the signal and shuts down.
* The consumer might be blocked waiting for the producer and is in a blocked state.&#x20;

{% hint style="success" %}
**Recommendation**:

Think about shut-down early and get it working early.&#x20;

It's going to take longer than you expect.

Review existing algorithms because this is probably harder than you think.
{% endhint %}

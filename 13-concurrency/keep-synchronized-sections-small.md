# Keep Synchronized Sections Small

## A synchronized section of code introduces a lock.&#x20;

* Only one thread of at any given time.
* Locks are expensive because they introduce delays and add overhead.
* The fewer the better. Littering code with lock statements is a bad idea.

### Naive programmers try to make their critical sections very large

* This will increase contention and degrade performance.

{% hint style="success" %}
**Recommendation**:

Keep Critical Sections as Small as Possible
{% endhint %}

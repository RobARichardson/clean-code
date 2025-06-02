# Know Your Library

* Use provided thread-safe collections
* Use the executor framework for executing unrelated tasks.
* Use nonblocking solutions when possible
* Know which libraries are not thread-safe.

## Thread Safe Collections

* Examples: `ConcurrentHashMap`, `ConcurrentDictionary`, etc
* Features like lock, Semaphore, SemaphoreSlim, etc support advanced concurrency design.

{% hint style="success" %}
**Recommendation**:&#x20;

Review the classes available to you. Become familiar with them. Know when to use them.
{% endhint %}

{% embed url="https://learn.microsoft.com/en-us/dotnet/standard/collections/thread-safe/" %}

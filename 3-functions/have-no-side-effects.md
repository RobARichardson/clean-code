# Have No Side Effects

* Side effects are lies because the function is doing more than it says.
* Side effects often create temporal coupling, where the method can only be called at certain time or order.

{% embed url="https://www.pluralsight.com/tech-blog/forms-of-temporal-coupling" %}

## Output Arguments

* Arguments are most naturally interpreted as _inputs_ to a function.
* Anything that forces you to check the function signature is equivalent to a _double-take;_ a cognitive break to be avoided.
* Output arguments should be avoided.&#x20;
  * Functions that must change the state of something should change the state of its owning object.

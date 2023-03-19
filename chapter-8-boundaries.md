---
description: >-
  Practices & techniques to keep the boundaries of our software clean when
  integration third-party packages and APIs.
---

# Chapter 8: Boundaries

## Using Third-Party Code

1. There is a natural _**tension**_ between the provider of an interface and the user.
2. Providers strive for broad applicability so they can appeal to a wide audience.
3. Users, want an interface focused to their particular needs.
4. **This tension can cause problems at the boundaries of our systems.**

## Exploring & Learning Boundaries

1. Third-Party code helps us get more functionality delivered in less time.
2. Where do we start when we want to utilize a third-party package?&#x20;
3. Learning & integrating third-party code is hard.
4. While it's not our job to test the third-party code, it may be in our best interest to write tests for the code we use.

### **Use Learning Tests**

1. Instead of experimenting and trying third-party code in our production code, we could write some tests to explore our understanding of the third-party code.
2. We call the third-party code (API) as we expect to use it in our application.
3. These are controlled experiments that check our understanding of an API.

### Learning Tests are Better Than Free

1. Learning tests are an easy, isolated way to gain knowledge.
2. They have a positive return on investment: the same tests are used to verify behavior during upgrades.
3. A clean boundary should be supported by a set of of outbound tests that exercise the interface in the same way Production code does.
   1. Without these test, we may be tempted to stay with an old version longer than we should.

## Clean Boundaries

1. Good software designs accommodate change without huge investments & rework.
2. Code at the boundaries needs clear separation & tests that define expectations.
3. We should avoid letting too much of our code know about the particulars of the third-party.
4. <mark style="color:yellow;">It's better to depend on something you control that on something you don't, lest it end up controlling you.</mark>
5. Manage third-party boundaries by having very few places in the code that refer to them. (i.e. use Wrappers or Adapters)

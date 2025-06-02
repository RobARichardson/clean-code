# Why Concurrency?

Writing clean, concurrent programs is hard!

It's easy to write multi-threaded code that is fine on the surface but broken at a deeper level - code that works fine until the system is placed under stress.

## Why Concurrency

* Concurrency is a decoupling strategy. Decouple _what_ gets done from _when_ it gets done.
* Decoupling what from when can dramatically improve throughput & structure of applications.
* Offers powerful ways to separate concerns, making a system easier to understand.

## Myths & Misconceptions

### Concurrency always improves performance

Concurrency can _**sometimes**_ improve performance, but only when there is a lot of wait time that can be shared between multiple threads or multiple processors.

### Design does not change when writing concurrent programs

Decoupling what from when usually has a huge effect on the structure of a system.

### Understanding concurrency issues is not important when working with a container (Web or EJB)

You need to know what your container is doing and how to guard against issues that comes with concurrent updates and deadlocks.

## Considerations when writing concurrent software

* Concurrency incurs some overhead, both in performance and additional code.
* Correct concurrency is complex, even for simple programs.
* Concurrency bugs aren't usually repeatable, so they are often ignored as one-offs.
* Concurrency often requires are fundamental change in design strategy.

---
description: There are several way to partition behavior in a concurrent application
---

# Know Your Execution Models

## Basic Definitions

<table data-header-hidden><thead><tr><th width="221">Term</th><th>Definition</th></tr></thead><tbody><tr><td>Bound Resources</td><td>Resources of a fixed size or number used in a concurrent environment. (e.g. DB connections)</td></tr><tr><td>Mutual Exclusion</td><td>One one thread can access shared data or a shared resource at a time.</td></tr><tr><td>Starvation</td><td>One thread or group of threads is prohibited from proceeding for an excessively long time (or forever).</td></tr><tr><td>Deadlock</td><td>Two or more threads waiting for each other to finish. Each thread has a thread the other requires. Neither can finish.</td></tr><tr><td>Livelock</td><td>Threads in lockstep, each trying to do work but the other is in the way. Due to resonance, threads continue trying to make progress but are unable for an excessively long time - or forever.</td></tr></tbody></table>

## Producer-Consumer Problem

* One or more producer threads create some work and place it in a buffer or queue.
* One (or more) consumer threads acquire that work from the queue and complete it.
* The queue between them is a _bound resource_.  Both wait to be notified when they can continue.

{% embed url="https://en.wikipedia.org/wiki/Producer%E2%80%93consumer_problem" %}

## Readers-Writers Problem

When you have a shared resource that serves as a source of information for readers, but is occasionally updated by writers, throughput is an issue.

Emphasizing throughput can cause starvation.

Tough Balancing Act: Coordinating readers to avoid reading something being updated by a writer.

Challenge: Balance the needs of reads and writes to:

* Satisfy correct operation
* Provide reasonable throughput.
* Avoid starvation.

{% embed url="https://en.wikipedia.org/wiki/Readers%E2%80%93writers_problem" %}

## Dining Philosophers Problem

An illustration to demonstrate concurrent algorithm design and solutions:

Philosophers sitting at a circular dining table, each with a fork to their left. A bowl of spaghetti in the center of the table. They spend their time thinking unless they get hungry. They can only eat if they have two forks. Once a philosopher eats, he puts both forks down making them available to the philosophers on either the right or left.

* Philosophers = Threads.&#x20;
* Forks = resources.

Unless carefully designed, systems that compete in this way can experience deadlock, livelock, throughput, and efficiency degradation.&#x20;

{% embed url="https://en.wikipedia.org/wiki/Dining_philosophers_problem" %}

## Summary

Most concurrent problems will be some variation of these problems.

Study and write solutions to these so that you're prepared.

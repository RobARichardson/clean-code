# Chapter 1: Clean Code

## There Will Be Code

* Does clean code matter?
* Claims that code will soon be generated instead of written are nonsense.
* We will never be rid of code, because code represents details of the requirements.
  * At some level those details cannot be ignored or abstracted; they must be specified.
  * Specifying requirements in such detail that a machine can execute them is _programming_.

{% hint style="info" %}
Code is the language in which we ultimately express the requirements!
{% endhint %}

## Bad Code

{% hint style="info" %}
**Wading**: The experience of being significantly impeded by bad code.
{% endhint %}

### Why do we write bad code?

* Were you trying to go too fast? Were you in a rush?
* Perhaps you felt that you didn't have time to do a good job; your boss would be angry if you took the time to clean up your code.
* Perhaps you were tired of working on this program and wanted it to be over.

### We've All Done It

* We've all looked at the mess we've made and chosen to leave it for another day. We've all said we'd go back & clean it up later.&#x20;
* LeBlanc's Law: "Later equals never"

{% embed url="http://on-agile.blogspot.com/2007/04/why-you-wont-fix-it-later.html" %}

## The Total Cost of Owning a Mess

* As a mess builds, the productivity of the team continues to decrease.
* As productivity decreases, management does the only thing they can.
  * They add staff to the project in hopes of increasing productivity.
  * New staff is not versed in the design of the system. They make changes that thwart the design.
* Pressure to increase productivity leads to more and more messes which further drives down productivity.

## The Grand Redesign in the Sky

The circle of life:

* Developers working in a bad code base eventually demand a redesign.
* Management reluctantly agrees due to poor productivity.
* A [tiger team](https://en.wikipedia.org/wiki/Tiger\_team) is selected to start over on a green-field project.
* The two teams are in a race to rebuild the new system while new features are continually added to the existing system.  The race goes on for a long time (many years).
* When it's done, the original members of the tiger team are gone and the new system needs another redesign because it's a mess (again).

{% hint style="success" %}
Spending time keeping code clean is not just cost effective; it's a matter of professional survival
{% endhint %}

## Attitude

Why does good code rot so quickly into bad code?

### Common Excuses

* We complain the requirements changed in ways that thwart the original design.
* We bemoan the schedules that were too tight to do things right.
* We blather about stupid managers, intolerant customers, and useless marketing types.

### The Real Reason

{% hint style="danger" %}
We Are Unprofessional
{% endhint %}

* Managers & marketers look to _us_ for the information they need to make promises & commitments. We should NOT be shy about telling them what we think.
* Users look to _us_ to validate the way the requirements will fit into the system.
* Project Managers look to _us_ to help work out the schedule.
* Most managers want good code, even when they are obsessing over a schedule.
  * It's a manager's job to defend the schedule & requirements.
  * It's _our_ job to defend the code.
* <mark style="color:yellow;">It is unprofessional for programmers to bend to the will of managers who don't understand the risks of making messes.</mark>

## The Primal Conundrum

* Programmers face a conundrum of basic values.
* Developers with a few years of experience know that previous messes slow them down.
* Yet, all developers feel pressure to make messes to meet deadlines.
* Professionals know that the second part of the conundrum is wrong.
  * You will not make the deadline by making a mess.

{% hint style="success" %}
The ONLY way to make the deadline - the only way to go fast - is to keep the code as clean as possible at all times.
{% endhint %}

## The Art of Clean Code?

{% hint style="info" %}
Code-Sense: Being able to identify bad code AND knowing what to do about it.
{% endhint %}

* Clean code requires the disciplined use of a myriad little techniques applied through a painstakingly acquired sense of "cleanliness" otherwise known as "code-sense".
* A programmer _without_ "code-sense" can recognize when code is a mess but have no idea what to do about it.
* A programmer _with_ "code-sense" will see a mess and see options & variations.
  * This will guide the programmer to plot a sequence of behavior preserving transformations to get from here to there (aka Refactoring).

## What is Clean Code?

### "Big" Dave Thomas

> Clean code can be read, and enhanced by a developer other than its original author. It has unit & acceptance tests. It has meaninful names. It provides one way rather than many ways for doing one thing. It has minimal dependencies, which explicitly defined and provides clear & minimal API. Code should be literate since depending on the language, not all necessary information can be expressed clearly in code alone.

### Michael Feathers

> Clean code looks like it was written by someone who cares. There is nothing obvious you can do to make it better. All those things were thought about by the original author and if you try to imagine improvements, you're led back to where you are, sitting in appreciation of the code someone left for you - code left by someone who cares deeply about the craft.

### Ron Jefferies

> Runs all the tests; Contains no duplication; Does one thing; Expresses all the design ideas that are in the system; Minimizes the number of entities such as classes, methods, functions, and the like.

### Ward Cunningham

> You know you're working with clean code when each routine you read turns out to be pretty much what you expected. You can call it beautiful code when the code also makes it look like the language was made for the problem.

## The Boy Scout Rule

{% hint style="info" %}
If we all checked-in our code a little cleaner than when we checked it out, the code simply could not rot.
{% endhint %}

* It's not enough to write the code well. Code must be _kept clean_ over time.
* Code rot and degradation happens as time passes.  Messes build quietly.
* We must take an active role in preventing that degradation.


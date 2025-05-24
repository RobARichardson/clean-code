---
icon: message-lines
---

# 4: Comments

## Comments Don't Make Up for Bad Code

{% hint style="success" %}
Don't Comment Bad Code - rewrite it!
{% endhint %}

* A common motivation for comments is bad code.
* Clear & expressive code with few comments is far superior to cluttered & complex code with lots of comments.&#x20;
* Rather than spend your time writing the comments that explain the mess you've made, spend it cleaning that mess.

## Explain Yourself in Code

* There are times when code makes a poor vehicle for explanation. These are rare.
* It takes only a few seconds of thought to explain more of your intent in code. &#x20;
  * Often it's simply a matter of creating a function that says the same thing as the comment you wanted to write.

## ✅ Good Comments

### Legal Comments

These are copyright & authorship statements.&#x20;

Where possible, refer to a standard license or external document instead.

### Informative Comments

Sometimes a comment can provide useful, basic information. Comments like this should be rare though - a function name is typically better suited for this job.

### Explanation of Intent

Sometimes a comment goes beyond just useful information about the implementation and provides the intent behind a decision. These comments help convey what the programmer was trying to do, especially when the implementation may not be immediately obvious or well understood.

### Clarification

Sometimes it can be helpful to explain the meaning of an obscure argument or return value. A clarification comment can be especially helpful when code can't be altered (i.e. a third party lib).

### Warning of Consequences

These are useful warnings to other developers about certain consequences.

### TODOs&#x20;

TODO comments are jobs that the programmer thinks should be done, but for some reason can't do at the moment. However, these are not an excuse to leave bad code in the system.  Code should not be littered with TODOs.

### Amplification

These comments amplify the importance of something that may otherwise seem inconsequential.

### XML Docs in Public APIs

If you're writing a public API, then you should certainly write good docs for it.

## ⛔ Bad Comments

### Mumbling

If you decide to write a comment, spend the time necessary to make sure it is the best comment you can write.  Any comment that requires you to look in another module for the meaning of the comment has failed to communicate.

### Redundant Comments

Comments that repeat what the code already explains only serve to clutter and obscure the code. They do not justify the code, or provide intent or rationale.

### Misleading Comments

Subtle misinformation in comments can create confusion, especially when the comment's existence encourages readers to read the comment instead of the code itself.

### Mandated Comments

Rules that state every function should have docs or every variable must have a comment are silly and contribute to noise.

### Journal Comments

This is an old practice of keeping a record of every change that has ever been made in a module.  Source Control makes this practice obsolete.

### Noise Comments

These are comments that restate the obvious and provide no new information. They are often ignored and thus they don't change as the code around them changes.&#x20;

Replace the temptation to create noise with the determination to clean your code.

### Position Markers

{% code title="Example:" %}
```
// Actions /////////////////////////////////////////
```
{% endcode %}

There are rare times when it makes sense to gather functions beneath a banner like this. But in general, they are clutter and should be eliminated.

### Closing Brace Comments

While this practice might make sense for long functions with deeply nested structures, it sever only to clutter the kind of small & encapsulated functions that we prefer. Shorten your functions instead.

### Attribution and Bylines

Comments that attribute the code to an author are better off in Source Control.

```
/ * Added by Rob */
```

### Commented-Out Code

&#x20;Keeping around commented code leads to confusion.  Why are these lines commented? Are they important? Were they left for a reason? Are they a reminder for an imminent change?&#x20;

Just delete the code! We can always get it back from Source Control.&#x20;

### HTML Comments

An abomination that makes comments hard to read. If comments are to be extracted by a tool and rendered in a web page, then it's the responsibility of that tool to adorn the comments with HTML.

### Nonlocal Information

If you must write a comment, make sure it describes the code it appears near rather than systemwide information or another part of the code base.

### Too Much Information

Don't put interesting historical discussions or irrelevant descriptions of details into comments. The person reading the code has no need for this arcane information.

### Unobvious Connection

The connection between a comment and the code it describes should be obvious. It's a pity when a comment needs its own explanation.

### Function Headers

When functions are short, they don't need a description.  A well-chosen name for a small function that does one thing is better than a comment header.

### XML Docs in Nonpublic Code

XML Documentation for classes & functions that aren't intended for public consumption is not generally useful and amounts to little more than cruft and distraction.


# ❌ Bad Comments

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

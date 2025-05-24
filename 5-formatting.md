---
icon: text-size
---

# 5: Formatting

## When people look under the hood of our software...

* We want them to be impressed with the neatness, consistency, and attention to detail that they perceive.
* We want their eyebrows to rise as they scroll through modules.
* We want them to perceive that _**Professionals**_ have been at work.

{% hint style="danger" %}
If they see a scrambled mass of code that looks like it was written by a bevy of drunken sailors, they will assume that the same inattention to detail pervades every other aspect of the project.
{% endhint %}

## Purpose of Formatting

* Code Formatting is important.  Too important to ignore.&#x20;
* Formatting is about communication. Communication is the professional developer's first order of business.
* Perhaps you thought that **"getting it working"** was the first order of business for a professional developer?
* The readability of code has a profound effect on all the changes that will ever be made.
* Coding style and readability set precedents that continue to affect maintainability and extensibility long after the original code has been changed.
* Style & discipline survives, even though your original code does not

## Vertical Formatting

How big should a source file be?  Small files are usually easier to understand than large files.

### The Newspaper Metaphor

Think of a well-written newspaper article.  We read it vertically.  At the top is headline telling us what the story is about.  The first paragraph provides a synopsis of the whole story, hiding the details while giving us a broad brush of the concepts.  The details increase as we progress downwards.

#### A source file should be like a newspaper article

* The name should be simple but explanatory
* The topmost parts of the source file should provide the high-level concepts & algorithms.&#x20;
* Details should increase as move downward.  At the end, we should find the lowest level functions and details.

### Vertical Openness Between Concepts

Each group of lines should represent a complete thought.  Thoughts should be separated by a blank line.

Specifically, blank lines should be used in between package declarations, functions, imports, etc.

This simple rule can have a profound effect on the visual layout of code. Each blank line is a visual cue that identifies a new and separate concept.&#x20;

### Vertical Density

Lines of code that are tightly related should appear vertically dense.&#x20;

### Vertical Distance

We often spend more time and mental energy trying to locate and remember where the pieces of a system are instead of trying to understand what a system does.

Concepts that are closely related should be kept vertically close to each other. Closely related concepts should not be separated into different files unless you have a very good reason.

We want to avoid forcing our readers to hop around through our source files and classes.

### Variable Declarations

Variables should be declared as close to their usage as possible. Because our functions should be short, local variables should appear at the top of each function.

In rare cases, a variable might be declared at the top of a block or just before a loop in a long-ish function.

### Instance Variables

Should be declared at the top of the class.  This should not increase the vertical distance of these variables.  In a well-designed class, these variables should be used by many (if not all) of the methods of the class.  Remember: Classes should be small.

### Dependent Functions

If one function calls another, they should be vertically close and the caller should be above the callee whenever possible.  This gives the program a natural flow.  It makes it easy to find the called functions and greatly enhances readability of the whole module.

### Conceptual Affinity

The stronger the affinity, the less vertical distance there should be between them.  Affinity is often based on direct dependence (one function calling another).  Other forms can include a common naming scheme and/or functions that perform variations of the same task.

### Vertical Ordering

We want function call dependencies to point in the downward direction. A function that is called should be below a function that does the calling.  This creates a high-level to low-level flow within the module.

We expect low-level details to come last. This allows us to skip the module, getting a gist from the first few functions without immersing ourselves in details.

## Horizontal Formatting




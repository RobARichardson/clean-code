# One Level of Abstraction per Function

To ensure functions are doing "one thing", statements within should be at the same level of abstraction.

Mixing levels of abstraction creates confusion.&#x20;

Like broken windows, once these details are mixed with essential concepts, more & more details tend to accumulate within the function.

## Reading Code from Top to Bottom: _The Step Down Rule_

* We want code to read like a top-down narrative.&#x20;

## **The Step-down Rule**

* Every function should be followed by those at the next level of abstraction so that we can read the program, descending one level of abstraction at a time as we read down the list of functions.
* This rule is the key to keeping functions short and doing "one thing".

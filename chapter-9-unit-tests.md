---
icon: vial
---

# 9: Unit tests

The Agile & TDD movements have encouraged many programmers to write automated tests, but in the mad rush to add testing to our discipline, many programmers have missed some of themore subtle, and important, points of writing good tests.

## The Three Laws of TDD

1. You may not write production code until you have written a failing unit test.
2. You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
3. Third Law: You may not write more production code than is sufficient to pass the currently failing test.

## Keeping Tests Clean

1. Having dirty tests is equivalent to, if not worse than, having no tests.
2. Test must change as production code evolves.
3. The dirtier the tests, the harder they are to change.
4. Test code is just as important as production code!
   * It is not a second-class citizen.
   * It requires thought, design, & care.
   * It must be kept as clean as production code.

## Tests Enable the -ilities

1. It is unit tests that keep your code flexible, maintainable, and reusable.
2. If you have tests, you do not fear making changes to your code! Without tests, every change is a possible bug.
3. The higher your test coverage, the less your fear.
4. Having an automated suite of unit tests that cover the production code is the key to keeping your design & architecture as clean as possible because tests enable _**change**_.
5. The dirtier your tests, the dirtier your code becomes.

## Clean Tests

1. What makes a clean test? Readability, Readability, Readability.
2. What makes tests readable? Clarity, Simplicity, and Density of Expression.
3. Anyone who reads a test should be able to work out what they do very quickly without being misled or overwhelmed by details.

### Domain-Specific Testing Language

* Disciplined developers refactor their test code into more succinct & expressive forms that make tests easier to read.

### A Dual Standard

* Code within the testing API has a different set of engineering standards than production code.
* It must still be simple, succinct, and expressive, but it need _**not**_ be as efficient as production code. Test & Production environments have very different needs.

## One Assert per Test

1. While the single assert rule is a good guideline, don't be afraid to put more than one assert in a test.
2. Instead, the number of asserts in a test ought to be minimized.
3. **Alternative: Single Concept per Test**
   1. Test a single concept in each test function.
   2. Minimize the number of asserts per concept.

## F.I.R.S.T

Clean tests follow 5 other rules:

### Fast

Tests should be fast. They should run quickly.

### Independent

Tests should NOT depend on each other. They should run in any order.

### Repeatable

Tests should be repeatable in any environment.

### Self-Validating

Test should have a Boolean output. Either they pass or fail. You should not have to read a log file to know whether tests passed.

### Timely

Tests need to be written in a timely fashion. They should be written just before production code. If written after, you may decide production code is too hard to test or you may not design the code to be testable.

## Conclusion

1. Tests are as important to the health of a project as the production code is.
2. Tests preserve & enhance the flexibility, maintainability, and reusability of production code.
3. If you let tests rot, then your code will rot too.

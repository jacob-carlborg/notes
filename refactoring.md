# Refactoring

"Refactoring is the process of changing a software system in such a way that it
does not alter the external behavior of the code yet improves its internal
structure."

You don’t have to know how to solve the whole problem in advance. The plan is
to nibble away, one code smell at a time, in faith that the path to openness
will be revealed.

## Things to Check For

* Is it DRY?
* Does it have one responsibility?
* Does everything in it change at the same rate?
* Does it depend on things that change less often than it does?

## Code Smells

* Switch statements
* Duplicated code

## Following the Flocking Rules

The good news is that you don’t have to be able to see the abstraction in
advance. You can find it by iteratively applying a small set of simple rules.
These rules are known as "Flocking Rules", and are as follows:

### Flocking Rules

1. Select the things that are most alike.
1. Find the smallest difference between them.
1. Make the simplest change that will remove that difference.

Changes to code can be subdivided into four distinct steps:

1. parse the new code
1. parse and execute it
1. parse, execute and use its result
1. delete unused code

As you’re following the rules:

* In general, change only one line at a time.
* Run the tests after every change.
* If you go red, undo and make a better change.

### Focusing on Difference

The good news is that a systematic application of the rules of refactoring
converts difference to sameness, decomposing a problem into its constituent
parts. The even better news is that this happens automatically. You don’t have
to identify the underlying abstractions in advance of refactoring. If you
merely write the code dictated by the rules, the abstractions will follow.

It takes many small, iterative steps, and results in a solution that is
discovered by refactoring.

Te rules say to first identify the things that are most alike. This means that
you should select the two branches that are most alike, and focus on making
them identical.

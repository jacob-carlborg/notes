# Object-Oriented Programming

Tests help prevent errors in code, but to characterize them so simply is a
disservice; they offer far more. Good OO is built upon small, interchangeable
objects that interact via abstractions. The behavior of each individual object
is often quite obvious, but the same cannot be said for the operation of the
whole. Tests fill this breach.

Object-oriented applications rely on message sending. The key virtue of
messages is that they add indirection. Messages allow the sender to ask for an
abstraction and be confident that the receiver will use the appropriate
concrete implementation to fulfill the request. Senders are responsible for
knowing what they want, receivers, for knowing how to do it. Separating
intention from implementation in this way allows you to introduce new
variations without altering existing code; simply create a new object that
responds to the original message with a different implementation.

When designed with the following features, object-oriented code can interact
with new and unanticipated variants without having to change:

1. Variants are isolated. They’re usually isolated in some kind of object, often a
    new class.

1. Variant selection is isolated. Selection happens in factories, which may be as
    simple as isolated conditionals that choose a class.

1. Message senders and receivers are loosely coupled. This is commonly
    accomplished by injecting dependencies.

1. Variants are interchangeable. Message senders treat injected objects as
    equivalent players of identical roles.


Initially, this reliance on abstractions and indirection increases the
complexity of code. What OO promises in return is a reduction in the future
cost of change. Highly concrete, tightly coupled code will resist tomorrow’s
change. Code that depends on loosely coupled abstractions will encourage it.

Because tests need to execute code, they supply early and direct information
about inadequate design, and they provide impetus and inspiration for
refinements. When tests are difficult to write, require lots of setup, or can’t
tell a satisfying story, something is wrong. Listen. Fixing problems now is not
only cheaper than fixing them later, but will improve your code, clarify your
tests, and make glad your work.

## Summary

Inject dependencies to loosen coupling,
leverage polymorphism to create interchangeable variants, and
use factories to select the specific concrete class of the correct variant.

## SOLID

* The [**single-responsibility principle**](https://en.wikipedia.org/wiki/Single-responsibility_principle):
    "There should never be more than one reason for a class to change." In other words, every class should have only one responsibility.
* The [**open–closed principle**](https://en.wikipedia.org/wiki/Open–closed_principle):
    "Software entities ... should be open for extension, but closed for modification."
* The [**Liskov substitution principle**](https://en.wikipedia.org/wiki/Liskov_substitution_principle):
    "Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it."
* The [**interface segregation principle**](https://en.wikipedia.org/wiki/Interface_segregation_principle):
    "Many client-specific interfaces are better than one general-purpose interface."
* The [**dependency inversion principle**](https://en.wikipedia.org/wiki/Dependency_inversion_principle):
    "Depend upon abstractions, [not] concretions."

### Dependency Inversion

Depend on abstractions, not concretions. Use dependency injection to accomplish
this.

### Liskov Substitution Principle

Objects of the same role should have the same interface.

## General Guidance

* Put domain behavior on instances.
* Be averse to allowing instance methods to know the names of constants.
* Seek to depend on injected abstractions rather than hard-coded concretions.
* Push object creation to the edges, expecting objects to be created in one place
    and used in another.
* Avoid Demeter violations, using the temptation to create them as a spur to
    search for deeper abstractions.
* Uncertainty about the future is not a license to guess; it’s a directive to
    decouple

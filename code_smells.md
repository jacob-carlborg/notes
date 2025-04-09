# Code Smells

## Blank Lines

Avoid blank lines. If you want to add a blank line it most likely is because
it's a change of topic and that most likely means the method has more than one
responsibility.

## Law of Demeter

You can talk to your friends, but not to their friends. More technically, you
should only send messages to your direct dependencies. You should not reach
across your dependencies to talk to their dependencies.

If you violate Demeter by talking to your friends' friends, you tightly couple
yourself to a network of objects. This makes your application fragile, that is,
your object might break because of an unexpected change to a distant and
apparently unrelated thing.

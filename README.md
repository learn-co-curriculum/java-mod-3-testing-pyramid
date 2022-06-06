# The Testing Pyramid

## Learning Goals

- Describe the testing pyramid

## Testing Pyramid

In the previous section, we touched on a very important concept that is worth
revisiting now, so we can underline its importance and also put it in the
context of the "testing pyramid".

> Once a specific piece of code and/or functionality is covered by one test, it
> does not need to be covered by another test.

We saw this in the previous section when we decided to extend the ability to
"FizzBuzz" one string to be able to "FizzBuzz" an array of strings. All we
needed to do was test the ability to properly pass each item in the array to the
existing `fizzBuzz()` method. Once we could do that properly, we felt confident
that method would do its job properly because we already had unit tests covering
that functionality.

Building on that observation, it follows pretty naturally that the "higher
level" the testing is, the less "detailed" scenarios it needs to cover.
"Detailed" is in quotes here because it's being used in a specific context to
mean "number and variety" of scenarios being covered:

1. Unit tests should cover all possible scenarios that our code is expected to
   handle
2. Functional and integration tests need to cover the expected behavior of the
   system (which may be comprised of more than one component) from a user's
   perspective. Note that in this case, the "user" may be an actual person or
   another component, set of components or entire system.
3. UI tests need to cover the components of the system that are responsible for
   presenting the information to actual end users (people) and getting
   information from those users.
4. Manual tests are tests that cannot be automated, usually because they require
   access to multiple systems or manual validation of results.

The exact categories of testing you will come across vary and include additional
types not described here, but based on the categories we have here, the
hierarchy of tests can be visualized like this:

![testing-pyramid.jpeg](testing-pyramid.jpeg)

While not all types of testing will be created or maintained by developers, it's
important that we understand the basic principles of the testing pyramid because
unit testing is the foundation on which all other types of testing are built,
and a pyramid can only be as strong as its foundation.

The principles of the testing pyramid can be summarized as follows:

1. The more automated and faster the tests are to run, the more permutations of
   possible use case they should cover, and the more frequently they should be
   run.
2. Conversely, the slower the tests are to run, the higher the level of
   functionality they cover (i.e. the more components the functionality requires
   to come together), the less permutations they should cover, and the less
   frequently they should run.

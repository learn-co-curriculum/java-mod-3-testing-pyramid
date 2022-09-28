# The Testing Pyramid

## Learning Goals

- Review and understand different types of testing.
- Describe the testing pyramid.

## Review Types of Testing

Let's review some different types of testing:

### Unit Testing

We have covered unit testing pretty well in this module. But as a review, unit
testing is a specific kind of testing that focuses on validating the
functionality of a single component of the system. It tests a small, specific
piece of functionality.

### Integration Testing

**Integration testing** is a type of testing that looks at multiple components of
a program and tests how well these modules may work together. The components
that are involved in integration testing are usually unit tested already with a
goal to see if any issues are exposed when they are integrated together.

### User Interface (UI) Testing

**User Interface (UI) testing** consists of testing the interface that users
interact with. UI tests need to cover the components of the system that are
responsible for presenting the information to actual end users and getting
information from those users. For example, testing the functionality and
features on a website. This could include looking at menus, images, and links.

### Manual Testing

Manual testing is the process of testing the system manually. An example of this
type of testing is when we would use print statements to verify if our code was
working properly.

## Testing Pyramid

A **testing pyramid** is a metaphor that can help developers and other types of
testers understand how to test. By that, we mean to answer the following
questions:

- How many tests are needed?
- How frequently should we run these tests?

The testing pyramid looks at the four types of tests we identified above to
answer these questions:

![testing-pyramid.jpeg](https://curriculum-content.s3.amazonaws.com/java-mod-3/testing-pyramid.jpeg)

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

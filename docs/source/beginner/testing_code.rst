============
Testing code
============

This section describes the basic concepts of software/code testing.

Introduction
============

There are various types of testing in different aspects of software development.
The two major types of testing based on user requirements are the Functional testing and non-functional testing.

Functional testing
------------------

Functional testing is used for verifying functional aspects of the code. Some common functional testing types are:

- Unit Testing
- Integration Testing
- API testing
- UI testing
- Acceptance testing

Non-functional testing
----------------------

Non-functional testing is used for verifying the non-functional requirements. Some common non-functional testing types are:

- Performance Testing
- Scalability testing
- Documentation testing
- Reliability testing
- Recovery testing
- Security testing

Python testing frameworks
=========================

unittest
--------

The `unittest <https://docs.python.org/3/library/unittest.html#module-unittest>`_ framework is an inbuilt testing framework in Python language.
Therefore, no additional installation required.

unittest is a xUnit-based Python testing framework. xUnit is a collective name for several unit testing frameworks and has the following main components:

- Test case: the basic element which defined the inputs, conditions, procedure and expected results of a single test.
- Test suite: a collection of test cases
- Test fixture: the fixed state used as a baseline for running tests
- Test runner: an executable program that run tests

Pytest
-------

It is more recommended using the `Pytest <https://docs.pytest.org/en/6.2.x/>`_ framework than unittest.
Pytest suits not only small unit tests but complex functional testing.
Moreover, Pytest supports running unittest-based tests and also provide features to write tests easily/compactly, run tests in parallel and more.

Some useful resources:

- `Enabling Pytest in Pycharm <https://www.jetbrains.com/help/pycharm/pytest.html#enable-pytest>`_
- `Best practices <https://docs.pytest.org/en/6.2.x/goodpractices.html#good-integration-practices>`_


=====
Fake it till you make it: mocks and fakes
=====

- Unit testing is critical to an application that you have to support
- Why unit tests?
  Fast
  Simple
  Greater localization of a failure
- Unit tests are for components, not entire app
- Unit tests don't test things that work together (those would be integration tests)
- The "mock" module is cool and useful -- use it!
- Action -> Assertion > Record -> Replay

How to create more testable code?
-----

- Limit scope of responsibility
- Smaller functions are easier to test
- Create local wrappers for things that interface externally or things which you might switch out later (db layer, http layer).
- Deduplicate the code

Overall
-----

- Recommended strategy: One test -- One Assert
- Tox = Virtualenv, multiple python versions, dependency list
- Unit testing is very similar to the Java world, but we don't have static typing so it's even more important!
- Unit tests are part of a complete breakfast

  - They don't solve the problem by themselves!

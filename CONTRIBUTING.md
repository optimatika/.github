# Contributing to ojAlgo or any related Optimatika project

Feel free to contribute any way you want. Whatever you feel is missing or "wrong", just fix it.

One very good way to contribute is to supply test cases that verify that the functionality you use works as expected. The ojAlgo code base is often refactored. Having tests specific to your use case, directly available to any developer, can be very beneficial (for you) in assuring future releases.

If something was hard to find or understand, but you've now got it, please contribute documentation.

Any/all code contributions should be done via pull requests, and before opening a PR consider:

- Is the change being proposed clearly explained and motivated?
- Is it ready for review?
- New code should have some level of tests.
- Bug fixes should come with a test that demonstrate the bug and show that you've now fixed it.
- Be prepared to have the proposed changes challenged...

When you contribute code, you affirm that the contribution is your original work and that you
license the work to the project under the project's open source license. Whether or not you
state this explicitly, by submitting any copyrighted material via pull request, email, or
other means you agree to license the material under the project's open source license and
warrant that you have the legal authority to do so.

## Code Style and Conventions

- Just make an effort to write code in line with what is already there (regardless of how you believe things should have been).
- Do NOT format or sort code that you did not actually change.

## Release Notes

Each project keeps a changelog on a format inspired by [Keep a Changelog](https://keepachangelog.com/en/1.0.0/). PR:s should also contain relevant updates to that log.

## Attribution

GitHub automatically keeps track of who contributed what, and if you've made a significant contribution to any individual class/file you may add yourself as an `@author` (javadoc). Other than that leave your name, e-mail or GitHub id out.

### Existing Tests

The already existing tests needs some attention as well:

1. @Disabled  Essentially there should be no disabled tests. Rather than disabled they may be tagged "unstabe" or "slow". The only tests that potentially could be permanently annnnotated as disabled are some difficult optimisation problems. Find a test that is disbaled, and figure out why it is. Then either fix the problem or tag the "unstabe" or "slow" rather than leave it disabled.
2. @Tag("unstable") There are some tests that sometimes fail due to randomly generated input. The solution here is typically NOT to set a fixed seed on the random number generator (or to otherwise "fix" the input). Instead the solution is to find the root cause of the test failure. When the tests fail - what happened? In many cases the problem seems to be related to complex number arithmatics. When/if you find the root problem, then create a separate test for that, and solve that problem.
3. @Tag("slow") Is it possible to reliably test the same thing faster?

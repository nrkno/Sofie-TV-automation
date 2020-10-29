---
description: >-
  The Sofie team happily encourage contributions to the Sofie project, and
  kindly ask you to observe these guidelines when doing so.
---

# Contribution Guidelines

## Reporting bugs

If you think you have found a bug in Sofie, we appreciate bug reports as GitHub issues.

As a minimum a bug report should include the following:

1. **Steps to reproduce:** a detailed description of what input or interaction caused the problem you are experiencing. This will help us greatly in reproducing the error situation ourselves, so that we can observe and analyze the problem.
2. **Expected behavior or result:** Following the steps given, what was it that you expected to happen?
3. **Actual behavior or result:** Following the steps given, what was it that actually happened?

Feel free to include additional information if you have it.

Issues should be reported in our main repository: [https://github.com/nrkno/Sofie-TV-automation/issues](https://github.com/nrkno/Sofie-TV-automation/issues)

## Contributing code

### How to contribute

#### Minor improvements and bug fixes

If you believe you have a minor improvement or a bug fix that can be added to the project you are welcome to contribute it as a pull request via GitHub.

#### New features or bigger changes

If you're considering a larger contribution, we would love to have a chat beforehand about it to make sure it fits nicely into our own development. Please open an issue for discussion over at [https://github.com/nrkno/Sofie-TV-automation/issues](https://github.com/nrkno/Sofie-TV-automation/issues)

### Things to keep in mind when contributing

#### Types

All of the Sofie projects use Typescript. When you contribute code, be sure to keep it as strictly-typed as possible.

#### Code style & formatting

Most of the projects use a linter. Before pushing your code, make sure it abides to the linting rules by running `yarn lint`.  `yarn lint --fix`can fix most of the issues.

{% hint style="info" %}
Tip: If using VS Code, turn on the "format on save"-feature in the settings, that way you won't have to think about formatting!
{% endhint %}

#### Documentation

To be honest, we don't aim to have the "absolute perfect documentation possible". BUT we do try to improve and add documentation to have a good-enough-to-be-comprehensible standard.

* The "what" something does something, is not as important - we can read the code for that.
* The "why" something does something, IS important. Implied usage, side-effects, descriptions of the context etc.. Those are things that greatly help a reader.

#### Tests

Most of the sofie-projects have unit-tests with a fairly good coverage. While developing, make sure any existing tests pass before you push your code. `yarn test` or `yarn watch` are your friends.

{% hint style="info" %}
We use Jest for running unit-tests. [Read more about its CLI here](https://jestjs.io/docs/en/cli).
{% endhint %}


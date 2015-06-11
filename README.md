# Contribution Guidelines

> Consolidated guidelines for contributing to iVantage Health Analytics, Inc.
> projects.


## Before You Start

We welcome contributions! However, before you begin working on a new feature
please create an issue requesting that feature in the respective project's
issue tracker and indicate that you would like to implement that feature. This
does two things:

1. It saves us from duplicating effort. We may already be working on that
   feature or something similar which serves the same use case.
2. It saves you from wasting time if this is not a feature we would like to add
   to the project.


## Coding Style

Take care to honor the existing style of the project you're contributing to. In
many cases there will already be a [`.editorconfig`][editor-config],
[.jshintrc][jshint] file, and/or a [.jscsrc][jscs] file in place. If so, please
make sure any additions adhere to the stylistic rules outlined there by running
the appropriate tool. Usually there will be an accompanying grunt or gulp task
to run those checks.


## Commit Message Guidelines

In general our commit messages follow the following format:

```
<type>: <summary>
<empty line>
<details>
```

Possible *type*s include:

- chore - E.g. updating build routines
- test - Adding, removing, fixing tests
- feature - Adding a new feature
- fix - Correcting broken functionality
- style - Cleaning up style, e.g. linting or appeasing jscs
- docs - Making edits to the documentation
- admin - This commit type is reserved for `svn` repos and should be used for
  actions such as deleting branches that have been fully reintegrated. Don't use
  `admin` if you are making source code changes.

The *type* should be all lower case and the first letter of *summary* should be
upper case.

Use an imperative mood and present tense for your summary (i.e. they should
sound read commands):

**Bad**: *Updated the bangs to whiz*<br />
**Good**: *Make the bangs whiz*

There should be one blank line between the summary and description. All lines
should be no longer than 80 characters.

If your commit closes or references any existing issues be sure to [make
reference to that issue in the message description][github-civcm].

#### Full Example

```
feature: Make the bangs whiz

If the user was not equipped to handle whirs they could not use this app. This
commit makes it whiz as well.

Closes #98
```


## Tests

Most projects have existing tests so please run them before submitting a PR :),
and be sure to add new tests when adding of changing functionality. Mosts tests
can be run with `npm run`, otherwise instructions will be laid out in the
project's README... if it's not clear how to run tests (or worse, you aren't
even sure tests exist) feel free to create an issue.


[editor-config]: http://editorconfig.org/
[jshint]: http://jshint.com/about/
[jscs]: http://jscs.info/
[github-civcm]: https://help.github.com/articles/closing-issues-via-commit-messages/

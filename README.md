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
<type>(scope): <summary>
<empty line>
<description>
```

Any line in the commit message should be *no longer than 80 characters*.

Platforms like Github and Bitbucket will pre-fill commit messages with
generic templates when merging pull requests. Please take the time when
merging your pull request to replace this with a nice commit message that
follows our format.

### Type

Possible *type*s include:

- chore - Changes only to supporting tooling, no production code changes.
  E.g. updating build routines
- docs - Making edits to the documentation
- feat - Adding a new feature
- fix - Correcting broken functionality
- perf - Code changes to improve performance
- refactor - Just like it used to be but better. All code changes that are
  not features, fixes, or performance improvements fit into this category
- style - Cleaning up style, e.g. linting, formatting, whitespace
- test - Adding, removing, fixing tests
- admin - This commit type is reserved for `svn` repos and should be used for
  actions such as deleting branches that have been fully reintegrated. Don't use
  `admin` if you are making source code changes.

The *type* should be all lower case.

### Scope (optional)

If your commit closes or references a Jira ticket or Github issue, the *scope*
should be the relevant issue number.

For example:

- Jira ticket - `feat(IVH-1234)`
- Github issue - `feat(#1234)`

### Summary

The first letter of *summary* should be upper case.
Use an imperative mood and present tense for your summary (i.e. they should
read like commands):

**Bad**: *Updated the bangs to whiz*<br />
**Good**: *Make the bangs whiz*

### Description (optional)

The description can contain any additional details you would like
to provide, e.g. the motivation or context for the change.

There should be one blank line between the summary and description.

If your commit closes any existing Github issue be sure to [make
reference to that issue in the message description][github-civcm].

### Full Example

```
feat(#98): Make the bangs whiz

If the user was not equipped to handle whirs they could not use this app. This
commit makes it whiz as well.

Closes #98
```


## Tests

Most projects have existing tests so please run them before submitting a PR :),
and be sure to add new tests when adding of changing functionality. Mosts tests
can be run with `npm test`, otherwise instructions will be laid out in the
project's README... if it's not clear how to run tests (or worse, you aren't
even sure tests exist) feel free to create an issue.


[editor-config]: http://editorconfig.org/
[jshint]: http://jshint.com/about/
[jscs]: http://jscs.info/
[github-civcm]: https://help.github.com/articles/closing-issues-via-commit-messages/

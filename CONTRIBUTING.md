# Contributing to iCore projects

You are here to help on iCore projects? Awesome, feel welcome and read the following sections in order to know how to ask questions and how to work on something.

Following these guidelines helps to communicate that you respect the time of the developers managing and developing this open source project. In return, they should reciprocate that respect in addressing your issue, assessing changes, and helping you finalize your pull requests.

There are many ways to contribute, from improving the documentation, submitting bug reports and feature requests or writing code which can be incorporated into iCore projects itself.

## Code of Conduct

All members of our community are expected to follow our [Code of Conduct][conduct]. Please make sure you are welcoming and friendly in all of our spaces.

## How to report a bug

We are using GitHub Issues for our public bugs. We keep a close eye on this and try to make it clear when we have an internal fix in progress. Before filing a new task, try to make sure your problem doesn’t already exist.

Here are some notes on how to report the bug so we can fix it as fast as possible:

* Explain, as detailed as possible, how to reproduce the issue.
* Include what you expected to happen, as well as what actually happened.
* If it's a bug with the website, please include information on what browser version and operating system you are running.
* If it helps, feel free to attach a screenshot or video illustrating the issue.
* If you're having trouble with a specific build, please include a link to the build or job in question.

## How to suggest a feature or enhancement

Contributions are welcome via Github pull requests. Each pull request should implement ONE feature or bugfix.
If you want to add or fix more than one thing, submit more than one pull request.

We have many projects written in different languages. For each language we use a corresponding code style that you should follow:

* [Golang Code Style][golang_code_style]
* [JavaScript Code Style][js_code_style]

The core team is monitoring for pull requests. We will review your pull request and either merge it,
request changes to it, or close it with an explanation.

Before submitting a pull request, please make sure the following is done:

* Fork the repository and create your branch from master.
* If you’ve fixed a bug or added code that should be tested, add tests!
* Ensure the test suite passes.
* Format your code with code style corresponding to the project.
* Make sure your code lints.

## Your First Pull Request

Working on your first Pull Request? You can learn how from this free video series:

[How to Contribute to an Open Source Project on GitHub][contributeguide]

To help you get your feet wet and get you familiar with our contribution process, we have a list of good first issues that contain bugs that have a relatively limited scope. This is a great place to get started.

If you decide to fix an issue, please be sure to check the comment thread in case somebody is already working on a fix. If nobody is working on it at the moment, please leave a comment stating that you intend to work on it so other people don’t accidentally duplicate your effort.

If somebody claims an issue but doesn’t follow up for more than two weeks, it’s fine to take it over but you should still leave a comment.

## Git Commit Guidelines

It is a recommended best practice to keep your changes as logically grouped
as possible within individual commits. There is no limit to the number of
commits any single Pull Request may have, and many contributors find it easier
to review changes that are split across multiple commits.

```text
$ git add my/changed/files
$ git commit
```

Note that multiple commits often get squashed when they are landed.

### Commit message format

A good commit message should describe what changed and why.

1. The first line should:
   - contain a short description of the change (preferably 50 characters or
     less, and no more than 72 characters)
   - be entirely in lowercase with the exception of proper nouns, acronyms, and
   the words that refer to code, like function/variable names
   - be prefixed with the name of the changed subsystem and start with an
   imperative verb. Check the output of `git log --oneline files/you/changed` to
   find out what subsystems your changes touch.

   Examples:
   - `net: add localAddress and localPort to Socket`
   - `src: fix typos in async_wrap.h`


2. Keep the second line blank.
3. Wrap all other lines at 72 columns (except for long URLs).

4. If your patch fixes an open issue, you can add a reference to it at the end
of the log. Use the `Fixes:` prefix and the full issue URL. For other references
use `Refs:`.

   Examples:
   - `Fixes: #1337`
   - `Refs: #3615`
   - `Refs: <URL>`

5. If your commit introduces a breaking change (`semver-major`), it should
contain an explanation about the reason of the breaking change, which
situation would trigger the breaking change and what is the exact change.

Sample complete commit message:

```txt
subsystem: explain the commit in one line

Body of commit message is a few lines of text, explaining things
in more detail, possibly giving some background about the issue
being fixed, etc.

The body of the commit message can be several paragraphs, and
please do proper word-wrap and keep columns shorter than about
72 characters or so. That way, `git log` will show things
nicely even when it is indented.

Fixes: #1337
Refs: <URL>
```

If you are new to contributing to iCore projects, please try to do your best at
conforming to these guidelines, but do not worry if you get something wrong.
One of the existing contributors will help get things situated and the
contributor landing the Pull Request will ensure that everything follows
the project guidelines.

## Semantic Versioning

iCore projects follow semantic versioning. We release patch versions for bugfixes, minor versions for new features, and major versions for any breaking changes. When we make breaking changes, we also introduce deprecation warnings in a minor version so that our users learn about the upcoming changes and migrate their code in advance.

Every significant change is documented in the changelog file of a project.

[conduct]: CODE_OF_CONDUCT.md
[contributeguide]: https://opensource.guide/how-to-contribute
[golang_code_style]: CODE_STYLE/golang.md
[js_code_style]: CODE_STYLE/js.md

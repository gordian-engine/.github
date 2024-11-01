# Contributing to the Gordian project

## General questions

For general questions about `gordian`, `gcosmos`,
or any other repository in the gordian-engine organization,
use the gordian-engine [discussion board](https://github.com/orgs/gordian-engine/discussions).

## Issues

Only file issues for bug reports and feature requests.

[Simon Tatham's article, _How to Report Bugs Effectively_](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html)
is a short article worth reading in its entirety.

## Pull requests

Follow the existing conventions in the repository against which
you are opening the pull request.

The rest of this section details some of the commonly missed conventions.

### Commit messages

There are many resources on writing good commit messages.
[This article from cbeams](https://cbea.ms/git-commit/)
is thorough and contains many source references.

We generally follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
This helps when browsing commits to understand the general scope of a change.
As a result of the prefixes imposed by Conventional Commits,
we don't tyipcally closely follow the 50-character subject rule in commit messages.

### Tests

Where possible, we use test-driven development within Gordian projects.
Both bug fixes and new features are expected to include tests.

Tests are expected to pass with the
[data race detector](https://go.dev/doc/articles/race_detector),
i.e. running `go test -race` should succeed.

### Semantic linefeeds

We use semantic linefeeds for markdown files and comments.
[Brandon Rhodes has a good article](https://rhodesmill.org/brandon/2012/one-sentence-per-line/)
explaining what semantic linefeeds are and why to follow that pattern.

> By starting a new line at the end of each sentence,
> and splitting sentences themselves at natural breaks between clauses,
> a text file becomes far easier to edit and version control.

Core maintainers frequently read diffs,
and semantic linefeeds make documentation and comment diffs readable.

### Godoc

There are conventions for using documentation comments in Go.
[The official docs](https://go.dev/doc/comment)
detail the conventions and available docuemtnation features.

One of the most commonly missed godoc patterns is:

> As with packages and funcs, doc comments for types start with complete sentences naming the declared symbol.

Complete sentences include punctuation. 

### Formatting

Use [goimports](https://pkg.go.dev/golang.org/x/tools/cmd/goimports) to format your Go code.

All Gordian repositories have a `.editorconfig` file in the root.
Make sure your editor [respects the configuration](https://editorconfig.org/#pre-installed).

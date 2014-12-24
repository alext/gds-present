# GDS presentation templates for Golang talks

This repository contains templates (HTML, JS, CSS) for use with Go's
[present][present-format] tool.  The templates are styled according to current
guidelines for GDS presentations, as of January 2015.

A tool is provided, `gds-present`, which wraps the `present` command and passes it
the path to the templates contained in this repository.

## Prerequisites

You'll need [Go][] installed and your `GOPATH` environment variable set.

## Installation

Run:

    export PATH=$PATH:$GOPATH/bin
    go get github.com/alphagov/gds-present

## Usage

In the directory containing the slides you wish to present, run:

    gds-present

`gds-present` will pass through any commandline arguments on to
the `present` command.

For more information on the present file format, see the [package
documentation][present-format].

## Rationale

Go's present tool is particularly useful when talking about Go code:

  - it allows Go code to be demonstrated during a presentation; code
    can be modified and executed mid-presentation

  - the `*.slide` [file format][present-format] is a simple text file which
    separates the presentation content from the presentation layout

## Provenance of the templates

The templates are based on the [default theme][] used by `present`. This repository
was created by cloning the repository containing those files and removing all
commits not relevant to the templates using '[git filter-branch][]'. As such,
all of the commit history for the default theme is retained.

[default theme]: https://github.com/golang/tools/tree/14ecce811fe734186cbf7b1481f7b8368ddb0e68/cmd/present
[git filter-branch]: http://git-scm.com/docs/git-filter-branch
[Go]: https://golang.org/
[present-format]: http://godoc.org/golang.org/x/tools/present

# acceptance

Daily acceptance tests for Jekyll. Builds 10 complex websites.

[![Build Status](https://travis-ci.org/jekyll/acceptance.svg?branch=master)](https://travis-ci.org/jekyll/acceptance)

## Background

[Jekyll](https://github.com/jekyll/jekyll) is a static site generator
written in Ruby. Any actively-developed software project needs to be
regularly tested. To this end, Jekyll runs unit tests and integration tests
for every pull request and push to `master`. Beyond this, Jekyll is tested
by adventurous users who build their site with pre-releases or from
`master`. Often, these real-world site builds uncover bugs that the unit &
integration tests miss. So I asked myself, "what if we built regularly
against a hand-picked set of Jekyll sites?"

## Acceptance Testing

Acceptance testing is a new concept from agile programming. In our case,
we're going to use it to mean real-world testing with user-created input.
We have a curated list of 10 sites (located in `script/cibuild`) that get
built with the latest `master` each night. If something starts breaking,
I'll get an email.

## Running

Want to run this locally? You probably won't want to. It expects a clean
environment at the moment. For the daring:

1. `script/bootstrap`
2. `script/cibuild`

That's it! `bootstrap` gets everything into place and `cibuild` commences
the building.

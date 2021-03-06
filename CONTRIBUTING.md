# Contributing to DIPY

DIPY is an open-source software project, and we have an open development
process. This means that we welcome contributions from anyone. We do ask that
you first read this document and follow the guidelines we have outlined here and
that you follow the [NIPY community code of conduct](http://nipy.org/conduct.html).

## Getting started

If you are looking for places that you could make a meaningful contribution,
please contact us! We respond to queries on the [Nipy mailing
list](https://mail.python.org/mailman/listinfo/neuroimaging), and to questions
on our [gitter channel](https://gitter.im/nipy/dipy). A good place to get an
idea for things that currently need attention is the
[issues](https://github.com/nipy/dipy/issues) page of our Github repository.
This page collects outstanding issues that you can help address. Join the
conversation about the issue, by typing into the text box in the issue page.

## The development process

Please refer to the [development section](http://dipy.org/devel/index.html)
of the documentation for the procedures we use in developing the code.

## When writing code, please pay attention to the following:

### Tests and test coverage

We use [nosetests](https://nose.readthedocs.org/) to write tests of the code,
and [Travis-CI](https://travis-ci.org/nipy/dipy) for continuous integration.

If you are adding code into a module that already has a 'test' file (e.g., if
you are adding code into ``dipy/tracking/streamline.py``), add additional tests
into the respective file (e.g., ``dipy/tracking/tests/test_streamline.py ``).

New contributions are required to have as close to 100% code coverage as
possible. This means that the tests written cause each and every statement in
the code to be executed, covering corner-cases, error-handling, and logical
branch points. To check how much coverage the tests have, you will need.

When running:

    nosetests --with-coverage --cover-package=dipy

You will get the usual output of nose, but also a table that indicates the test
coverage in each module: the percentage of coverage and also the lines of code
that are not run in the tests. You can also see the test coverage in the Travis
run corresponding to the PR (in the log for the machine with ``COVERAGE=1``).

Contributions to tests that extend test coverage in older modules that are not
fully covered are very welcome!

### Supporting both Python 2 and 3

Most of the functionality in DIPY works on both Python 3 and Python 2. Please
follow the instructions [here](http://dipy.org/devel/python3.html) to
write code that works on both versions.

### Code style

Code contributions should be formatted according to the [DIPY Coding Style Guideline](./doc/devel/coding_style_guideline.rst).
Please, read the document to conform your code contributions to the DIPY standard.


### Documentation

DIPY uses `Sphinx <http://www.sphinx-doc.org/en/stable/index.html>`_ to generate
documentation. The [DIPY Coding Style Guideline](./doc/devel/coding_style_guideline.rst)
contains details about documenting the contributions.

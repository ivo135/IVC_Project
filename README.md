International Virtual Currency Integration/Staging Tree 
=====================================

Currently based on Bitcoin Core

https://ivc-project.com

What is IVC (International Virtual Currrency)?
----------------

IVC (International Virtual Currency) is an experimental digital currency that enables instant payments to anyone, anywhere in the world, also something I wanted to learn in an attempt to make an alternative payment method. IVC uses peer-to-peer technology to operate with no central authority: managing transactions and issuing money are carried out collectively by the network. IVC Core is the name of open source software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of the IVC Core software, see https://ivc-project.com/en/download, or read the [original whitepaper](https://ivc-project.com/ivc-project.pdf).

License
-------

IVC Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/IVC_Project/IVC_Project/tags) are created
regularly to indicate new official, stable release versions of IVC Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://lists.linuxfoundation.org/mailman/listinfo/ivc-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #ivc-core-dev.

Testing
-------

Testing and code review are a bottleneck for development. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
significant money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[IVC Core's Transifex page](https://www.transifex.com/projects/p/ivc-project/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Translators should also subscribe to the [mailing list](https://groups.google.com/forum/#!forum/ivc-translators).

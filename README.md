oil
===

Oil is a new Unix shell, still in its early stages.

This repo contains a prototype in Python of a very complete bash parser, along
with a runtime that is less complete.

The dialect of bash that is recognized is called the **osh language**.  The
main goal now is to design the **oil language**, which shell scripts can be
automatically converted to.

After that, the Python dependency can be broken, which will involve some C++
code (but hopefully not too much).

Try it
------

Clone the repo and run `bin/osh`.  Basic things like pipelines, variables,
functions, etc. should work.

    bash$ bin/osh
    osh$ name=world
    osh$ echo "hello $name"
    hello world

Contributing
------------

If you want to contribute, e-mail [oil-dev@oilshell.org][oil-dev].

[oil-dev]: http://lists.oilshell.org/listinfo.cgi/oil-dev-oilshell.org

[The blog](http://www.oilshell.org/blog/) has some general updates on the
project status.

For information on how to build and test Oil, see [Contributing][] on the wiki.

[Contributing]: https://github.com/oilshell/oil/wiki/Contributing

Code Overview
-------------

Try this to show a summary of what's in the repo and their line counts:

    $ ./count.sh all

(Other functions in this file may be useful as well.)

Directory Structure
-------------------

    asdl/             # ASDL implementation
    bin/              # programs to run (bin/osh)
    core/             # the implementation (AST, runtime, etc.)
    osh/              # osh front end
    oil/              # oil front end (empty now)
    ovm/              # C++ runtime (empty now)
    tests/            # spec tests
    web/              # HTML/JS/CSS for tests and tools

    build.sh          # build support
    setup.py

    unit.sh           # test runners
    spec.sh
    wild.sh

    smoke.sh
    sh_spec.py        # shell test framework

    lint.sh           # static analysis
    count.sh          # Get an overview of the repo

    _tmp/             # For test temp files
    build/            # Python setup.py makes this directory

Unit tests are named `foo_test.py` and live next to `foo.py`.

More info
---------

Right now we're using
[/r/oilshell on Reddit](https://www.reddit.com/r/oilshell/) for general discussion.


I have docs that need to be cleaned up and published.  For now, there is a fair
amount of design information on
the [blog at oilshell.org](http://www.oilshell.org/blog/).


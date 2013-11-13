# Building

When you make changes to the greppy source, you probably want to (re-)build the
files at some point.

## Requirements

You should have ``node.js`` installed. If you have, switch to the ``greppy``-folder
via terminal and run the command ``npm install``. This will install the required
dependencies.

## Start building

Building is done via ``make``.

The following targets are currently available in the ``Makefile``:

* ``dist``: Build css and js.
* ``dist-js``: Build js only.
* ``dist-css``: Build css only.

So if for example you'd like to have your changes to source files translated to
minified versions, you'd simply switch to the ``greppy``-folder via terminal again
and run the command ``make dist``. The files located in the ``dist``-folder will be
replaced with new ones based upon the current sources.


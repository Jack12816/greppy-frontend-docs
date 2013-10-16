# Header

The header contains code, which is executed *before* every other file.

When concatenating the source file to greppy.js and greppy.min.js, the header
contents will be placed first.

## Examples

Currently, the global `greppy` is being defined in the header:

    var greppy = {};


# Footer

The footer contains code, which is executed after every other file.

When concatenating the source file to greppy.js and greppy.min.js, the footer
will be appended last.

## Examples

Currently, the `application class` is being instantiated in the footer:

    greppy.app = new greppy.Application();


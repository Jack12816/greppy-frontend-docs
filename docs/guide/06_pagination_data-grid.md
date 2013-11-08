# Paginator (Data-Grid)

The ``paginator class`` is meant to be used in conjunction with the
``data-grid class``. In fact, it will be instantiated by the data-grid class
most of the time.

As it's name suggests, it mainly handles pagination-related functionality;
mostly event handling of the paginator, to be precise.

## Methods

### getParameters(page)

Only used in internals. Returns an array of objects with relevant parameters
(page and limit). The ``page``-parameter is optional and defaults to the page
of the instance.

## Examples

None at this time. Please refer to ``data-grid``.

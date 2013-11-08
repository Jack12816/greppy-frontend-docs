# Data-Grid

The ``data-grid class`` is responsible for the core data-grid functionality.

It's constructor instantiates some other relevant data-grid classes:

* Search
* Sort
* Paginator

They are assigned to properties of the data-grid instance.

## Methods

The following methods are offered by the data-grid class:

### load(rows, pagination, page)

This method is used to trigger loading of the data-grid. The parameters are all
optional and allow defining custom settings for rebuilding.

By default, the first two parameters, ``rows`` and ``pagination``, are true which
means that the rows and the pagination will be updated.

The third parameter, ``page``, can be used to define a custom page which should be
loaded. Providing it is only needed, if you don't want the data-grid to handle
the current page.

If you'd want to update only the pagination (and not the rows), you could simply
pass a ``false`` as the first argument:

    load(false);

It's quite similar, if you'd only want the rows to be updated:

    load(true, false);

### buildUrl(params)

Only used in internals.

### loadAndRebuild(params, callback)

Only used in internals. Executes preLoad-hooks (if any exist) and sends the
AJAX-request to load the rows and update the table.

### reset()

Only used in internals. Reloads the data-grid. If there's a preReset-hook
provided, it's executed with the reload-function as first argument.

## Examples

Initialize a new data-grid with softDeletion-option:

    var datagrid = new greppy.DataGrid($('table.datagrid'), {
        softDeletion: true
    });


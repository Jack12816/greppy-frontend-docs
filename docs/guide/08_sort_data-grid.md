# Sort (Data-Grid)

The `sort class` is meant to be used in conjunction with the
`data-grid class`. In fact, it will be instantiated by the data-grid class
most of the time.

It is responsible for attaching sort-related events and handling
sort-operations.

## Methods

### toggle(th)

Only used in internals. Clears eventually exiting old sort-settings and applies
sorting regarding the current settings.
If there's no sorting specified, the data-grid will simply be reset by calling
it's `reset`-method. Else, the `load`-method of the associated `data-grid`-
object will be called.

### getParameters()

Only used in internals. Returns an array of objects with relevant parameters
(order and oprop).

## Examples

None at this time. Please refer to `data-grid`.

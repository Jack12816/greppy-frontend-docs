# Styler

The ``styler class`` offers easy to use methods for enhancing the ui.

## Methods

### initOverlay(el, showEvent, removeEvent)

With help of this method, you can create a dynamic overlay for an element of
your choice (first parameter). This is especially useful for situations where
a page is loading for some time. The overlay will have a spin.js based spinner
in it.

Parameters:

  * ``el`` The element which should be covered by the overlay
  * ``showEvent`` The event which triggers the overlay to be shown
  * ``removeEvent`` The event which triggers the overlay to be removed

### initSpinner(target, opts)

Only used internally.

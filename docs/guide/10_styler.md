# Styler

The `styler class` offers easy to use methods for enhancing the ui.

## Methods

### styleUpload(elem)

Since Twitters' Bootstrap doesn't offer a possibility to style file-uploads,
greppy offers a method which fills this gap.
`elem` is the only required parameter. It's the input element, which should be
styled.

Nice to know: You can't really style upload elements. All that's happening
internally is, that we create a pseudo upload element and hide the actual one.
Then some event bindings are done and the user only interacts with the dummy
element (which accesses the original upload internally).

### styleNumber(elem)

While HTML5 offers the possibility to define inputs of type number, modern
browsers don't handle these inputs in a similar way: Chrome and Opera offer
a spinner, but Firefox for example doesn't. That's why we came up with the
styleNumber-method. Simply pass in an input element as the parameter `elem`
(preferably type="text") and greppy will add a plus and a minus button next to
the input, which controls it's content.

You can use the attributes `data-min` and `data-max` to define the minimum and
maximum allowed value for the input (the spinner will stop then).

### initOverlay(el, showEvent, removeEvent)

With help of this method, you can create a dynamic overlay for an element of
your choice (first parameter). This is especially useful for situations where
a page is loading for some time. The overlay will have a spin.js based spinner
in it.

Parameters:

  * `el`: The element which should be covered by the overlay
  * `showEvent` The event which triggers the overlay to be shown
  * `removeEvent` The event which triggers the overlay to be removed

### validateStyleUpload(elem)

Only used internally.

### validateStyleNumber(elem)

Only used internally.

### initSpinner(target, opts)

Only used internally.

## Examples

### Styling an upload

Styling an upload is done by calling the `styleUpload` method on a greppy styler
instance and passing the input element as parameter:

    var g = new greppy.Styler();

    g.styleUpload($('#myFileInput'));

These are all necessary steps to style the input with the id `#myFileInput`.

### Styling a number

A number can be styled in a similar way:

    var s = new greppy.Styler();
    s.styleNumber($('#myNumInput'));

The result is, that our input with the id `#myFileInput` now has a spinner
attached to it.


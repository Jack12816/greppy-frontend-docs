# Number (Styler)

The ``number class`` is used to style an input element (or a set of
input elements) to have a number spinner attached to them.

## Methods

### style(el)

The only relevant method for the end user (that's probably you!).
``el`` might be a selector string or a jQuery object. If you pass a selector
or a set of jQuery elements, ensure that every element is an input element.
``style`` will then style the passed elements.

## More methods (these are used mainly internally)

### validate(el)
### handleCleanup(el)
### addStyles(el)
### addButtonHandlers(el)
### getVal(el)
### getAddedVal(el)
### getSubtractedVal(el)
### isNumber(el)
### clearStyled(el)

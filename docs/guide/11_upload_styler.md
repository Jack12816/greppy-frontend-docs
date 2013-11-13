# Upload (Styler)

The ``upload class`` is used to style an input[type="file"] element (or a set of
such elements) to have them replaced by elements in Bootstrap 3 look.

## Methods

### style(el)

The only relevant method for the end user (that's probably you!).
``el`` might be a selector string or a jQuery object. If you pass a selector
or a set of jQuery elements, ensure that every element is an input[type="file"]
element.
``style`` will then style the passed elements.

## More methods (these are used mainly internally)

### validate(el)
### addStyles(el)
### getMarkup(el)
### showFilename(el)
### getStyledUploadSelector(el)
### handleFilePreselected(el)
### addNewFileSelectedHandler(el)
### addButtonHandlers(el)
### showFileDialog(el)
### hideOriginalInput(el)

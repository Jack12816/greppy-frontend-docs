# Validator

The `validator class` offers a clean and uniform HTML5 validation for bootstrap elements.

## How to use it

Simply add the class `greppy-validator` to every input, select or textarea element
you want to be validated. Then just use regular HTML5 validation attributes to
define validation rules.

Greppy will then show a red box with an error message, if the validation fails.

## Attributes

Attributes help you customizing the behavior of validators. They are optional.

* ``data-greppy-validator-msg`` If added, it needs to be placed directly to the
validated element. You can define a message for a failing validation here.

* ``data-greppy-validator-mark`` Defines the element which is marked on failed
validation and under which the validation message is placed. The value must be
the name of the corresponding validated element.


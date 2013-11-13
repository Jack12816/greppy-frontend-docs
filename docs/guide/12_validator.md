# Validator

The ``validator class`` offers a clean and uniform HTML5 validation for
bootstrap elements.

## How to use it

Simply add the class ``greppy-validator`` to every input, select or textarea
element you want to be validated. Then just use regular HTML5 validation
attributes to define validation rules.

Greppy will then show a red box with an error message, if the validation fails.

## Attributes

Attributes help you customizing the behavior of validators. They are optional.

* ``data-greppy-validator-msg`` You can define a message for a failing validation here.
If added, it needs to be placed either to the element which has the
``data-greppy-validator-mark``-attribute (preferred for radio buttons) or
directly to the validated element.


* ``data-greppy-validator-mark`` Defines the element which is marked on failed
validation and under which the validation message is placed. The value must be
the name of the corresponding validated element.

## Multiple Elements with the same name

If there are multiple elements with the same name - which can occur when using
radio buttons - you need to give every one of them the class ``greppy-validator``.
However, duplicating the message or mark would be annoying in our opinion, so
Greppy validator only considers the attributes of the first matched element if
there is more than one element with the same name.

## Methods

Except the init-method, most methods aren't really important for simple usage of
the validator - just use attributes to define basic behavior.
But in case you need advanced functionality, you have to take a look at the
methods described here.

### init()

Simply call it, to initialize the Greppy validator. By default, it searches for
all input-, select- and textarea-elements with the class ``greppy-validator`` and
registers the following events triggered by them: ``invalid``, ``change``,
``keyup``.

### bindEvent(origEvtName, gEvtName)

This one is useful, if your inputs are modified by third party plugins, which
trigger custom events. Since Greppy validator does only register the standard
events by default, it can't always properly revalidate elements with custom
behavior.
To fix this, simply call bindEvent with the following parameters:

* ``origEvtName`` A string with the event you'd like to register
* ``gEvtName`` The corresponding Greppy validator event as String.

``gEvtName`` may be either ``gValidationUpdate`` or ``gValidationInvalid``. You
will probably mostly use ``gValidationUpdate``, which checks if the element is
valid and shows/removes the warning if it is/isn't. For more details, see the
section *Events*.

### getMark(el)

The getMark-method will return the corresponding mark of the element (which may
be the element with the corresponding ``data-greppy-validator-mark`` attribute
or the passed element itself).
Use it if you need to know, what will be marked on validation.

## More methods (these are used mainly internally)

### isUniqueValidator(el)
### getUniqueValidator(el)
### getUniqueValidators(allValidators)
### validate(el)
### markInvalid(el)
### removeInvalidMark(el)
### showMsg(el)
### hasActiveMsg(el)
### removeMsg(el)

## Events

Greppy validator uses two events internally: ``gValidationUpdate`` and
``gValidationInvalid``.

It's recommended to not directly attach these events and instead make use of the
``bindEvent``-method to register custom events.

``gValidationUpdate`` will basically check if the corresponding element is valid
or invalid and display or remove the warning message according to it's state.

``gValidationInvalid`` will show the warning message and prevent the default
behavior of the element (which is especially useful to suppress displaying the
*default* browser messages for HTML5 validation).

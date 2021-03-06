# Structure

The Greppy Frontend source is divided into multiple js-files and mostly follows
the rule *one class per file*.

* ``header.js`` Contains code which will be executed *first*.

* ``application.js`` Contains the application class. Allows easy modal handling.

* ``controller.js`` Contains the controller class. Allows easy link generation.

* ``data-grid.js`` Contains the base class for the data-grid.

* ``data-grid/``

    * ``pagination.js`` Contains the paginator class which allows paginating of the data-grid.

    * ``search.js`` Contains the search class which handles search operations of the data-grid.

    * ``sort.js`` Contains the sort class which handles sorting of the data-grid.

* ``styler.js`` Contains the styler class. Allows easy styling of different elements.

* ``styler/``

    * ``number.js`` Contains the number-styler. Allows adding a number spinner to inputs.

    * ``upload.js`` Contains the upload-styler. Allows "styling" an upload to look like BS3.

* ``validator.js`` Contains the validator class. Allows better HTML5 validation for bootstrap elements.

* ``footer.js`` Contains code which will be executed *last*.

The files are concatenated into one .js (and .min.js respectively) on building.

# Structure

The Greppy Frontend source is divided into multiple js-files and mostly follows
the rule "one class per file"``

* ``header.js`` Initializes the global `greppy`-object.

* ``application.js`` Contains the application class. Allows easy modal handling.

* ``controller.js`` Contains the controller class. Allows easy link generation.

* ``data-grid.js`` Contains the base class for the data-grid.

* ``data-grid/``

    * ``pagination.js`` Contains the paginator class which allows paginating of the data-grid.

    * ``search.js`` Contains the search class which handles search operstions of the data-grid.

    * ``sort.js`` Contains the sort class which handles sorting of the data-grid.

* ``sanitizer.js`` Contains the sanitizer class. Allows sanitation of elements.

* ``styler.js`` Contains the styler class. Allows easy styling of different elements.

* ``footer.js`` Initializes the Applications class to the global `greppy.app`.

The files are concatenated into one .js (and .min.js respectively) on building.

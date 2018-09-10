List of Objects
=======================


At the end of each lists of objects, the PRIDE Archive provides always *hyperlinks* to navegate each page:

.. code-block:: json

    _links: {
         self: {
             href: "http://www.ebi.ac.uk/pride/ws/archive/projects?pageSize=100&page=0"
         },
         next: {
             href: "http://www.ebi.ac.uk/pride/ws/archive/projects?pageSize=100&page=1"
         },
         previous: {
             href: "http://www.ebi.ac.uk/pride/ws/archive/projects?pageSize=100&page=0"
         },
         first: {
             href: "http://www.ebi.ac.uk/pride/ws/archive/projects?pageSize=100&page=0"
         },
         last: {
             href: "http://www.ebi.ac.uk/pride/ws/archive/projects?pageSize=100&page=55"
         }
    },
    page: {
        size: 100,
        totalElements: 5501,
        totalPages: 55,
        number: 0
    }

The page in defined by the parameters:

- **pageSize** : Number of objects in the list.
- **page** : Number of the page.

The *links* provide a way to navigate the list of paginated objects:

- *self* : Is a link to the current list of objects (e.g. projects, files, proteins )
- *next* : Is a link to the next set of objects (next page).
- *previous*: Is a link to the previous set of objects (previous page).
- *first* : Is a list ot the first set of objects (first page).
- *last* : Is a list ot the last set of objects (last page).
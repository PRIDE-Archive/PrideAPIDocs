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
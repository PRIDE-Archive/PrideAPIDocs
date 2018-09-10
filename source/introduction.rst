Introduction
============

.. sidebar:: API Browser Quick Guide
   :subtitle: **It can make your life easier** if you want to explore by yourself our api:

   * Please visit our `Swagger docs <https://www.ebi.ac.uk/pride/ws/archive/>`_


A hypermedia API provides an entry point to the API, which contains hyperlinks the clients can follow.
Just like a human user of a regular website, who knows the initial URL of a website and then follows hyperlinks to navigate through the site.
This has the advantage that the client only needs to understand how to detect and follow links.
The URLs (apart from the inital entry point) and other details of the API can change without breaking the client.

The entry point to the Plone RESTful API is the portal root.
The client can ask for a :term:`REST` API response by setting the ``'Accept'`` HTTP header to ``'application/json'``:

.. http:example:: curl python-requests

   GET /Plone/front-page HTTP/1.1
   Host: localhost:8080
   Accept: application/json
   Authorization: Basic YWRtaW46YWRtaW4=

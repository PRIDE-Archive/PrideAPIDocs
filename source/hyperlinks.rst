Hyperlinks
=====================

A hypermedia API provides an entry point to the API, which contains hyperlinks the clients can follow. Just like a human user of a regular website, who knows the initial URL of a website and then follows hyperlinks to navigate through the site. This has the advantage that the client only needs to understand how to detect and follow links. The URLs (apart from the initial entry point) and other details of the API can change without breaking the client.

For example, when we *query* the projects entry point, the end of the call returns the hyperlinks:

.. http:example:: curl python-requests

   GET projects HTTP/1.1
   Host: www.ebi.ac.uk/pride/ws/archive/
   Accept: application/json


The first part of the result response contains the PRIDE projects:

.. code-block:: json

    {
       _embedded: {
           projects: [
                {
                  accession: "PRD000001",
                  title: "COFRADIC proteome of unstimulated human blood platelets",
                  additionalAttributes: null,
                  projectDescription: "Not available",
                  sampleProcessingProtocol: "Not available",
                  dataProcessingProtocol: "Not available",
                  projectTags: [ ],
                  keywords: ["Not available"],
                  doi: null,
                  submissionDate: "2004-01-01",
                  publicationDate: "2005-12-09",
                  updatedDate: null,
                  submitters: [
                      {
                        title: "Mr",
                        affiliation: "HUPO Plasma Proteome Project",
                        email: "lennart.martens@UGent.be"
                      }
                  ],
                  labPIs: [ ],
                  affiliations: [
                        "HUPO Plasma Proteome Project"
                  ],
                  instruments: [
                    {
                      accession: "MS:1000031",
                      name: "instrument model",
                      value: "Micromass Q-TOF I",
                      cvLabel: "MS",
                      id: "MS:1000031"
                  }],
                  softwares: [
                    {
                      accession: "MS:1000531",
                      name: "software",
                      value: null,
                      cvLabel: "MS",
                      id: "MS:1000531"
                    }
                  ]
           ...


The last part of the each **Project Object** response contains the *hyperlinks* that allows to navigate each methods of an object:

.. code-block:: json

    _links: {
         self: {
              href: "http://www.ebi.ac.uk/pride/ws/archive/projects/PRD000001"
         },
         files: {
              href: "http://www.ebi.ac.uk/pride/ws/archive/projects/PRD000001/files?filter=&pageSize=100&page=0"
         }
     }

The *self* hyperlink is an entry point to the full information of the **Project** including all the data for the files, the _files_ entry point only provided the list of files that belongs to the **Project**.

.. toctree::
   :maxdepth: 1

   Hyperlinks in Lists <lists>


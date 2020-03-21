########
API Docs
########

*API endpoint urls to be determined*

**********
nonprofits
**********

==============
GET nonprofits
==============
/api/v0/nonprofits

Get JSON array of nonprofits

-------
REQUEST
-------

GET https://fuguefoundation.org/nonprofits

=======  ======
REQUEST  PARAMS
=======  ======
none
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl "https://fuguefoundation.org/nonprofits"


--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
name    name of the object
======  ======

BODY

.. code-block:: javascript

    This endpoint returns a `text/plain` response body.

==================
GET nonprofits/:id
==================
/api/v0/nonprofits/:id

Get JSON of nonprofit by id

-------
REQUEST
-------

GET https://fuguefoundation.org/nonprofits/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       example
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl "https://fuguefoundation.org/nonprofits/example"


--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
name    name of the object
======  ======

BODY

.. code-block:: javascript

    This endpoint returns a `text/plain` response body.

***********
classifiers
***********

===============
GET classifiers
===============
/api/v0/classifiers

Get JSON array of classifiers

-------
REQUEST
-------

GET https://fuguefoundation.org/classifiers

=======  ======
REQUEST  PARAMS
=======  ======
none
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl "https://fuguefoundation.org/classifiers"


--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
name    name of the object
======  ======

BODY

.. code-block:: javascript

    This endpoint returns a `text/plain` response body.

===================
GET classifiers/:id
===================
/api/v0/classifiers/:id

Get JSON of classifier by id

-------
REQUEST
-------

GET https://fuguefoundation.org/classifiers/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       example
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl "https://fuguefoundation.org/classifiers/example"


--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
name    name of the object
======  ======

BODY

.. code-block:: javascript

    This endpoint returns a `text/plain` response body.
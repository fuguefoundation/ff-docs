.. _ref-api:

########
API Docs
########
.. index:: ! Application Programming Interface

*API details, endpoint urls, and specification is a work in progress*

**********
nonprofits
**********

.. code-block:: javascript

    Schema({
        _id: mongoose.Schema.Types.ObjectId,
        classifier: {
            type: mongoose.Schema.Types.ObjectId,
            ref: 'Classifier',
            require: true
        },
        name: {type: String, required: true},
        url: {type: String, required: true},
        image: {type: String, required: true},
        logo: {type: String, required: true},
        desc: {type: String, required: true},
        short_desc: {type: String, required: true},
        stats: { 
            metric1: Number, 
            metric2: Number
        }
    });

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

=================
GET /:nonprofitId
=================
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

==============
POST nonprofit
==============
/api/v0/nonprofits

Get JSON of nonprofit by id

-------
REQUEST
-------

GET https://fuguefoundation.org/nonprofits

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

===================
PATCH /:nonprofitId
===================
/api/v0/nonprofits

Get JSON of nonprofit by id

-------
REQUEST
-------

GET https://fuguefoundation.org/nonprofits

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

====================
DELETE /:nonprofitId
====================
/api/v0/nonprofits/:nonprofitId

Get JSON of nonprofit by id

-------
REQUEST
-------

GET https://fuguefoundation.org/nonprofits

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

.. code-block:: javascript

    Schema({
        _id: mongoose.Schema.Types.ObjectId,
        name: {type: String, required: true},
        url: {type: String, required: true},
        image: {type: String, required: true},
        logo: {type: String, required: true},
        desc: {type: String, required: true},
        short_desc: {type: String, required: true}
    });

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

==================
GET /:classifierId
==================
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

===============
POST classifier
===============
/api/v0/classifiers

Get JSON of classifier by id

-------
REQUEST
-------

GET https://fuguefoundation.org/classifiers

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

====================
PATCH /:classifierId
====================
/api/v0/classifiers

Get JSON of classifier by id

-------
REQUEST
-------

GET https://fuguefoundation.org/classifiers

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

=====================
DELETE /:classifierId
=====================
/api/v0/classifiers/:classifierId

Get JSON of classifier by id

-------
REQUEST
-------

GET https://fuguefoundation.org/classifiers

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
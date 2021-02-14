.. _ref-api:

########
API Docs
########
.. index:: ! Application Programming Interface

See `API Github repo <https://github.com/fuguefoundation/ff-api>`_ for code base. *Docs under development*

**********
nonprofits
**********

.. code-block:: javascript

    Schema({
        _id: mongoose.Schema.Types.ObjectId,
        name: {type: String, required: true},
        url: {type: String, required: true},
        address: {type: String, required: true},
        logo: {type: String, required: true},
        image: {type: String, required: true},
        short_desc: {type: String, required: true},
        desc: {type: String, required: true},
        evaluatorId: {
            type: mongoose.Schema.Types.ObjectId,
            ref: 'Evaluator',
            require: true
        },
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

GET /api/v0/nonprofits

=======  ======
REQUEST  PARAMS
=======  ======
none
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl /api/v0/nonprofits

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
Array   [{nonprofits}]}
======  ======

BODY

This endpoint returns a `text/json` response body.

.. code-block:: javascript

    [{
        id: result.id,
        name: result.name,
        url: result.url,
        address: result.address,
        logo: result.logo,
        image: result.image,
        short_desc: result.short_desc,
        desc: result.desc,
        evaluatorId: result.evaluatorId,
        stats: result.stats,
        request: {
            type: 'GET',
            url: 'api/v0/nonprofits/' + result.id
        }
    }]

=================
GET /:nonprofitId
=================
/api/v0/nonprofits/:id

Get JSON of nonprofit by id

-------
REQUEST
-------

GET /api/v0/nonprofits/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl /api/v0/nonprofits/:id

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
Object  {nonprofit}
======  ======

BODY

.. code-block:: javascript

    This endpoint returns a `text/json` response body.

==============
POST nonprofit
==============
/api/v0/nonprofits

Post JSON of nonprofit

-------
REQUEST
-------

POST /api/v0/nonprofits

--------
RESPONSE
--------

On success, the call to this endpoint will return with 201 and the following body:

BODY

.. code-block:: javascript

    createdNonprofit: {
        name: result.name,                  
        _id: result._id,
        request: {
            type: 'GET',
            url: 'api/v0/nonprofits/' + result._id
        }
    }

===================
PATCH /:nonprofitId
===================
/api/v0/nonprofits/:id

Patch JSON of nonprofit by id

-------
REQUEST
-------

PATCH /api/v0/nonprofits/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl "https://fuguefoundation.org/nonprofits/example"

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

BODY

.. code-block:: javascript

    {
        message: 'Nonprofit updated',
        request: {
            type: 'GET',
            url: 'api/v0/nonprofits/' + id
        }
    }

====================
DELETE /:nonprofitId
====================
/api/v0/nonprofits/:id

Delete JSON of nonprofit by id

-------
REQUEST
-------

DELETE /api/v0/nonprofits/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

BODY

.. code-block:: javascript

    {
        message: 'Nonprofit deleted',
        request: {
            type: 'POST',
            url: 'api/v0/nonprofits',
            body: { name: 'String', url: 'String', address: 'String', url: 'String', image: 'String', 
            logo: 'String', desc: 'String', short_desc: 'String', evaluatorId: 'String',
            stats: {metric1: 'Number', metric2: 'Number'}}
        }
    }

**********
evaluators
**********

.. code-block:: javascript

    Schema({
        _id: mongoose.Schema.Types.ObjectId,
        name: {type: String, required: true},
        url: {type: String, required: true},
        image: {type: String, required: true},
        logo: {type: String, required: true},
        focus: {type: String, required: true},
        short_desc: {type: String, required: true},
        desc: {type: String, required: true}
    });

==============
GET evaluators
==============
/api/v0/evaluators

Get JSON array of evaluators

-------
REQUEST
-------

GET /api/v0/evaluators

=======  ======
REQUEST  PARAMS
=======  ======
none     none
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl /api/v0/evaluators

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
Array   [{evaluators}]
======  ======

BODY

.. code-block:: javascript

    [{
        id: result._id,
        name: result.name,
        url: result.url,
        logo: result.logo,
        image: result.image,
        focus: result.focus,
        short_desc: result.short_desc,
        desc: result.desc,
        request: {
            type: 'GET',
            url: 'api/v0/evaluators/' + result._id
        }
    }]

=================
GET /:evaluatorId
=================
/api/v0/evaluators/:id

Get JSON of evaluator by id

-------
REQUEST
-------

GET /api/v0/evaluators/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

EXAMPLE

.. code-block:: javascript

    // GET
    curl /api/v0/evaluators/:id

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

======  ======
RESULT  FIELDS
======  ======
Object  {evaluator}
======  ======

BODY

.. code-block:: javascript

    {
        id: result.id,
        name: result.name,
        url: result.url,
        logo: result.logo,
        image: result.image,
        focus: result.focus,
        short_desc: result.short_desc,
        desc: result.desc,
        request: {
            type: 'GET',
            description: 'Get all evaluators',
            url: 'api/v0/evaluators'
        }
    }

==============
POST evaluator
==============
/api/v0/evaluators

Post JSON of evaluator

-------
REQUEST
-------

POST /api/v0/evaluators

--------
RESPONSE
--------

On success, the call to this endpoint will return with 201 and the following body:

BODY

.. code-block:: javascript

    {
        message: "New evaluator created",
        createdEvaluator: {
            _id: result._id,
            name: result.name,
            request: {
                type: 'GET',
                url: '/api/v0/evaluators/' + result._id
            }
        }
    }

===================
PATCH /:evaluatorId
===================
/api/v0/evaluators/:id

Patch JSON of evaluator by id

-------
REQUEST
-------

PATCH /api/v0/evaluators/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

BODY

.. code-block:: javascript

    {
        message: 'Evaluator updated',
        request: {
            type: 'GET',
            url: 'api/v0/evaluators/' + id
        }
    }

====================
DELETE /:evaluatorId
====================
/api/v0/evaluators/:id

Delete JSON of evaluator by id

-------
REQUEST
-------

DELETE /api/v0/evaluators/:id

=======  ======
REQUEST  PARAMS
=======  ======
id       string
=======  ======

--------
RESPONSE
--------

On success, the call to this endpoint will return with 200 and the following body:

BODY

.. code-block:: javascript

    {
        message: 'Evaluator deleted',
        request: {
            type: 'POST',
            url: 'api/v0/evaluators',
            body: { name: 'String', url: 'String', image: 'String', 
            logo: 'String', desc: 'String', short_desc: 'String'}
        }
    }
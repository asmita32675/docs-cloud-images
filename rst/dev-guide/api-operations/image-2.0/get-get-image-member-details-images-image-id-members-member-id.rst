
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

Get Image Member Details
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    GET /images/{image_id}/members/{member_id}

Gets the details for the specified image member. 

This operation shows details of the image member. The response conforms to the schema found in `4.5.3. Get image members schema <http://docs.rackspace.com/images/api/v2/ci-devguide/content/GET_getImageMembersSchemas_schemas_members_Schema_Calls.html>`__.

To get a successful response, either the image owner must make the call or the ``tenant_id`` of the user making the call must match the specified ``member_id``. Otherwise the response is ``HTTP 404``.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |Success                  |Request succeeded.       |
+--------------------------+-------------------------+-------------------------+
|400                       |Error                    |A general error has      |
|                          |                         |occured.                 |
+--------------------------+-------------------------+-------------------------+
|401                       |Unauthorized             |Unauthorized.            |
+--------------------------+-------------------------+-------------------------+
|403                       |Forbidden                |Forbidden.               |
+--------------------------+-------------------------+-------------------------+
|405                       |Bad Method               |Bad method.              |
+--------------------------+-------------------------+-------------------------+
|413                       |Over Limit               |The number of items      |
|                          |                         |returned is above the    |
|                          |                         |allowed limit.           |
+--------------------------+-------------------------+-------------------------+
|503                       |Service Unavailable      |The requested service is |
|                          |                         |unavailable.             |
+--------------------------+-------------------------+-------------------------+
|500                       |API Fault                |API fault.               |
+--------------------------+-------------------------+-------------------------+
|404                       |Not Found                |Resource not found.      |
+--------------------------+-------------------------+-------------------------+


Request
""""""""""""""""

This table shows the URI parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|{image_id}                |csapi:uuid               |Image ID stored through  |
|                          |                         |the image API, typically |
|                          |                         |a UUID.                  |
+--------------------------+-------------------------+-------------------------+
|{member_id}               |xsd:string               |Image member ID. For     |
|                          |                         |example, the tenant ID   |
|                          |                         |of the user with whom    |
|                          |                         |the image is being       |
|                          |                         |shared.                  |
+--------------------------+-------------------------+-------------------------+








Response
""""""""""""""""


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|created_at                |xsd:string *(Required)*  |The date and time that   |
|                          |                         |the image member was     |
|                          |                         |created.                 |
+--------------------------+-------------------------+-------------------------+
|image_id                  |xsd:string *(Required)*  |The UUID of the image.   |
+--------------------------+-------------------------+-------------------------+
|member_id                 |xsd:string *(Required)*  |The id of the image      |
|                          |                         |member.                  |
+--------------------------+-------------------------+-------------------------+
|schema                    |xsd:string *(Required)*  |The schema of the image  |
|                          |                         |member.                  |
+--------------------------+-------------------------+-------------------------+
|status                    |xsd:string *(Required)*  |The status of the image  |
|                          |                         |member ( ``pending``,    |
|                          |                         |``accepted``, or         |
|                          |                         |``rejected``.            |
+--------------------------+-------------------------+-------------------------+
|updated_at                |xsd:string *(Required)*  |The date and time that   |
|                          |                         |the image member was     |
|                          |                         |updated.                 |
+--------------------------+-------------------------+-------------------------+





**Example Get Image Member Details: JSON response**


.. code::

    {
        "created_at": "2014-02-20T04:15:17Z",
        "image_id": "634985e5-0f2e-488e-bd7c-928d9a8ea82a",
        "member_id": "348129",
        "schema": "/v2/schemas/member",
        "status": "pending",
        "updated_at": "2014-02-20T04:15:17Z"
    }


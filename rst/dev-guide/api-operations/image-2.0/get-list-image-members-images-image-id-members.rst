
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

List Image Members
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    GET /images/{image_id}/members

Returns collection of members (users) with whom the image has been shared.

This operation returns collection of members (users) with whom the image has been shared. The response conforms to the schema found in `4.5.3. Get image members schema <http://docs.rackspace.com/images/api/v2/ci-devguide/content/GET_getImageMembersSchemas_schemas_members_Schema_Calls.html>`__.

If a user with whom this image is shared makes this call, the member list contains only information for that user. If a user with whom this image has not been shared makes this call, the response is ``HTTP 404``.



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








Response
""""""""""""""""


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|members                   |array *(Required)*       |The array of image       |
|                          |                         |members.                 |
+--------------------------+-------------------------+-------------------------+
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
|schema                    |xsd:string *(Required)*  |The schema of the image  |
|                          |                         |members.                 |
+--------------------------+-------------------------+-------------------------+





**Example List Image Members: JSON response**


.. code::

    {
        "members": [
            {
                "created_at": "2013-10-07T17:58:03Z",
                "image_id": "dbc999e3-c52f-4200-bedd-3b18fe7f87fe",
                "member_id": "123456789",
                "schema": "/v2/schemas/member",
                "status": "pending",
                "updated_at": "2013-10-07T17:58:03Z"
            },
            {
                "created_at": "2013-10-07T17:58:55Z",
                "image_id": "dbc999e3-c52f-4200-bedd-3b18fe7f87fe",
                "member_id": "987654321",
                "schema": "/v2/schemas/member",
                "status": "accepted",
                "updated_at": "2013-10-08T12:08:55Z"
            }
        ],
        "schema": "/v2/schemas/members"
    }


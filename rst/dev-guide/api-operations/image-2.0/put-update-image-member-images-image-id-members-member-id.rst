
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

Update Image Member
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    PUT /images/{image_id}/members/{member_id}

Sets the specified status for the specified member of the specified image.

This operation updates the image member. The response conforms to the schema found in `4.5.3. Get image members schema <http://docs.rackspace.com/images/api/v2/ci-devguide/content/GET_getImageMembersSchemas_schemas_members_Schema_Calls.html>`__.

If the call is made by the image owner, the response is ``HTTP 403 (Forbidden)``.

If the call is made by a user who is not the owner and whose ``tenant ID`` is not the same as the {member_id} is the operation URI, the response is ``HTTP 404``.



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
|415                       |Bad Media Type           |Bad media type. This may |
|                          |                         |result if the wrong      |
|                          |                         |media type is used in    |
|                          |                         |the cURL request.        |
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





This table shows the body parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|status                    |xsd:string *(Required)*  |The status to which this |
|                          |                         |image member should be   |
|                          |                         |set. Valid values are as |
|                          |                         |follows: ``pending``At   |
|                          |                         |creation, the member's   |
|                          |                         |status is set to         |
|                          |                         |pending. The image is    |
|                          |                         |not visible in the       |
|                          |                         |member's image-list, but |
|                          |                         |the member can still     |
|                          |                         |boot instances from the  |
|                          |                         |image. ``accepted``The   |
|                          |                         |image is visible in the  |
|                          |                         |member's image-list. The |
|                          |                         |member can boot          |
|                          |                         |instances from the       |
|                          |                         |image. ``rejected``The   |
|                          |                         |member has decided that  |
|                          |                         |he or she does not want  |
|                          |                         |to see the image. The    |
|                          |                         |image is not visible in  |
|                          |                         |the member's image-list, |
|                          |                         |but the member can still |
|                          |                         |boot instances from the  |
|                          |                         |image.                   |
+--------------------------+-------------------------+-------------------------+





**Example Update Image Member: JSON request**


.. code::

    {
        "status": "accepted"
    }


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





**Example Update Image Member: JSON response**


.. code::

    {
        "created_at": "2013-09-20T19:22:19Z",
        "image_id": "a96be11e-8536-4910-92cb-de50aa19dfe6",
        "member_id": "554433",
        "schema": "/v2/schemas/member",
        "status": "accepted",
        "updated_at": "2013-09-20T20:15:31Z"
    }


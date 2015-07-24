
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

Get Tasks Schema
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    GET /schemas/tasks

Gets a json-schema document that represents a container of tasks entities.

This operation returns a list of task entities. The following response is just an example. Consider the response to the API call as authoritative.



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


Request
""""""""""""""""









Response
""""""""""""""""





**Example Get Tasks Schema: JSON response**


.. code::

    {
        "links": [
            {
                "href": "{schema}", 
                "rel": "describedby"
            }
        ], 
        "name": "tasks", 
        "properties": {
            "schema": {
                "type": "string"
            }, 
            "tasks": {
                "items": {
                    "name": "task", 
                    "properties": {
                        "created_at": {
                            "description": "Datetime when this resource was created", 
                            "type": "string"
                        }, 
                        "expires_at": {
                            "description": "Datetime when this resource would be subject to removal", 
                            "type": "string"
                        }, 
                        "id": {
                            "description": "An identifier for the task", 
                            "pattern": "^([0-9a-fA-F]){8}-([0-9a-fA-F]){4}-([0-9a-fA-F]){4}-([0-9a-fA-F]){4}-([0-9a-fA-F]){12}$", 
                            "type": "string"
                        }, 
                        "owner": {
                            "description": "An identifier for the owner of this task", 
                            "type": "string"
                        }, 
                        "schema": {
                            "type": "string"
                        }, 
                        "self": {
                            "type": "string"
                        }, 
                        "status": {
                            "description": "The current status of this task", 
                            "enum": [
                                "pending", 
                                "processing", 
                                "success", 
                                "failure"
                            ], 
                            "type": "string"
                        }, 
                        "type": {
                            "description": "The type of task represented by this content", 
                            "enum": [
                                "import", 
                                "export"
                            ], 
                            "type": "string"
                        }, 
                        "updated_at": {
                            "description": "Datetime when this resource was updated", 
                            "type": "string"
                        }
                    }
                }, 
                "type": "array"
            }
        }
    }
    


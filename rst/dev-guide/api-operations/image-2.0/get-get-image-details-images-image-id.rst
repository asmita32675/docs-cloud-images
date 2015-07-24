
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

Get Image Details
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    GET /images/{image_id}

Gets the details for the specified image. 

This operation shows the details for the image. The response body is a single image entity and conforms to the schema found in `4.5.2. Get image schema <http://docs.rackspace.com/images/api/v2/ci-devguide/content/GET_getImageSchema_schemas_image_Schema_Calls.html>`__.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |                         |                         |
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

+----------------+---------------+---------------------------------------------+
|Name            |Type           |Description                                  |
+================+===============+=============================================+
|id              |xsd:string     |The UUID of the image.                       |
+----------------+---------------+---------------------------------------------+
|name            |xsd:string     |The name of the image.                       |
+----------------+---------------+---------------------------------------------+
|status          |xsd:string     |The status of the image. For possible image  |
|                |               |statuses, see ` 1.4.1. Image statuses        |
|                |               |<http://docs.rackspace.com/images/api/v2/ci- |
|                |               |devguide/content/image-statuses.html>`__.    |
+----------------+---------------+---------------------------------------------+
|visibility      |xsd:string     |Specifies image visibility as either         |
|                |               |``public``, ``private``, or ``shared``.      |
+----------------+---------------+---------------------------------------------+
|checksum        |xsd:string     |The checksum of the image.                   |
+----------------+---------------+---------------------------------------------+
|minRam          |xsd:string     |The minimum server RAM required for this     |
|                |               |image.                                       |
+----------------+---------------+---------------------------------------------+
|minDisk         |xsd:string     |The minimum server disk size required for    |
|                |               |this image.                                  |
+----------------+---------------+---------------------------------------------+
|tags            |array          |An array of user-defined image tags.         |
+----------------+---------------+---------------------------------------------+
|created_at      |xsd:string     |The date and time that the image was created.|
+----------------+---------------+---------------------------------------------+
|updated_at      |xsd:string     |The date and time that the image was updated.|
+----------------+---------------+---------------------------------------------+
|schema          |xsd:string     |The schema of the image.                     |
+----------------+---------------+---------------------------------------------+





**Example Get Image Details: JSON response**


.. code::

    {
    	"container_format": "ovf",
    	"min_ram": 512,
    	"updated_at": "2015-03-09T19:32:29Z",
    	"owner": "657197",
    	"file": "/v2/images/126a6674-6308-421f-801e-fc302ab4f53f/file",
    	"flavor_classes": "*,!onmetal",
    	"vm_mode": "hvm",
    	"id": "126a6674-6308-421f-801e-fc302ab4f53f",
    	"size": 758777106,
    	"os_distro": "centos",
    	"image_type": "base",
    	"self": "/v2/images/126a6674-6308-421f-801e-fc302ab4f53f",
    	"disk_format": "vhd",	
    	"schema": "/v2/schemas/image",
    	"status": "active",	
    	"tags": [],	
    	"visibility": "public",
    	"auto_disk_config": "disabled",
    	"min_disk": 20,
    	"name": "CentOS 7 (PVHVM)",
    	"checksum": "554bd2ad5b3a275c46b6d8983ae4da26",
    	"created_at": "2015-01-28T19:31:37Z",
    	"cache_in_nova": "True",
    	"protected": false,	
    	"os_type": "linux",
    	"com.rackspace__1__release_id": "220",
    	"com.rackspace__1__build_core": "1",
    	"com.rackspace__1__options": "0",
    	"com.rackspace__1__release_version": "10",
        "com.rackspace__1__platform_target": "PublicCloud",
    	"com.rackspace__1__build_managed": "1",
    	"com.rackspace__1__visible_managed": "0",
    	"com.rackspace__1__source": "kickstart",
    	"com.rackspace__1__ui_default_show": "True",
    	"com.rackspace__1__release_build_date": "2015-01-28_18-59-30",
    	"com.rackspace__1__visible_core": "0",
    	"com.rackspace__1__build_rackconnect": "1",
    	"com.rackspace__1__visible_rackconnect": "0",
    	"org.openstack__1__os_version": "7",
    	"org.openstack__1__architecture": "x64",
        "org.openstack__1__os_distro": "org.centos"
    }
    


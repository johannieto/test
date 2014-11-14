================
REST Service API
================
This document provides the necessary guidelines and few examples for using the Service API.

Customers End Points
====================

Search Customers
----------------
The endpoint returns customers for the parameters specified. 

**Example**

+----------------------------------------------------------------------------------------------------------+
| GET *https://{subdomain}.zent.io/api/v1/customer/search?apikey={api_key}&name=jhon&page=1&page_size=10*  |
+----------------------------------------------------------------------------------------------------------+

**Parameters**

 =========  ========  ======================================================================================================
 Name       Required  Description
 =========  ========  ======================================================================================================
 name       Yes       The customer's name.
 email      No        The customer's email.  
 phone      No        The customer's phone. 
 page       Yes       The result's page. 
 page_size  No        The result's page size. Defaults to 10.   
 sorting    No        The result's sorting. Possible values are *last_created* and *last_updated*. Defaults to last_updated.   
 =========  ========  ======================================================================================================

**Response Example**

::

    [
        {
            "id":"54652afd3896ede40a000000",
            "name":"Jhon Doe",
            "surname":null,
            "email":"jhon@gmail.com",
            "phone":"88888888888",
            "createdAt":"2014-11-13T17:04:45-05:00",
            "updatedAt":"2014-11-13T17:23:46-05:00",
            "customAttributes":[]
        },
        {
            "id":"54652f6f3896ed8018000000",
            "name":"Marissa Mayer",
            "surname":null,
            "email":"marissa@gmail.com",
            "phone":"9999999999999",
            "createdAt":"2014-11-13T17:23:43-05:00",
            "updatedAt":"2014-11-13T17:23:43-05:00",
            "customAttributes":[]
        }
    ]


Get Customer
----------------
The endpoint returns customers for the parameters specified. 

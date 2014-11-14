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
 name          yes    The customer's name.
 email         no     The customer's email.  
 phone         no     The customer's phone. 
 page          yes    The result's page. 
 page_size     no     The result's page size. Defaults to 10.   
 sorting       no     The result's sorting. Possible values are *last_created* and *last_updated*. Defaults to last_updated.   
 =========  ========  ======================================================================================================

**Response Sample**

::

    [
        {
            "id":"54652afd3896ede40a000000",
            "name":"Jhon",
            "surname":"Doe",
            "email":"jhon@gmail.com",
            "phone":"88888888888",
            "createdAt":"2014-11-13T17:04:45-05:00",
            "updatedAt":"2014-11-13T17:23:46-05:00",
            "customAttributes":[]
        },
        {
            "id":"54652f6f3896ed8018000000",
            "name":"Marissa",
            "surname":"Mayer",
            "email":"marissa@gmail.com",
            "phone":"9999999999999",
            "createdAt":"2014-11-13T17:23:43-05:00",
            "updatedAt":"2014-11-13T17:23:43-05:00",
            "customAttributes":[]
        },
        ...
    ]



Get Customer
------------
The endpoint returns a customer for the parameter specified.

**Example**

+-------------------------------------------------------------------------------------------------------+
| GET *https://{subdomain}.zent.io/api/v1/customer?apikey={api_key}&customer=54652afd3896ede40a000000*  |
+-------------------------------------------------------------------------------------------------------+

**Parameters**

 =========  ========  ======================================================================================================
 Name       Required  Description
 =========  ========  ======================================================================================================
 customer      yes    The customer's id or the customer's email.
 =========  ========  ======================================================================================================

**Response Sample**

::

    {
        "id":"54652afd3896ede40a000000",
        "name":"Jhon",
        "surname":"Doe",
        "email":"jhon@gmail.com",
        "phone":"88888888888",
        "createdAt":"2014-11-13T17:04:45-05:00",
        "updatedAt":"2014-11-13T17:23:46-05:00",
        "customAttributes":[]
    }



Get Customer Stories
--------------------
The endpoint returns the customer stories for the parameters specified.

**Example**

+----------------------------------------------------------------------------------------------------------+
| GET *https://{subdomain}.zent.io/api/v1/customer/search?apikey={api_key}&name=jhon&page=1&page_size=10*  |
+----------------------------------------------------------------------------------------------------------+

**Parameters**

 =========  ========  ======================================================================================================
 Name       Required  Description
 =========  ========  ======================================================================================================
 customer      yes    The customer's id or the customer's email.
 page          yes    The result's page.
 page_size     no     The result's page size. Defaults to 10.
 sorting       no     The result's sorting. Possible values are *last_created* and *last_updated*. Defaults to last_updated.
 =========  ========  ======================================================================================================

**Response Sample**

::

    [
        {
            "id":"546466313896ed7c21000000",
            "state":0,
            "subject":"My story subject",
            "createdAt":"2014-11-13T03:05:05-05:00"
        },
        {
            "id":"54646c653896ed1023000000",
            "state":0,
            "subject":"My story subject",
            "createdAt":"2014-11-13T03:31:33-05:00"
        },
        ...
    ]



Create Customer
---------------
The endpoint creates a customer for the parameters specified.

**Example**

+--------------------------------------------------------------------------+
| POST *https://{subdomain}.zent.io/api/v1/customer/new?apikey={api_key}*  |
+--------------------------------------------------------------------------+

**Parameters**

 =========  ========  ======================================================================================================
 Name       Required  Description
 =========  ========  ======================================================================================================
 name          yes    The customer's name.
 email         yes    The customer's email.  
 phone         yes    The customer's phone. 
 address       yes    The customer's address. 
 tags          no     The customer's tags.
 =========  ========  ======================================================================================================

**Response Sample**

::

    {
        "id":"546581583896ed8813000002",
    }



Update Customer
---------------
The endpoint updates a customer with the parameters specified.

**Example**

+-----------------------------------------------------------------------------+
| POST *https://{subdomain}.zent.io/api/v1/customer/update?apikey={api_key}*  |
+-----------------------------------------------------------------------------+

**Parameters**

 =========  ========  ======================================================================================================
 Name       Required  Description
 =========  ========  ======================================================================================================
 customer      yes    The customer's id or the customer's email.
 name          yes    The customer's name.
 email         yes    The customer's email.  
 phone         yes    The customer's phone. 
 address       yes    The customer's address. 
 tags          no     The customer's tags.
 =========  ========  ======================================================================================================

**Response Sample**

::

    {
        "id":"546581583896ed8813000002",
    }



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

+---------------------------------------------------------------------------------------------------------------+
| GET *https://{subdomain}.zent.io/api/v1/customer/search?apikey={your_api_key}&name=jhon&page=1&page_size=10*  |
+---------------------------------------------------------------------------------------------------------------+

**Parameters**

 =========  ========  ==================================================================================================
 Name       Required  Description
 =========  ========  ==================================================================================================
 name       Yes       The customer's name.
 email      No        The customer's email.  
 phone      No        The customer's phone. 
 page       Yes       The result's page. 
 page_size  No        The result's page size. Defaults to 10.   
 sorting    No        The result's sorting. Possible values are last_created and last_updated. Defaults to last_updated.   
 =========  ========  ==================================================================================================


+-------+----------+------------------------+
| Name  | Required | Description            |
+=======+==========+========================+
| name  | Yes      |  The customer's name   |
+-------+----------+------------------------+
| email | No       |  The customer's email  |
+-------+----------+------------------------+
| phone | No       |  The customer's phone  |
+-------+----------+------------------------+
| page  | Yes      |  The result's page     |
+-------+----------+------------------------+
| page_size | No   |  The result's page size. Defaults to 10.   |
+-------+----------+------------------------+
| sorting | No     |  The result's sorting. Possible values are last_created and last_updated. Defaults to last_updated.   |
+-------+----------+------------------------+



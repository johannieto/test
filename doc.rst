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

.. t3-field-list-table::
 :header-rows: 1

 - :File:
         File

   :Description:
         Description

 - :File:
         fe_adminLib.inc

   :Description:
         Main class used to display the frontend administration forms.

         Call it from a USER_INT cObject with 'userFunc =
         user_feAdmin->init'. See the static_templates for examples.

         **Note:** Using the USER_INT cObject allows the script to work
         regardless of the page-cache which is necessary!

 - :File:
         fe_admin_dmailsubscrip.tmpl

   :Description:
         Example template file for subscription to newsletters of users to the
         tt_address table. This template is used by the static_template
         'plugin.feadmin.dmailsubscription'.

**Parameters**

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



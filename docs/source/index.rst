.. doc_sc_api documentation master file, created by
   sphinx-quickstart on Wed Mar 21 10:08:40 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

==================================
SunCoast RHIO Api's documentation!
==================================


Access to Api
=============

Our sandbox api is available from this url :  *https://suncoastapi.herokuapp.com/apisc/{endpoint_here}*

In order to access our Api you will need a valid token provided from us.::

    curl -X GET \
        https://suncoastapi.herokuapp.com/apisc/{endpoint_here} \
        -H 'Authorization: Bearer Token_Here' \
        -H 'Content-Type: application/json' \

.. note::

    You will need to provide that token for accesing any enpoint in our Api.


Guide
*****

.. toctree::
   :maxdepth: 4


   Endpoints<endpoints/index>
   Help<help>



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

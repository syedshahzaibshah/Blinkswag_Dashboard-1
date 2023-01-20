Custom Functions
===============

.. _installation:

 

Function: convert_estimate_to_so
---------------------------------

:Module: Estimate

:Function: convert_estimate_to_so

:Workflow Rule: Convert Estimate To SO



Description : This code is used to take information from an estimate in Zoho Books and create a new sales order using that information. The script starts by retrieving the estimate ID and organization ID and then goes on to get more detailed information about the estimate, such as the project ID, contact persons, and other details. It then takes the line items from the estimate and updates their custom fields. The script also updates the custom fields of the estimate itself. Finally, it creates a new sales order using the information gathered from the estimate.

It basically is a way to automate the process of converting an estimate to a sales order in Zoho Books, it eliminates the need for manual entry of data and saves time.

* The script starts by getting the "estimate_id", "organization_id" and "customer_id" from the estimate object.

* Then, it uses the "zoho.books.getRecordsByID" method to retrieve detailed information about the estimate using the organization ID and estimate ID. It stores this     detailed. 


To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


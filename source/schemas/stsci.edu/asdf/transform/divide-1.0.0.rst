

.. _http://stsci.edu/schemas/asdf/transform/divide-1.0.0:

divide: Perform a list of subtransforms in parallel and then divide their results.
==================================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` any.

Perform a list of subtransforms in parallel and then divide their results.



Each of the subtransforms must have the same number of inputs and
outputs.

Invertibility: This transform is not automatically invertible.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/divide-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/divide-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A list of transforms, performed in parallel, and then combined through division.::

  !transform/divide-1.0.0
    forward:
      - !transform/generic-1.0.0
        n_inputs: 1
        n_outputs: 2
      - !transform/generic-1.0.0
        n_inputs: 1
        n_outputs: 2
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <divide-1.0.0.yaml>`
.. literalinclude:: divide-1.0.0.yaml
    :language: yaml
    :linenos:




.. _http://stsci.edu/schemas/asdf/transform/multiply-1.0.0:

multiply: Perform a list of subtransforms in parallel and then multiply their results.
======================================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` any.

Perform a list of subtransforms in parallel and then multiply their results.



Each of the subtransforms must have the same number of inputs and
outputs.

Invertibility: This transform is not automatically invertible.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/multiply-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/multiply-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A list of transforms, performed in parallel, and then combined through multiplication.::

  !transform/multiply-1.0.0
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

   :download:`[Download raw] <multiply-1.0.0.yaml>`
.. literalinclude:: multiply-1.0.0.yaml
    :language: yaml
    :linenos:


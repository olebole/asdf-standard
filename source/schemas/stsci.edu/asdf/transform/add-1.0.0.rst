

.. _http://stsci.edu/schemas/asdf/transform/add-1.0.0:

add: Perform a list of subtransforms in parallel and then add their results together.
=====================================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` any.

Perform a list of subtransforms in parallel and then add their results together.



Each of the subtransforms must have the same number of inputs and
outputs.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/add-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/add-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A list of transforms, performed in parallel and added together::

  !transform/add-1.0.0
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

   :download:`[Download raw] <add-1.0.0.yaml>`
.. literalinclude:: add-1.0.0.yaml
    :language: yaml
    :linenos:


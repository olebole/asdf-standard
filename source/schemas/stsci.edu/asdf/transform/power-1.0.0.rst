

.. _http://stsci.edu/schemas/asdf/transform/power-1.0.0:

power: Perform a list of subtransforms in parallel and then raise each result to the power of the next.
=======================================================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` any.

Perform a list of subtransforms in parallel and then raise each result to the power of the next.



Each of the subtransforms must have the same number of inputs and
outputs.

Invertibility: This transform is not automatically invertible.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/power-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/power-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <power-1.0.0.yaml>`
.. literalinclude:: power-1.0.0.yaml
    :language: yaml
    :linenos:


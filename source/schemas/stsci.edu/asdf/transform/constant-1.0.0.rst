

.. _http://stsci.edu/schemas/asdf/transform/constant-1.0.0:

constant: A transform that takes no inputs and always outputs a constant value.
===============================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

A transform that takes no inputs and always outputs a constant value.



Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform, which always outputs zero values.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/constant-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/constant-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/constant-1.0.0/allOf/1/properties/value:

    :entry:`value`

    :soft:`Type:` number. Required.

    

    

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <constant-1.0.0.yaml>`
.. literalinclude:: constant-1.0.0.yaml
    :language: yaml
    :linenos:


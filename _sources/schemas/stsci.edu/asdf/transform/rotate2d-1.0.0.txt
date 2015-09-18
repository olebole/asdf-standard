

.. _http://stsci.edu/schemas/asdf/transform/rotate2d-1.0.0:

rotate2d: A 2D rotation.
========================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

A 2D rotation.



A 2D rotation around the origin, in degrees.
Invertibility: All ASDF tools are required to be able to compute the analytic inverse of this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/rotate2d-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/rotate2d-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/rotate2d-1.0.0/allOf/1/properties/angle:

    :entry:`angle`

    :soft:`Type:` number. Required.

    

    Angle, in degrees.
    
    

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <rotate2d-1.0.0.yaml>`
.. literalinclude:: rotate2d-1.0.0.yaml
    :language: yaml
    :linenos:


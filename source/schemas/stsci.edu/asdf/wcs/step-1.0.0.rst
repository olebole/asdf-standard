

.. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0:

step: Describes a single step of a WCS transform pipeline.
==========================================================

:soft:`Type:` object.

Describes a single step of a WCS transform pipeline.





:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/frame:

  :entry:`frame`

  :soft:`Type:` string :soft:`or` :doc:`frame-1.0.0 <frame-1.0.0>`. Required.

  

  The frame of the inputs to the transform.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/frame/anyOf/0:

    :entry:`—`

    :soft:`Type:` string.

    

    



    .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/frame/anyOf/1:

    :entry:`—`

    :soft:`Type:` :doc:`frame-1.0.0 <frame-1.0.0>`.

    

    



  .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/transform:

  :entry:`transform`

  :soft:`Type:` :doc:`transform-1.0.0 <../transform/transform-1.0.0>` :soft:`or` null.

  

  The transform from this step to the next one.  The
  last step in a WCS should not have a transform, but
  exists only to describe the frames and units of the
  final output axes.
  
  

  :soft:`Default:` null

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/transform/anyOf/0:

    :entry:`—`

    :soft:`Type:` :doc:`transform-1.0.0 <../transform/transform-1.0.0>`.

    

    



    .. _http://stsci.edu/schemas/asdf/wcs/step-1.0.0/properties/transform/anyOf/1:

    :entry:`—`

    :soft:`Type:` null.

    

    

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <step-1.0.0.yaml>`
.. literalinclude:: step-1.0.0.yaml
    :language: yaml
    :linenos:


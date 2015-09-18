

.. _http://stsci.edu/schemas/asdf/transform/pseudocylindrical-1.0.0:

pseudocylindrical: Base class of all pseudocylindrical projections.
===================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Base class of all pseudocylindrical projections.



Pseudocylindrical projections are like cylindrical projections
except the parallels of latitude are projected at diminishing
lengths toward the polar regions in order to reduce lateral
distortion there.  Consequently, the meridians are curved.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/pseudocylindrical-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/pseudocylindrical-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/pseudocylindrical-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <pseudocylindrical-1.0.0.yaml>`
.. literalinclude:: pseudocylindrical-1.0.0.yaml
    :language: yaml
    :linenos:


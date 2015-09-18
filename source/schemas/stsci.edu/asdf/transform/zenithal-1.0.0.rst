

.. _http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0:

zenithal: Base class of all zenithal (or azimuthal) projections.
================================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Base class of all zenithal (or azimuthal) projections.



Zenithal projections are completely specified by defining the radius
as a function of native latitude, :math:`R_\theta`.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \arg(-y, x) \\
   R_\theta &= \sqrt{x^2 + y^2}

and the inverse (sky-to-pixel) is defined as:

.. math:: 

   x &= R_\theta \sin \phi \\
   y &= R_\theta \cos \phi



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <zenithal-1.0.0.yaml>`
.. literalinclude:: zenithal-1.0.0.yaml
    :language: yaml
    :linenos:


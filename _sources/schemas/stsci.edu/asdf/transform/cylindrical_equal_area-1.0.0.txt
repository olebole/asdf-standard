

.. _http://stsci.edu/schemas/asdf/transform/cylindrical_equal_area-1.0.0:

cylindrical_equal_area: The cylindrical equal area projection.
==============================================================

:soft:`Type:` :doc:`cylindrical-1.0.0 <cylindrical-1.0.0>` :soft:`and` object.

The cylindrical equal area projection.



Corresponds to the :code:`CEA` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= x \\
   \theta &= \sin^{-1}\left(\frac{\pi}{180^{\circ}}\lambda y\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \phi \\
   y &= \frac{180^{\circ}}{\pi}\frac{\sin \theta}{\lambda}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/cylindrical_equal_area-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`cylindrical-1.0.0 <cylindrical-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/cylindrical_equal_area-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/cylindrical_equal_area-1.0.0/allOf/1/properties/lambda:

    :entry:`lambda`

    :soft:`Type:` number.

    

    Radius of the cylinder in spherical radii, default is 0.
    
    

    :soft:`Default:` 0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <cylindrical_equal_area-1.0.0.yaml>`
.. literalinclude:: cylindrical_equal_area-1.0.0.yaml
    :language: yaml
    :linenos:


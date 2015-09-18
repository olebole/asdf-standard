

.. _http://stsci.edu/schemas/asdf/transform/cylindrical_perspective-1.0.0:

cylindrical_perspective: The cylindrical perspective projection.
================================================================

:soft:`Type:` :doc:`cylindrical-1.0.0 <cylindrical-1.0.0>` :soft:`and` object.

The cylindrical perspective projection.



Corresponds to the :code:`CYP` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \frac{x}{\lambda} \\
   \theta &= \arg(1, \eta) + \sin{-1}\left(\frac{\eta \mu}{\sqrt{\eta^2 + 1}}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \lambda \phi \\
   y &= \frac{180^{\circ}}{\pi}\left(\frac{\mu + \lambda}{\mu + \cos \theta}\right)\sin \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/cylindrical_perspective-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`cylindrical-1.0.0 <cylindrical-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/cylindrical_perspective-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/cylindrical_perspective-1.0.0/allOf/1/properties/mu:

    :entry:`mu`

    :soft:`Type:` number.

    

    Distance from center of sphere in the direction opposite the
    projected surface, in spherical radii.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/transform/cylindrical_perspective-1.0.0/allOf/1/properties/lambda:

    :entry:`lambda`

    :soft:`Type:` number.

    

    Radius of the cylinder in spherical radii, default is 0.
    
    

    :soft:`Default:` 0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <cylindrical_perspective-1.0.0.yaml>`
.. literalinclude:: cylindrical_perspective-1.0.0.yaml
    :language: yaml
    :linenos:


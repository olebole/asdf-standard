

.. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0:

slant_zenithal_perspective: The slant zenithal perspective projection.
======================================================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>` :soft:`and` object.

The slant zenithal perspective projection.



Corresponds to the :code:`SZP` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = \tan^{-1}\left(\frac{180^{\circ}}{\pi R_\theta}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\cot \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0/allOf/1/properties/mu:

    :entry:`mu`

    :soft:`Type:` number.

    

    Distance from point of projection to center of sphere in
    spherical radii.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0/allOf/1/properties/phi0:

    :entry:`phi0`

    :soft:`Type:` number.

    

    The longitude :math:`\phi_0` of the reference point, in degrees.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/transform/slant_zenithal_perspective-1.0.0/allOf/1/properties/theta0:

    :entry:`theta0`

    :soft:`Type:` number.

    

    The latitude :math:`\theta_0` of the reference point, in degrees.
    
    

    :soft:`Default:` 90

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <slant_zenithal_perspective-1.0.0.yaml>`
.. literalinclude:: slant_zenithal_perspective-1.0.0.yaml
    :language: yaml
    :linenos:


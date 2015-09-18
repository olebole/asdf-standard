

.. _http://stsci.edu/schemas/asdf/transform/zenithal_perspective-1.0.0:

zenithal_perspective: The zenithal perspective projection.
==========================================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>` :soft:`and` object.

The zenithal perspective projection.



Corresponds to the :code:`AZP` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \arg(-y \cos \gamma, x) \\
   \theta &= \left\{\genfrac{}{}{0pt}{}{\psi - \omega}{\psi + \omega + 180^{\circ}}\right.

where:

.. math:: 

   \psi &= \arg(\rho, 1) \\
   \omega &= \sin^{-1}\left(\frac{\rho \mu}{\sqrt{\rho^2 + 1}}\right) \\
   \rho &= \frac{R}{\frac{180^{\circ}}{\pi}(\mu + 1) + y \sin \gamma} \\
   R &= \sqrt{x^2 + y^2 \cos^2 \gamma}

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= R \sin \phi \\
   y &= -R \sec \gamma \cos \theta

where:

.. math:: 

   R = \frac{180^{\circ}}{\pi} \frac{(\mu + 1) \cos \theta}{(\mu + \sin \theta) + \cos \theta \cos \phi \tan \gamma}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/zenithal_perspective-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/zenithal_perspective-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/zenithal_perspective-1.0.0/allOf/1/properties/mu:

    :entry:`mu`

    :soft:`Type:` number.

    

    Distance from point of projection to center of sphere in
    spherical radii.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/transform/zenithal_perspective-1.0.0/allOf/1/properties/gamma:

    :entry:`gamma`

    :soft:`Type:` number.

    

    Look angle, in degrees.
    
    

    :soft:`Default:` 0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <zenithal_perspective-1.0.0.yaml>`
.. literalinclude:: zenithal_perspective-1.0.0.yaml
    :language: yaml
    :linenos:


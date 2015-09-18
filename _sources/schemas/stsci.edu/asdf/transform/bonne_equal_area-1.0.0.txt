

.. _http://stsci.edu/schemas/asdf/transform/bonne_equal_area-1.0.0:

bonne_equal_area: Bonne's equal area pseudoconic projection.
============================================================

:soft:`Type:` :doc:`pseudoconic-1.0.0 <pseudoconic-1.0.0>` :soft:`and` object.

Bonne's equal area pseudoconic projection.



Corresponds to the :code:`BON` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \frac{\pi}{180^\circ} A_\phi R_\theta / \cos \theta \\
     \theta &= Y_0 - R_\theta

where:

.. math:: 

   R_\theta &= \mathrm{sign} \theta_1 \sqrt{x^2 + (Y_0 - y)^2} \\
     A_\phi &= \arg\left(\frac{Y_0 - y}{R_\theta}, \frac{x}{R_\theta}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= R_\theta \sin A_\phi \\
     y &= -R_\theta \cos A_\phi + Y_0

where:

.. math:: 

   A_\phi &= \frac{180^\circ}{\pi R_\theta} \phi \cos \theta \\
     R_\theta &= Y_0 - \theta \\
     Y_0 &= \frac{180^\circ}{\pi} \cot \theta_1 + \theta_1

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/bonne_equal_area-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`pseudoconic-1.0.0 <pseudoconic-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/bonne_equal_area-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/bonne_equal_area-1.0.0/allOf/1/properties/theta1:

    :entry:`theta1`

    :soft:`Type:` number.

    

    Bonne conformal latitude, in degrees.
    
    

    :soft:`Default:` 0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <bonne_equal_area-1.0.0.yaml>`
.. literalinclude:: bonne_equal_area-1.0.0.yaml
    :language: yaml
    :linenos:


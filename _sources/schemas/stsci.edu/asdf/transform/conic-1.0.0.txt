

.. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0:

conic: Base class of all conic projections.
===========================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` object.

Base class of all conic projections.



In conic projections, the sphere is thought to be projected onto the
surface of a cone which is then opened out.

In a general sense, the pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \arg\left(\frac{Y_0 - y}{R_\theta}, \frac{x}{R_\theta}\right) / C \\
     R_\theta &= \mathrm{sign} \theta_a \sqrt{x^2 + (Y_0 - y)^2}

and the inverse (sky-to-pixel) is defined as:

.. math:: 

   x &= R_\theta \sin (C \phi) \\
     y &= R_\theta \cos (C \phi) + Y_0

where :math:`C` is the "constant of the cone":

.. math:: 

   C = \frac{180^\circ \cos \theta}{\pi R_\theta}



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0/allOf/1/properties/direction:

    :entry:`direction`

    :soft:`Type:` any :soft:`from` ["pix2sky", "sky2pix"].

    

    

    :soft:`Default:` "pix2sky"



    .. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0/allOf/1/properties/sigma:

    :entry:`sigma`

    :soft:`Type:` number.

    

    :math:`(\theta_1 + \theta_2) / 2` where :math:`\theta_1` and :math:`\theta_2`
    are the latitudes of the standard parallels, in degrees.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/transform/conic-1.0.0/allOf/1/properties/delta:

    :entry:`delta`

    :soft:`Type:` number.

    

    :math:`(\theta_1 - \theta_2) / 2` where :math:`\theta_1` and :math:`\theta_2`
    are the latitudes of the standard parallels, in degrees.
    
    

    :soft:`Default:` 0

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <conic-1.0.0.yaml>`
.. literalinclude:: conic-1.0.0.yaml
    :language: yaml
    :linenos:


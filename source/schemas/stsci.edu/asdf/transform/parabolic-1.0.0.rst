

.. _http://stsci.edu/schemas/asdf/transform/parabolic-1.0.0:

parabolic: Parabolic projection.
================================

:soft:`Type:` :doc:`pseudocylindrical-1.0.0 <pseudocylindrical-1.0.0>`.

Parabolic projection.



Corresponds to the :code:`PAR` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \frac{180^\circ}{\pi} \frac{x}{1 - 4(y / 180^\circ)^2} \\
     \theta &= 3 \sin^{-1}\left(\frac{y}{180^\circ}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \phi \left(2\cos\frac{2\theta}{3} - 1\right) \\
     y &= 180^\circ \sin \frac{\theta}{3}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <parabolic-1.0.0.yaml>`
.. literalinclude:: parabolic-1.0.0.yaml
    :language: yaml
    :linenos:




.. _http://stsci.edu/schemas/asdf/transform/molleweide-1.0.0:

molleweide: Molleweide's projection.
====================================

:soft:`Type:` :doc:`pseudocylindrical-1.0.0 <pseudocylindrical-1.0.0>`.

Molleweide's projection.



Corresponds to the :code:`MOL` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \frac{\pi x}{2 \sqrt{2 - \left(\frac{\pi}{180^\circ}y\right)^2}} \\
     \theta &= \sin^{-1}\left(\frac{1}{90^\circ}\sin^{-1}\left(\frac{\pi}{180^\circ}\frac{y}{\sqrt{2}}\right) + \frac{y}{180^\circ}\sqrt{2 - \left(\frac{\pi}{180^\circ}y\right)^2}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \frac{2 \sqrt{2}}{\pi} \phi \cos \gamma \\
     y &= \sqrt{2} \frac{180^\circ}{\pi} \sin \gamma

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <molleweide-1.0.0.yaml>`
.. literalinclude:: molleweide-1.0.0.yaml
    :language: yaml
    :linenos:


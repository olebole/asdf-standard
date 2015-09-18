

.. _http://stsci.edu/schemas/asdf/transform/hammer_aitoff-1.0.0:

hammer_aitoff: Hammer-Aitoff projection.
========================================

:soft:`Type:` :doc:`pseudocylindrical-1.0.0 <pseudocylindrical-1.0.0>`.

Hammer-Aitoff projection.



Corresponds to the :code:`AIT` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= 2 \arg \left(2Z^2 - 1, \frac{\pi}{180^\circ} \frac{Z}{2}x\right) \\
     \theta &= \sin^{-1}\left(\frac{\pi}{180^\circ}yZ\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= 2 \gamma \cos \theta \sin \frac{\phi}{2} \\
     y &= \gamma \sin \theta

where:

.. math:: 

   \gamma = \frac{180^\circ}{\pi} \sqrt{\frac{2}{1 + \cos \theta \cos(\phi / 2)}}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <hammer_aitoff-1.0.0.yaml>`
.. literalinclude:: hammer_aitoff-1.0.0.yaml
    :language: yaml
    :linenos:


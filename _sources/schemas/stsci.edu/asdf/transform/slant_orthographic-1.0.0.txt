

.. _http://stsci.edu/schemas/asdf/transform/slant_orthographic-1.0.0:

slant_orthographic: The slant orthographic projection.
======================================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

The slant orthographic projection.



Corresponds to the :code:`SIN` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = \cos^{-1}\left(\frac{\pi}{180^{\circ}}R_\theta\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\cos \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <slant_orthographic-1.0.0.yaml>`
.. literalinclude:: slant_orthographic-1.0.0.yaml
    :language: yaml
    :linenos:




.. _http://stsci.edu/schemas/asdf/transform/stereographic-1.0.0:

stereographic: The stereographic projection.
============================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

The stereographic projection.



Corresponds to the :code:`STG` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = 90^{\circ} - 2 \tan^{-1}\left(\frac{\pi R_\theta}{360^{\circ}}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = \frac{180^{\circ}}{\pi}\frac{2 \cos \theta}{1 + \sin \theta}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <stereographic-1.0.0.yaml>`
.. literalinclude:: stereographic-1.0.0.yaml
    :language: yaml
    :linenos:


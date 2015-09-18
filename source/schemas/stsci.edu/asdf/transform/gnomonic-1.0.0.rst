

.. _http://stsci.edu/schemas/asdf/transform/gnomonic-1.0.0:

gnomonic: The gnomonic projection.
==================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

The gnomonic projection.



Corresponds to the :code:`TAN` projection in the FITS WCS standard.

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



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <gnomonic-1.0.0.yaml>`
.. literalinclude:: gnomonic-1.0.0.yaml
    :language: yaml
    :linenos:




.. _http://stsci.edu/schemas/asdf/transform/zenithal_equal_area-1.0.0:

zenithal_equal_area: The zenithal equal area projection.
========================================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

The zenithal equal area projection.



Corresponds to the :code:`ZEA` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = 90^\circ - 2 \sin^{-1} \left(\frac{\pi R_\theta}{360^\circ}\right)

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta &= \frac{180^\circ}{\pi} \sqrt{2(1 - \sin\theta)} \\
              &= \frac{360^\circ}{\pi} \sin\left(\frac{90^\circ - \theta}{2}\right)

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <zenithal_equal_area-1.0.0.yaml>`
.. literalinclude:: zenithal_equal_area-1.0.0.yaml
    :language: yaml
    :linenos:


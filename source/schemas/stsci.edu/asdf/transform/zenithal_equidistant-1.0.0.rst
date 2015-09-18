

.. _http://stsci.edu/schemas/asdf/transform/zenithal_equidistant-1.0.0:

zenithal_equidistant: The zenithal equidistant projection.
==========================================================

:soft:`Type:` :doc:`zenithal-1.0.0 <zenithal-1.0.0>`.

The zenithal equidistant projection.



Corresponds to the :code:`ARC` projection in the FITS WCS standard.

See
:ref:`zenithal <http://stsci.edu/schemas/asdf/transform/zenithal-1.0.0>`
for the definition of the full transformation.

The pixel-to-sky transformation is defined as:

.. math:: 

   \theta = 90^\circ - R_\theta

And the sky-to-pixel transformation is defined as:

.. math:: 

   R_\theta = 90^\circ - \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <zenithal_equidistant-1.0.0.yaml>`
.. literalinclude:: zenithal_equidistant-1.0.0.yaml
    :language: yaml
    :linenos:


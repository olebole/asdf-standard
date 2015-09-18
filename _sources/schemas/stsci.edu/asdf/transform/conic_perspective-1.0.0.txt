

.. _http://stsci.edu/schemas/asdf/transform/conic_perspective-1.0.0:

conic_perspective: Colles' conic perspecitve projection.
========================================================

:soft:`Type:` :doc:`conic-1.0.0 <conic-1.0.0>`.

Colles' conic perspecitve projection.



Corresponds to the :code:`COP` projection in the FITS WCS standard.

See
:ref:`conic <http://stsci.edu/schemas/asdf/transform/conic-1.0.0>`
for the definition of the full transformation.

The transformation is defined as:

.. math:: 

   C &= \sin \theta_a \\
     R_\theta &= \frac{180^\circ}{\pi} \cos \eta [ \cot \theta_a - \tan(\theta - \theta_a)] \\
     Y_0 &= \frac{180^\circ}{\pi} \cos \eta \cot \theta_a

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <conic_perspective-1.0.0.yaml>`
.. literalinclude:: conic_perspective-1.0.0.yaml
    :language: yaml
    :linenos:


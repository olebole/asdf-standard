

.. _http://stsci.edu/schemas/asdf/transform/conic_equidistant-1.0.0:

conic_equidistant: Conic equidistant projection.
================================================

:soft:`Type:` :doc:`conic-1.0.0 <conic-1.0.0>`.

Conic equidistant projection.



Corresponds to the :code:`COD` projection in the FITS WCS standard.

See
:ref:`conic <http://stsci.edu/schemas/asdf/transform/conic-1.0.0>`
for the definition of the full transformation.

The transformation is defined as:

.. math:: 

   C &= \frac{180^\circ}{\pi} \frac{\sin\theta_a\sin\eta}{\eta} \\
     R_\theta &= \theta_a - \theta + \eta\cot\eta\cot\theta_a \\
     Y_0 = \eta\cot\eta\cot\theta_a

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <conic_equidistant-1.0.0.yaml>`
.. literalinclude:: conic_equidistant-1.0.0.yaml
    :language: yaml
    :linenos:


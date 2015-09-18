

.. _http://stsci.edu/schemas/asdf/transform/conic_equal_area-1.0.0:

conic_equal_area: Alber's conic equal area projection.
======================================================

:soft:`Type:` :doc:`conic-1.0.0 <conic-1.0.0>`.

Alber's conic equal area projection.



Corresponds to the :code:`COE` projection in the FITS WCS standard.

See
:ref:`conic <http://stsci.edu/schemas/asdf/transform/conic-1.0.0>`
for the definition of the full transformation.

The transformation is defined as:

.. math:: 

   C &= \gamma / 2 \\
     R_\theta &= \frac{180^\circ}{\pi} \frac{2}{\gamma} \sqrt{1 + \sin \theta_1 \sin \theta_2 - \gamma \sin \theta} \\
     Y_0 &= \frac{180^\circ}{\pi} \frac{2}{\gamma} \sqrt{1 + \sin \theta_1 \sin \theta_2 - \gamma \sin((\theta_1 + \theta_2)/2)}

where:

.. math:: 

   \gamma = \sin \theta_1 + \sin \theta_2

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <conic_equal_area-1.0.0.yaml>`
.. literalinclude:: conic_equal_area-1.0.0.yaml
    :language: yaml
    :linenos:


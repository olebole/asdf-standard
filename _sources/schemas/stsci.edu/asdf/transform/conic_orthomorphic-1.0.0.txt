

.. _http://stsci.edu/schemas/asdf/transform/conic_orthomorphic-1.0.0:

conic_orthomorphic: Conic orthomorphic projection.
==================================================

:soft:`Type:` :doc:`conic-1.0.0 <conic-1.0.0>`.

Conic orthomorphic projection.



Corresponds to the :code:`COO` projection in the FITS WCS standard.

See
:ref:`conic <http://stsci.edu/schemas/asdf/transform/conic-1.0.0>`
for the definition of the full transformation.

The transformation is defined as:

.. math:: 

   C &= \frac{\ln \left( \frac{\cos\theta_2}{\cos\theta_1} \right)}
               {\ln \left[ \frac{\tan\left(\frac{90^\circ-\theta_2}{2}\right)}
                                {\tan\left(\frac{90^\circ-\theta_1}{2}\right)} \right] } \\
     R_\theta &= \psi \left[ \tan \left( \frac{90^\circ - \theta}{2} \right) \right]^C \\
     Y_0 &= \psi \left[ \tan \left( \frac{90^\circ - \theta_a}{2} \right) \right]^C

where:

.. math:: 

   \psi = \frac{180^\circ}{\pi} \frac{\cos \theta}
            {C\left[\tan\left(\frac{90^\circ-\theta}{2}\right)\right]^C}

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <conic_orthomorphic-1.0.0.yaml>`
.. literalinclude:: conic_orthomorphic-1.0.0.yaml
    :language: yaml
    :linenos:


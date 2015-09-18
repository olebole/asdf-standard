

.. _http://stsci.edu/schemas/asdf/transform/sanson_flamsteed-1.0.0:

sanson_flamsteed: The Sanson-Flamsteed projection.
==================================================

:soft:`Type:` :doc:`pseudocylindrical-1.0.0 <pseudocylindrical-1.0.0>`.

The Sanson-Flamsteed projection.



Corresponds to the :code:`SFL` projection in the FITS WCS standard.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= \frac{x}{\cos y} \\
     \theta &= y

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \phi \cos \theta \\
     y &= \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <sanson_flamsteed-1.0.0.yaml>`
.. literalinclude:: sanson_flamsteed-1.0.0.yaml
    :language: yaml
    :linenos:


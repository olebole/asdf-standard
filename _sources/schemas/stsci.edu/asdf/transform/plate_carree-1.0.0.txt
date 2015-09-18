

.. _http://stsci.edu/schemas/asdf/transform/plate_carree-1.0.0:

plate_carree: The plate carrée projection.
==========================================

:soft:`Type:` :doc:`cylindrical-1.0.0 <cylindrical-1.0.0>`.

The plate carrée projection.



Corresponds to the :code:`CAR` projection in the FITS WCS standard.

The main virtue of this transformation is its simplicity.

The pixel-to-sky transformation is defined as:

.. math:: 

   \phi &= x \\
   \theta &= y

And the sky-to-pixel transformation is defined as:

.. math:: 

   x &= \phi \\
   y &= \theta

Invertibility: All ASDF tools are required to provide the inverse of
this transform.



Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <plate_carree-1.0.0.yaml>`
.. literalinclude:: plate_carree-1.0.0.yaml
    :language: yaml
    :linenos:


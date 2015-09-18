

.. _http://stsci.edu/schemas/asdf/transform/compose-1.0.0:

compose: Perform a list of subtransforms in series.
===================================================

:soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>` :soft:`and` any.

Perform a list of subtransforms in series.



The output of each subtransform is fed into the input of the next
subtransform.

The number of output dimensions of each subtransform must be equal
to the number of input dimensions of the next subtransform in list.
To reorder or add/drop axes, insert :code:`remap_axes` transforms in the
subtransform list.

Invertibility: All ASDF tools are required to be able to compute the
analytic inverse of this transform, by reversing the list of
transforms and applying the inverse of each.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/transform/compose-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  



  .. _http://stsci.edu/schemas/asdf/transform/compose-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` any.

  

  

:category:`Examples:`

A series of transforms::

  !transform/compose-1.0.0
    forward:
      - !transform/generic-1.0.0
        n_inputs: 1
        n_outputs: 2
      - !transform/generic-1.0.0
        n_inputs: 2
        n_outputs: 1
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <compose-1.0.0.yaml>`
.. literalinclude:: compose-1.0.0.yaml
    :language: yaml
    :linenos:


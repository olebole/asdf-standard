

.. _http://stsci.edu/schemas/asdf/wcs/wcs-1.0.0:

wcs: A system for describing generalized world coordinate transformations.
==========================================================================

:soft:`Type:` object.

A system for describing generalized world coordinate transformations.



ASDF WCS is a way of specifying transformations (usually from detector space to world coordinate space and back) by using the transformations in the :code:`transform-schema` module.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/wcs/wcs-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string. Required.

  

  A descriptive name for this WCS.
  
  



  .. _http://stsci.edu/schemas/asdf/wcs/wcs-1.0.0/properties/steps:

  :entry:`steps`

  :soft:`Type:` array :soft:`of` ( :doc:`step-1.0.0 <step-1.0.0>` ). Required.

  

  A list of steps in the forward transformation from detector to
  world coordinates.
  The inverse transformation is determined automatically by
  reversing this list, and inverting each of the individual
  transforms according to the rules described in
  :ref:`inverse <http://stsci.edu/schemas/asdf/transform/transform-1.0.0/properties/inverse>`.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/wcs/wcs-1.0.0/properties/steps/items:

    :soft:`Type:` :doc:`step-1.0.0 <step-1.0.0>`.

    

    

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <wcs-1.0.0.yaml>`
.. literalinclude:: wcs-1.0.0.yaml
    :language: yaml
    :linenos:


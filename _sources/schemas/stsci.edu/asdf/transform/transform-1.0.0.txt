

.. _http://stsci.edu/schemas/asdf/transform/transform-1.0.0:

transform: A generic type used to mark where other transforms are accepted.
===========================================================================

:soft:`Type:` object.

A generic type used to mark where other transforms are accepted.



These objects are designed to be nested in arbitrary ways to build up transformation pipelines out of a number of low-level pieces.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/transform/transform-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string.

  

  A user-friendly name for the transform, to give it extra
  meaning.
  
  



  .. _http://stsci.edu/schemas/asdf/transform/transform-1.0.0/properties/domain:

  :entry:`domain`

  :soft:`Type:` array :soft:`of` ( :doc:`domain-1.0.0 <domain-1.0.0>` ).

  

  The domain (range of valid inputs) to the transform.
  Each entry in the list corresponds to an input dimension.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/transform/transform-1.0.0/properties/domain/items:

    :soft:`Type:` :doc:`domain-1.0.0 <domain-1.0.0>`.

    

    



  .. _http://stsci.edu/schemas/asdf/transform/transform-1.0.0/properties/inverse:

  :entry:`inverse`

  :soft:`Type:` :doc:`transform-1.0.0 <transform-1.0.0>`.

  

  Explicitly sets the inverse transform of this transform.
  
  If the transform has a direct analytic inverse, this
  property is usually not necessary, as the ASDF-reading tool
  can provide it automatically.
  
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <transform-1.0.0.yaml>`
.. literalinclude:: transform-1.0.0.yaml
    :language: yaml
    :linenos:


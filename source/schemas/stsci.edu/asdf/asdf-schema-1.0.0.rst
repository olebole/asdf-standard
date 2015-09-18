

.. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0:

asdf-schema: ASDF schema
========================

:soft:`Type:` `draft-01 <http://stsci.edu/schemas/yaml-schema/draft-01>`__ :soft:`and` object.

ASDF schema



A metaschema extending YAML Schema and JSON Schema to add support
for some ASDF-specific checks, related to nd-arrays.



:category:`All of:`



  .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/0:

  :entry:`0`

  :soft:`Type:` `draft-01 <http://stsci.edu/schemas/yaml-schema/draft-01>`__.

  

  



  .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/1:

  :entry:`1`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/1/properties/max_ndim:

    :entry:`max_ndim`

    :soft:`Type:` integer  ≥ 0.

    

    Specifies that the corresponding ndarray is at most the
    given number of dimensions.  If the array has fewer
    dimensions, it should be logically treated as if it were
    "broadcast" to the expected dimensions by adding 1's to the
    front of the shape list.
    
    



    .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/1/properties/ndim:

    :entry:`ndim`

    :soft:`Type:` integer  ≥ 0.

    

    Specifies that the matching ndarray is exactly the given
    number of dimensions.
    
    



    .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/1/properties/datatype:

    :entry:`datatype`

    :soft:`Type:` `datatype-1.0.0 <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0#definitions/datatype-1.0.0>`__.

    

    Specifies the datatype of the ndarray.
    
    By default, an array is considered "matching" if the array
    can be cast to the given datatype without data loss.  For
    exact datatype matching, set :code:`exact_datatype` to :code:`true`.
    
    



    .. _http://stsci.edu/schemas/asdf/asdf-schema-1.0.0/allOf/1/properties/exact_datatype:

    :entry:`exact_datatype`

    :soft:`Type:` boolean.

    

    If :code:`true`, the datatype must match exactly.
    
    

    :soft:`Default:` false

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <asdf-schema-1.0.0.yaml>`
.. literalinclude:: asdf-schema-1.0.0.yaml
    :language: yaml
    :linenos:


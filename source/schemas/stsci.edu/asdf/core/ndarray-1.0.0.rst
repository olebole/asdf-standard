

.. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0:

ndarray: An *n*-dimensional array.
==================================

:soft:`Type:` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>` :soft:`or` object.

An *n*-dimensional array.



There are two ways to store the data in an ndarray.

-  Inline in the tree: This is recommended only for small arrays.  In
   this case, the entire :code:`ndarray` tag may be a nested list, in
   which case the type of the array is inferred from the content. (See
   the rules for type inference in the :code:`inline-data` definition
   below.)  The inline data may also be given in the :code:`data`
   property, in which case it is possible to explicitly specify the
   :code:`datatype` and other properties.

-  External to the tree: The data comes from a :ref:`block <block>`
   within the same ASDF file or an external ASDF file referenced by a
   URI.



:category:`Definitions:`



  .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype:

  :entry:`scalar-datatype`

  :soft:`Type:` string :soft:`from` ["int8", "uint8", "int16", "uint16", "int32", "uint32", "int64", "uint64", "float32", "float64", "complex64", "complex128", "bool8"] :soft:`or` array.

  

  Describes the type of a single element.
  
  There is a set of numeric types, each with a single identifier:
  
  -  :code:`int8`, :code:`int16`, :code:`int32`, :code:`int64`: Signed
     integer types, with the given bit size.
  
  -  :code:`uint8`, :code:`uint16`, :code:`uint32`, :code:`uint64`:
     Unsigned integer types, with the given bit size.
  
  -  :code:`float32`: Single-precision floating-point type or
     "binary32", as defined in IEEE 754.
  
  -  :code:`float64`: Double-precision floating-point type or
     "binary64", as defined in IEEE 754.
  
  -  :code:`complex64`: Complex number where the real and imaginary
     parts are each single-precision floating-point ("binary32")
     numbers, as defined in IEEE 754.
  
  -  :code:`complex128`: Complex number where the real and imaginary
     parts are each double-precision floating-point ("binary64")
     numbers, as defined in IEEE 754.
  
  There are two distinct fixed-length string types, which must
  be indicated with a 2-element array where the first element is an
  identifier for the string type, and the second is a length:
  
  -  :code:`ascii`: A string containing ASCII text (all codepoints <
     128), where each character is 1 byte.
  
  -  :code:`ucs4`: A string containing unicode text in the UCS-4
     encoding, where each character is always 4 bytes long.  Here the
     number of bytes used is 4 times the given length.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype/anyOf/0:

    :entry:`—`

    :soft:`Type:` string :soft:`from` ["int8", "uint8", "int16", "uint16", "int32", "uint32", "int64", "uint64", "float32", "float64", "complex64", "complex128", "bool8"].

    

    



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype/anyOf/1:

    :entry:`—`

    :soft:`Type:` array.

    

    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype/anyOf/1/0:

      :entry:`index[0]`

      :soft:`Type:` string :soft:`from` ["ascii", "ucs4"].

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype/anyOf/1/1:

      :entry:`index[1]`

      :soft:`Type:` integer  ≥ 0.

      

      



  .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype:

  :entry:`datatype`

  :soft:`Type:` :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>` :soft:`or` array :soft:`of` ( :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>` :soft:`or` object ).

  

  The data format of the array elements.  May be a single scalar
  datatype, or may be a nested list of datatypes.  When a list, each field
  may have a name.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/0:

    :entry:`—`

    :soft:`Type:` :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>`.

    

    



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1:

    :entry:`—`

    :soft:`Type:` array :soft:`of` ( :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>` :soft:`or` object ).

    

    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items:

      :soft:`Type:` :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>` :soft:`or` object.

      

      

      :category:`Any of:`



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/0:

        :entry:`—`

        :soft:`Type:` :ref:`definitions/scalar-datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/scalar-datatype>`.

        

        



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1:

        :entry:`—`

        :soft:`Type:` object.

        

        

        :category:`Properties:`



          .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1/properties/name:

          :entry:`name`

          :soft:`Type:` string ( :soft:`regex` :regexp:`[A-Za-z_][A-Za-z0-9_]*` ).

          

          The name of the field
          
          



          .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1/properties/datatype:

          :entry:`datatype`

          :soft:`Type:` :ref:`definitions/datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype>`. Required.

          

          



          .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1/properties/byteorder:

          :entry:`byteorder`

          :soft:`Type:` string :soft:`from` ["big", "little"].

          

          The byteorder for the field.  If not provided, the
          byteorder of the datatype as a whole will be used.
          
          



          .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1/properties/shape:

          :entry:`shape`

          :soft:`Type:` array :soft:`of` ( integer  ≥ 0 ).

          

          

          :category:`Items:`



            .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype/anyOf/1/items/anyOf/1/properties/shape/items:

            :soft:`Type:` integer  ≥ 0.

            

            



  .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data:

  :entry:`inline-data`

  :soft:`Type:` array :soft:`of` ( number :soft:`or` string :soft:`or` null :soft:`or` :doc:`complex-1.0.0 <complex-1.0.0>` :soft:`or` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>` :soft:`or` boolean ).

  

  Inline data is stored in YAML format directly in the tree, rather than
  referencing a binary block.  It is made out of nested lists.
  
  If the datatype of the array is not specified, it is inferred from
  the array contents.  Type inference is supported only for
  homogeneous arrays, not tables.
  
  -  If any of the elements in the array are YAML strings, the
     :code:`datatype` of the entire array is :code:`ucs4`, with the
     width of the largest string in the column, otherwise...
  
  -  If any of the elements in the array are complex numbers, the
     :code:`datatype` of the entire column is :code:`complex128`,
     otherwise...
  
  -  If any of the types in the column are numbers with a decimal point,
     the :code:`datatype` of the entire column is :code:`float64`,
     otherwise..
  
  -  If any of the types in the column are integers, the
     :code:`datatype` of the entire column is :code:`int64`,
     otherwise...
  
  -  The :code:`datatype` of the entire column is :code:`bool8`.
  
  Masked values may be included in the array using :code:`null`.  If an
  explicit mask array is also provided, it takes precedence.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items:

    :soft:`Type:` number :soft:`or` string :soft:`or` null :soft:`or` :doc:`complex-1.0.0 <complex-1.0.0>` :soft:`or` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>` :soft:`or` boolean.

    

    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/0:

      :entry:`—`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/1:

      :entry:`—`

      :soft:`Type:` string.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/2:

      :entry:`—`

      :soft:`Type:` null.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/3:

      :entry:`—`

      :soft:`Type:` :doc:`complex-1.0.0 <complex-1.0.0>`.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/4:

      :entry:`—`

      :soft:`Type:` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>`.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data/items/anyOf/5:

      :entry:`—`

      :soft:`Type:` boolean.

      

      

:category:`Any of:`



  .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/0:

  :entry:`—`

  :soft:`Type:` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>`.

  

  



  .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1:

  :entry:`—`

  :soft:`Type:` object.

  

  

  :category:`Properties:`



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/source:

    :entry:`source`

    :soft:`Type:` integer :soft:`or` string ( :soft:`format` uri ).

    

    The source of the data.
    
    -  If an integer: If positive, the zero-based index of the block
       within the same file. If negative, the index from the last block
       within the same file.  For example, a source of :code:`-1`
       corresponds to the last block in the same file.
    
    -  If a string, a URI to an external ASDF file containing the block
       data.  Relative URIs and :code:`file:` and :code:`http:` protocols
       must be supported.  Other protocols may be supported by specific
       library implementations.
    
    The ability to reference block data in an external ASDF file
    is intentionally limited to the first block in the external
    ASDF file, and is intended only to support the needs of
    :ref:`exploded <exploded>`.  For the more general case of
    referencing data in an external ASDF file, use tree
    :ref:`references <references>`.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/source/anyOf/0:

      :entry:`—`

      :soft:`Type:` integer.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/source/anyOf/1:

      :entry:`—`

      :soft:`Type:` string ( :soft:`format` uri ).

      

      



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/data:

    :entry:`data`

    :soft:`Type:` :ref:`definitions/inline-data <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/inline-data>`.

    

    The data for the array inline.
    
    If :code:`datatype` and/or :code:`shape` are also provided, they must
    match the data here and can be used as a consistency check.
    :code:`strides`, :code:`offset` and :code:`byteorder` are meaningless when
    :code:`data` is provided.
    
    



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/shape:

    :entry:`shape`

    :soft:`Type:` array :soft:`of` ( integer  ≥ 0 :soft:`or` any :soft:`from` ["*"] ).

    

    The shape of the array.
    
    The first entry may be the string :code:`*`, indicating that the
    length of the first index of the array will be automatically
    determined from the size of the block.  This is used for
    streaming support.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/shape/items:

      :soft:`Type:` integer  ≥ 0 :soft:`or` any :soft:`from` ["*"].

      

      

      :category:`Any of:`



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/shape/items/anyOf/0:

        :entry:`—`

        :soft:`Type:` integer  ≥ 0.

        

        



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/shape/items/anyOf/1:

        :entry:`—`

        :soft:`Type:` any :soft:`from` ["*"].

        

        



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/datatype:

    :entry:`datatype`

    :soft:`Type:` :ref:`definitions/datatype <http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/definitions/datatype>`.

    

    The data format of the array elements.
    
    



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/byteorder:

    :entry:`byteorder`

    :soft:`Type:` string :soft:`from` ["big", "little"].

    

    The byte order (big- or little-endian) of the array data.
    
    



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/offset:

    :entry:`offset`

    :soft:`Type:` integer  ≥ 0.

    

    The offset, in bytes, within the data for this start of this view.
    
    

    :soft:`Default:` 0



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/strides:

    :entry:`strides`

    :soft:`Type:` array :soft:`of` ( integer  ≥ 1 :soft:`or` integer  ≤ -1 ).

    

    The number of bytes to skip in each dimension.  If not provided, the array is assumed by be contiguous and in C order.  If provided, must be the same length as the shape property.
    
    

    :category:`Items:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/strides/items:

      :soft:`Type:` integer  ≥ 1 :soft:`or` integer  ≤ -1.

      

      

      :category:`Any of:`



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/strides/items/anyOf/0:

        :entry:`—`

        :soft:`Type:` integer  ≥ 1.

        

        



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/strides/items/anyOf/1:

        :entry:`—`

        :soft:`Type:` integer  ≤ -1.

        

        



    .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask:

    :entry:`mask`

    :soft:`Type:` number :soft:`or` :doc:`complex-1.0.0 <complex-1.0.0>` :soft:`or` :doc:`ndarray-1.0.0 <ndarray-1.0.0>` :soft:`and` any.

    

    Describes how missing values in the array are stored.  If a scalar number, that number is used to represent missing values. If an ndarray, the given array provides a mask, where non-zero values represent missing values in this array.  The mask array must be broadcastable to the dimensions of this array.
    
    

    :category:`Any of:`



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask/anyOf/0:

      :entry:`—`

      :soft:`Type:` number.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask/anyOf/1:

      :entry:`—`

      :soft:`Type:` :doc:`complex-1.0.0 <complex-1.0.0>`.

      

      



      .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask/anyOf/2:

      :entry:`—`

      :soft:`Type:` :doc:`ndarray-1.0.0 <ndarray-1.0.0>` :soft:`and` any.

      

      

      :category:`All of:`



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask/anyOf/2/allOf/0:

        :entry:`0`

        :soft:`Type:` :doc:`ndarray-1.0.0 <ndarray-1.0.0>`.

        

        



        .. _http://stsci.edu/schemas/asdf/core/ndarray-1.0.0/anyOf/1/properties/mask/anyOf/2/allOf/1:

        :entry:`1`

        :soft:`Type:` any.

        

        

:category:`Examples:`

An inline array, with implicit data type::

  !core/ndarray-1.0.0
    [[1, 0, 0],
     [0, 1, 0],
     [0, 0, 1]]
  

An inline array, with an explicit data type::

  !core/ndarray-1.0.0
    datatype: float64
    data:
      [[1, 0, 0],
       [0, 1, 0],
       [0, 0, 1]]
  

An inline structured array, where the types of each column are automatically detected::

  !core/ndarray-1.0.0
    [[M110, 110, 205, And],
     [ M31,  31, 224, And],
     [ M32,  32, 221, And],
     [M103, 103, 581, Cas]]
  

An inline structured array, where the types of each column are explicitly specified::

  !core/ndarray-1.0.0
    datatype: [['ascii', 4], uint16, uint16, ['ascii', 4]]
    data:
      [[M110, 110, 205, And],
       [ M31,  31, 224, And],
       [ M32,  32, 221, And],
       [M103, 103, 581, Cas]]
  

A double-precision array, in contiguous memory in a block within the same file::

  !core/ndarray-1.0.0
    source: 0
    shape: [1024, 1024]
    datatype: float64
    byteorder: little
  

A view of a tile in that image::

  !core/ndarray-1.0.0
    source: 0
    shape: [256, 256]
    datatype: float64
    byteorder: little
    strides: [8192, 8]
    offset: 2099200
  

A structured datatype, with nested columns for a coordinate in (*ra*, *dec*), and a 3x3 convolution kernel::

  !core/ndarray-1.0.0
    source: 0
    shape: [64]
    datatype:
      - name: coordinate
        datatype:
          - name: ra
            datatype: float64
          - name: dec
            datatype: float64
      - name: kernel
        datatype: float32
        shape: [3, 3]
    byteorder: little
  

An array in Fortran order::

  !core/ndarray-1.0.0
    source: 0
    shape: [1024, 1024]
    datatype: float64
    byteorder: little
    strides: [8192, 8]
  

An array where values of -999 are treated as missing::

  !core/ndarray-1.0.0
    source: 0
    shape: [256, 256]
    datatype: float64
    byteorder: little
    mask: -999
  

An array where another array is used as a mask::

  !core/ndarray-1.0.0
    source: 0
    shape: [256, 256]
    datatype: float64
    byteorder: little
    mask: !core/ndarray-1.0.0
      source: 1
      shape: [256, 256]
      datatype: bool8
      byteorder: little
  

An array where the data is stored in the first block in another ASDF file.::

  !core/ndarray-1.0.0
    source: external.asdf
    shape: [256, 256]
    datatype: float64
    byteorder: little
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <ndarray-1.0.0.yaml>`
.. literalinclude:: ndarray-1.0.0.yaml
    :language: yaml
    :linenos:


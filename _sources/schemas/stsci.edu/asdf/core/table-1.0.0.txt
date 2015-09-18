

.. _http://stsci.edu/schemas/asdf/core/table-1.0.0:

table: A table.
===============

:soft:`Type:` object.

A table.



A table is represented as a list of columns, where each entry is a
:ref:`column <http://stsci.edu/schemas/asdf/core/column-1.0.0>`
object, containing the data and some additional information.

The data itself may be stored inline as text, or in binary in either
row- or column-major order by use of the :code:`strides` property on the
individual column arrays.

Each column in the table must have the same first (slowest moving)
dimension.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/core/table-1.0.0/properties/columns:

  :entry:`columns`

  :soft:`Type:` array :soft:`of` ( :doc:`column-1.0.0 <column-1.0.0>` ).

  

  A list of columns in the table.
  
  

  :category:`Items:`



    .. _http://stsci.edu/schemas/asdf/core/table-1.0.0/properties/columns/items:

    :soft:`Type:` :doc:`column-1.0.0 <column-1.0.0>`.

    

    



  .. _http://stsci.edu/schemas/asdf/core/table-1.0.0/properties/meta:

  :entry:`meta`

  :soft:`Type:` object.

  

  Additional free-form metadata about the table.
  
  

  :soft:`Default:` {}

:category:`Examples:`

A table stored in column-major order, with each column in a separate block::

  !core/table-1.0.0
    columns:
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 0
        datatype: float64
        byteorder: little
        shape: [3]
      description: RA
      meta: {foo: bar}
      name: a
      unit: !unit/unit-1.0.0 deg
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 1
        datatype: float64
        byteorder: little
        shape: [3]
      description: DEC
      name: b
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 2
        datatype: [ascii, 1]
        byteorder: big
        shape: [3]
      description: The target name
      name: c
  

A table stored in row-major order, all stored in the same block::

  !core/table-1.0.0
    columns:
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 0
        datatype: float64
        byteorder: little
        shape: [3]
        strides: [13]
      description: RA
      meta: {foo: bar}
      name: a
      unit: !unit/unit-1.0.0 deg
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 0
        datatype: float64
        byteorder: little
        shape: [3]
        offset: 4
        strides: [13]
      description: DEC
      name: b
    - !core/column-1.0.0
      data: !core/ndarray-1.0.0
        source: 0
        datatype: [ascii, 1]
        byteorder: big
        shape: [3]
        offset: 12
        strides: [13]
      description: The target name
      name: c
  

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <table-1.0.0.yaml>`
.. literalinclude:: table-1.0.0.yaml
    :language: yaml
    :linenos:


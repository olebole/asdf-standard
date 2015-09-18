

.. _http://stsci.edu/schemas/asdf/core/column-1.0.0:

column: A column in a table.
============================

:soft:`Type:` object.

A column in a table.



Each column contains a name and an array of data, and an optional description
and unit.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/core/column-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string ( :soft:`regex` :regexp:`[A-Za-z_][A-Za-z0-9_]*` ).

  

  The name of the column.  Each name in a
  `table <http://stsci.edu/schemas/asdf/core/table-1.0.0>`__ must be
  unique.
  
  



  .. _http://stsci.edu/schemas/asdf/core/column-1.0.0/properties/data:

  :entry:`data`

  :soft:`Type:` :doc:`ndarray-1.0.0 <ndarray-1.0.0>`.

  

  The array data for the column.
  
  



  .. _http://stsci.edu/schemas/asdf/core/column-1.0.0/properties/description:

  :entry:`description`

  :soft:`Type:` string.

  

  An optional description of the column.
  
  

  :soft:`Default:` ""



  .. _http://stsci.edu/schemas/asdf/core/column-1.0.0/properties/unit:

  :entry:`unit`

  :soft:`Type:` :doc:`unit-1.0.0 <../unit/unit-1.0.0>`.

  

  An optional unit for the column.
  
  



  .. _http://stsci.edu/schemas/asdf/core/column-1.0.0/properties/meta:

  :entry:`meta`

  :soft:`Type:` object.

  

  Additional free-form metadata about the column.
  
  

  :soft:`Default:` {}

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <column-1.0.0.yaml>`
.. literalinclude:: column-1.0.0.yaml
    :language: yaml
    :linenos:




.. _http://stsci.edu/schemas/asdf/unit/defunit-1.0.0:

defunit: Define a new physical unit.
====================================

:soft:`Type:` object.

Define a new physical unit.



Defines a new unit.  It can be used to either:

-  Define a new base unit.

-  Create a new unit name that is a equivalent to a given unit.

The new unit must be defined before any unit tags that use it.



:category:`Properties:`



  .. _http://stsci.edu/schemas/asdf/unit/defunit-1.0.0/properties/name:

  :entry:`name`

  :soft:`Type:` string ( :soft:`regex` :regexp:`[A-Za-z_][A-Za-z0-9_]+` ). Required.

  

  The name of the new unit.
  
  



  .. _http://stsci.edu/schemas/asdf/unit/defunit-1.0.0/properties/unit:

  :entry:`unit`

  :soft:`Type:` :doc:`unit-1.0.0 <unit-1.0.0>` :soft:`or` null.

  

  The unit that the new name is equivalent to.  It is optional,
  and if not provided, or :code:`null`, this :code:`defunit` defines a new
  base unit.
  
  

  :category:`Any of:`



    .. _http://stsci.edu/schemas/asdf/unit/defunit-1.0.0/properties/unit/anyOf/0:

    :entry:`—`

    :soft:`Type:` :doc:`unit-1.0.0 <unit-1.0.0>`.

    

    



    .. _http://stsci.edu/schemas/asdf/unit/defunit-1.0.0/properties/unit/anyOf/1:

    :entry:`—`

    :soft:`Type:` null.

    

    

Original schema in YAML
-----------------------

.. only:: html

   :download:`[Download raw] <defunit-1.0.0.yaml>`
.. literalinclude:: defunit-1.0.0.yaml
    :language: yaml
    :linenos:

